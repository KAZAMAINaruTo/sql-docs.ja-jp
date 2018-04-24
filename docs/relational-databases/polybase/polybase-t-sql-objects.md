---
title: PolyBase T-SQL オブジェクト | Microsoft Docs
ms.custom: ''
ms.date: 08/15/2017
ms.prod: sql
ms.prod_service: database-engine, sql-data-warehouse, pdw
ms.service: ''
ms.component: polybase
ms.reviewer: ''
ms.suite: sql
ms.technology:
- database-engine-polybase
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- PolyBase, fundamentals
- PolyBase, SQL statements
- PolyBase, SQL objects
caps.latest.revision: 20
author: barbkess
ms.author: barbkess
manager: craigg
ms.workload: On Demand
ms.openlocfilehash: 56339954a2ae2cf0f2bb69acfeaec787621fd20e
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2018
---
# <a name="polybase-t-sql-objects"></a>PolyBase T-SQL オブジェクト
[!INCLUDE[appliesto-ss-xxxx-asdw-pdw-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
  PolyBase を使用するには、外部テーブルを作成して、外部データを参照する必要があります。  
  
 [CREATE DATABASE SCOPED CREDENTIAL &#40;Transact-SQL&#41;](../../t-sql/statements/create-database-scoped-credential-transact-sql.md)  
  
 [CREATE EXTERNAL DATA SOURCE &#40;Transact-SQL&#41;](../../t-sql/statements/create-external-data-source-transact-sql.md)  
  
 [CREATE EXTERNAL FILE FORMAT &#40;Transact-SQL&#41;](../../t-sql/statements/create-external-file-format-transact-sql.md)  
  
 [CREATE EXTERNAL TABLE &#40;Transact-SQL&#41;](../../t-sql/statements/create-external-table-transact-sql.md)  
  
 [CREATE STATISTICS &#40;Transact-SQL&#41;](../../t-sql/statements/create-statistics-transact-sql.md)  
 
> [!NOTE]
>  SQL Server 2016 の PolyBase は、Windows ユーザーのみをサポートします。 SQL ユーザーを使って PolyBase の外部テーブルをクエリしようとすると、クエリは失敗します。

## <a name="prerequisites"></a>Prerequisites  
 PolyBase を構成します。 「 [PolyBase configuration](../../relational-databases/polybase/polybase-configuration.md)」を参照してください。  
  
## <a name="create-external-tables-for-hadoop"></a>Hadoop の外部テーブルの作成
適用対象: SQL Server (2016 以降)、Parallel Data Warehouse
  
 **1.データベース スコープ ベースの資格情報を作成する**  
  
 この手順が必要なのは、Kerberos でセキュリティ保護された Hadoop クラスターのみです。  
  
```sql  
-- Create a master key on the database.  
-- Required to encrypt the credential secret.  
  
CREATE MASTER KEY ENCRYPTION BY PASSWORD = 'S0me!nfo';  
  
-- Create a database scoped credential  for Kerberos-secured Hadoop clusters.  
-- IDENTITY: the Kerberos user name.  
-- SECRET: the Kerberos password  
  
CREATE DATABASE SCOPED CREDENTIAL HadoopUser1   
WITH IDENTITY = '<hadoop_user_name>', Secret = '<hadoop_password>';  
  
```  
  
 **2.外部データ ソースを作成する**  
  
```sql  
-- Create an external data source.  
-- LOCATION (Required) : Hadoop Name Node IP address and port.  
-- RESOURCE MANAGER LOCATION (Optional): Hadoop Resource Manager location to enable pushdown computation.  
-- CREDENTIAL (Optional):  the database scoped credential, created above.  
  
CREATE EXTERNAL DATA SOURCE MyHadoopCluster WITH (  
        TYPE = HADOOP,   
        LOCATION ='hdfs://10.xxx.xx.xxx:xxxx',   
        RESOURCE_MANAGER_LOCATION = '10.xxx.xx.xxx:xxxx',   
        CREDENTIAL = HadoopUser1      
);  
  
```  
  
 **3.外部のファイル形式を作成する**  
  
```sql  
-- Create an external file format.  
-- FORMAT TYPE: Type of format in Hadoop (DELIMITEDTEXT,  RCFILE, ORC, PARQUET).  
  
CREATE EXTERNAL FILE FORMAT TextFileFormat WITH (  
        FORMAT_TYPE = DELIMITEDTEXT,   
        FORMAT_OPTIONS (FIELD_TERMINATOR ='|',   
                USE_TYPE_DEFAULT = TRUE)  
  
```  
  
 **4.外部テーブルを作成する**  
  
```sql  
-- Create an external table pointing to data stored in Hadoop.  
-- LOCATION: path to file or directory that contains the data (relative to HDFS root).  
  
CREATE EXTERNAL TABLE [dbo].[CarSensor_Data] (  
        [SensorKey] int NOT NULL,   
        [CustomerKey] int NOT NULL,   
        [GeographyKey] int NULL,   
        [Speed] float NOT NULL,   
        [YearMeasured] int NOT NULL  
)  
WITH (LOCATION='/Demo/',   
        DATA_SOURCE = MyHadoopCluster,  
        FILE_FORMAT = TextFileFormat  
);  
  
```  
  
 **5.統計を作成する**  
  
```sql  
-- Create statistics on an external table.   
CREATE STATISTICS StatsForSensors on CarSensor_Data(CustomerKey, Speed)  
  
```  
  
## <a name="create-external-tables-for-azure-blob-storage"></a>Azure BLOB ストレージ用の外部テーブルを作成します。  
適用対象: SQL Server (2016 以降)、Azure SQL Data Warehouse、Parallel Data Warehouse

 **1.データベース スコープ ベースの資格情報を作成する**  
  
```sql  
-- Create a master key on the database.  
-- Required to encrypt the credential secret.  
  
CREATE MASTER KEY ENCRYPTION BY PASSWORD = 'S0me!nfo';  
  
-- Create a database scoped credential  for Azure blob storage.  
-- IDENTITY: any string (this is not used for authentication to Azure storage).  
-- SECRET: your Azure storage account key.  
  
CREATE DATABASE SCOPED CREDENTIAL AzureStorageCredential   
WITH IDENTITY = 'user', Secret = '<azure_storage_account_key>';  
  
```  
  
 **2.外部データ ソースを作成する**  
  
```sql  
-- Create an external data source.  
-- LOCATION:  Azure account storage account name and blob container name.  
-- CREDENTIAL: The database scoped credential created above.  
  
CREATE EXTERNAL DATA SOURCE AzureStorage with (  
        TYPE = HADOOP,   
        LOCATION ='wasbs://<blob_container_name>@<azure_storage_account_name>.blob.core.windows.net',  
        CREDENTIAL = AzureStorageCredential  
);  
  
```  
  
 **3.外部のファイル形式を作成する**  
  
```sql  
-- Create an external file format.  
-- FORMAT TYPE: Type of format in Hadoop (DELIMITEDTEXT,  RCFILE, ORC, PARQUET).  
  
CREATE EXTERNAL FILE FORMAT TextFileFormat WITH (  
        FORMAT_TYPE = DELIMITEDTEXT,   
        FORMAT_OPTIONS (FIELD_TERMINATOR ='|',   
                USE_TYPE_DEFAULT = TRUE)  
  
```  
  
 **4.外部テーブルを作成する**  
  
```sql  
-- Create an external table pointing to data stored in Azure storage.  
-- LOCATION: path to a file or directory that contains the data (relative to the blob container).  
-- To point to all files under the blob container, use LOCATION='/'   
  
CREATE EXTERNAL TABLE [dbo].[CarSensor_Data] (  
        [SensorKey] int NOT NULL,   
        [CustomerKey] int NOT NULL,   
        [GeographyKey] int NULL,   
        [Speed] float NOT NULL,   
        [YearMeasured] int NOT NULL  
)  
WITH (LOCATION='/Demo/',   
        DATA_SOURCE = AzureStorage,  
        FILE_FORMAT = TextFileFormat  
);  
  
```  
  
 **5.統計を作成する**  
  
```sql  
-- Create statistics on an external table.   
CREATE STATISTICS StatsForSensors on CarSensor_Data(CustomerKey, Speed)  
  
```  
 
## <a name="create-external-tables-for-azure-data-lake-store"></a>Azure Data Lake Store 用の外部テーブルを作成する
適用対象: Azure SQL Data Warehouse

詳しくは、「[Azure Data Lake Store から Azure SQL Data Warehouse へのデータの読み込み](https://docs.microsoft.com/en-us/azure/sql-data-warehouse/sql-data-warehouse-load-from-azure-data-lake-store)」をご覧ください
 
 **1.データベース スコープ ベースの資格情報を作成する**   

```sql
-- Create a Database Master Key.
-- Only necessary if one does not already exist.
-- Required to encrypt the credential secret in the next step.

CREATE MASTER KEY;

-- Create a database scoped credential
-- IDENTITY: Pass the client id and OAuth 2.0 Token Endpoint taken from your Azure Active Directory Application
-- SECRET: Provide your AAD Application Service Principal key.
-- For more information on Create Database Scoped Credential: https://msdn.microsoft.com/en-us/library/mt270260.aspx

CREATE DATABASE SCOPED CREDENTIAL ADL_User
WITH
    IDENTITY = '<client_id>@<OAuth_2.0_Token_EndPoint>'
    ,SECRET = '<key>'
;
```  
  
 **2.外部データ ソースを作成する**  
  
```sql  
-- TYPE: HADOOP - PolyBase uses Hadoop APIs to access data in Azure Data Lake Store.
-- LOCATION: Provide Azure storage account name and blob container name.
-- CREDENTIAL: Provide the credential created in the previous step.

CREATE EXTERNAL DATA SOURCE AzureDataLakeStore
WITH (
    TYPE = HADOOP,
    LOCATION = 'adl://<AzureDataLake account_name>.azuredatalake.net,
    CREDENTIAL = AzureStorageCredential
);
```  
  
 **3.外部のファイル形式を作成する**  
  
```sql  
-- FIELD_TERMINATOR: Marks the end of each field (column) in a delimited text file
-- STRING_DELIMITER: Specifies the field terminator for data of type string in the text-delimited file.
-- DATE_FORMAT: Specifies a custom format for all date and time data that might appear in a delimited text file.
-- Use_Type_Default: Store all Missing values as NULL

CREATE EXTERNAL FILE FORMAT TextFileFormat
WITH
(   FORMAT_TYPE = DELIMITEDTEXT
,    FORMAT_OPTIONS    (   FIELD_TERMINATOR = '|'
                    ,    STRING_DELIMITER = ''
                    ,    DATE_FORMAT         = 'yyyy-MM-dd HH:mm:ss.fff'
                    ,    USE_TYPE_DEFAULT = FALSE
                    )
);
```  
  
 **4.外部テーブルを作成する**  
  
```sql  
-- LOCATION: Folder under the ADLS root folder.
-- DATA_SOURCE: Specifies which Data Source Object to use.
-- FILE_FORMAT: Specifies which File Format Object to use
-- REJECT_TYPE: Specifies how you want to deal with rejected rows. Either Value or percentage of the total
-- REJECT_VALUE: Sets the Reject value based on the reject type.

-- DimProduct
CREATE EXTERNAL TABLE [dbo].[DimProduct_external] (
    [ProductKey] [int] NOT NULL,
    [ProductLabel] [nvarchar](255) NULL,
    [ProductName] [nvarchar](500) NULL
)
WITH
(
    LOCATION='/DimProduct/'
,   DATA_SOURCE = AzureDataLakeStore
,   FILE_FORMAT = TextFileFormat
,   REJECT_TYPE = VALUE
,   REJECT_VALUE = 0
)
;
```  
  
 **5.統計を作成する**  
  
```sql     
CREATE STATISTICS StatsForProduct on DimProduct_external(ProductKey)  
```  

## <a name="next-steps"></a>次の手順  
 クエリの例については、「 [PolyBase Queries (PolyBase のクエリ)](../../relational-databases/polybase/polybase-queries.md)」を参照してください。  
  
## <a name="see-also"></a>参照  
 [PolyBase の概要](../../relational-databases/polybase/get-started-with-polybase.md)   
 [PolyBase ガイド](../../relational-databases/polybase/polybase-guide.md)  
  
  
