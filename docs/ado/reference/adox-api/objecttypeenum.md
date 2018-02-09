---
title: ObjectTypeEnum | Microsoft Docs
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: ado
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: sql
ms.tgt_pltfrm: 
ms.topic: article
apitype: COM
f1_keywords:
- ObjectTypeEnum
helpviewer_keywords:
- ObjectTypeEnum enumeration [ADOX]
ms.assetid: 3fdecfca-aa91-4596-ad98-610f1b7f840b
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 2deffcf2d45b5b2fe8920435ab06b139c80143ab
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/09/2018
---
# <a name="objecttypeenum"></a>ObjectTypeEnum
Ownership のいずれかのアクセス許可を設定する対象のデータベース オブジェクトの種類を指定します。  
  
|定数|[値]|Description|  
|--------------|-----------|-----------------|  
|**adPermObjColumn**|2|オブジェクトは、列です。|  
|**adPermObjDatabase**|3|オブジェクトは、データベースです。|  
|**adPermObjProcedure**|4|オブジェクトは、プロシージャです。|  
|**adPermObjProviderSpecific**|-1|オブジェクトは、プロバイダーによって定義された型です。 場合、エラーが発生、 *ObjectType*パラメーターは**adPermObjProviderSpecific**と*ObjectTypeId*が指定されていません。|  
|**adPermObjTable**|1|オブジェクトは、テーブルです。|  
|**adPermObjView**|5|オブジェクトは、ビューです。|  
  
## <a name="applies-to"></a>適用対象  
  
|||  
|-|-|  
|[GetObjectOwner メソッド (ADOX)](../../../ado/reference/adox-api/getobjectowner-method-adox.md)|[GetPermissions メソッド (ADOX)](../../../ado/reference/adox-api/getpermissions-method-adox.md)|  
|[SetObjectOwner メソッド](../../../ado/reference/adox-api/setobjectowner-method.md)|[SetPermissions メソッド (ADOX)](../../../ado/reference/adox-api/setpermissions-method-adox.md)|
