---
title: 'レッスン 3: レポート サーバーからレポート定義の読み込み |Microsoft Docs'
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- reporting-services-native
ms.topic: conceptual
ms.assetid: 5ad8b31c-43b0-4481-a31b-090cbed4a438
author: craigg-msft
ms.author: douglasl
manager: craigg
ms.openlocfilehash: c9555f2ec58aefa5f0a3b071b0d4cf7c8ee7ff14
ms.sourcegitcommit: 9ece10c2970a4f0812647149d3de2c6b75713e14
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2018
ms.locfileid: "51813875"
---
# <a name="lesson-3-load-a-report-definition-from-the-report-server"></a>レッスン 3 : レポート サーバーからのレポート定義の読み込み
  プロジェクトを作成し、RDL スキーマからクラスを生成すると、レポート定義をレポート サーバーから読み込めるようになります。  
  
### <a name="to-load-a-report-definition"></a>レポート定義を読み込むには  
  
1.  上部にあるプライベート フィールドを追加、`ReportUpdater`クラス (モジュールを使用する場合[!INCLUDE[vbprvb](../includes/vbprvb-md.md)]) の`Report`クラス。 このフィールドは、アプリケーションの動作中、レポート サーバーから読み込んだレポートへの参照を保持するために使用されます。  
  
    ```csharp  
    private Report _report;  
    ```  
  
    ```vb  
    Private m_report As Report  
    ```  
  
2.  Program.cs ファイル ([!INCLUDE[vbprvb](../includes/vbprvb-md.md)] では Module1.vb) で、`LoadReportDefinition()` メソッドのコードを次のコードに置き換えます。  
  
    ```csharp  
    private void LoadReportDefinition()  
    {  
        System.Console.WriteLine("Loading Report Definition");  
  
        string reportPath =   
            "/AdventureWorks 2012 Sample Reports/Company Sales 2012";  
  
        // Retrieve the report definition   
        // from the report server  
        byte[] bytes =   
            _reportService.GetItemDefinition(reportPath);  
  
        if (bytes != null)  
        {  
            XmlSerializer serializer =   
                new XmlSerializer(typeof(Report));  
  
            // Load the report bytes into a memory stream  
            using (MemoryStream stream = new MemoryStream(bytes))  
            {  
                // Deserialize the report stream to an   
                // instance of the Report class  
                _report = (Report)serializer.Deserialize(stream);  
            }  
        }  
    }  
    ```  
  
    ```vb  
    Private Sub LoadReportDefinition()  
  
        System.Console.WriteLine("Loading Report Definition")  
  
        Dim reportPath As String = _  
            "/AdventureWorks 2012 Sample Reports/Company Sales 2012"  
  
        'Retrieve the report definition   
        'from the report server  
        Dim bytes As Byte() = _  
            m_reportService.GetItemDefinition(reportPath)  
  
        If Not (bytes Is Nothing) Then  
  
            Dim serializer As XmlSerializer = _  
                New XmlSerializer(GetType(Report))  
  
            'Load the report bytes into a memory stream  
            Using stream As MemoryStream = New MemoryStream(bytes)  
  
                'Deserialize the report stream to an   
                'instance of the Report class  
                m_report = CType(serializer.Deserialize(stream), _  
                                 Report)  
  
            End Using  
  
        End If  
  
    End Sub  
    ```  
  
## <a name="next-lesson"></a>次のレッスン  
 次のレッスンでは、レポート サーバーから読み込んだレポート定義を更新するコードを記述します。 参照してください[レッスン 4: レポート定義をプログラムで更新](../../2014/tutorials/lesson-4-update-the-report-definition-programmatically.md)します。  
  
## <a name="see-also"></a>参照  
 [RDL スキーマから生成されたクラスを使用してレポートを更新&#40;SSRS チュートリアル&#41;](../../2014/tutorials/updating-reports-using-classes-generated-from-the-rdl-schema-ssrs-tutorial.md)   
 [レポート定義言語 &#40;SSRS&#41;](../reporting-services/reports/report-definition-language-ssrs.md)  
  
  
