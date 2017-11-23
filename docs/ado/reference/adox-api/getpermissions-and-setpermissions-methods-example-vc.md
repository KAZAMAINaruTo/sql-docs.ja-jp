---
title: "GetPermissions と SetPermissions メソッドの例 (vc++) |Microsoft ドキュメント"
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: reference
ms.technology: drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: sql
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- SetPermissions method [ADOX], VC++ example
- GetPermissions method [ADOX], VC++ example
ms.assetid: 8c75d547-d3d7-44c4-b7de-eead5d11b92e
caps.latest.revision: "10"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 5a3993cb3047052c5fe553390530c944133a0940
ms.sourcegitcommit: 44cd5c651488b5296fb679f6d43f50d068339a27
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2017
---
# <a name="getpermissions-and-setpermissions-methods-example-vc"></a>GetPermissions と SetPermissions メソッドの例 (vc++)
この例で、 [GetPermissions](../../../ado/reference/adox-api/getpermissions-method-adox.md)と[SetPermissions](../../../ado/reference/adox-api/setpermissions-method-adox.md)メソッドです。 次のコードでは、完全なアクセス権を Orders テーブルに、管理ユーザーに与えられます。  
  
```  
// BeginGrantPermissionCpp.cpp  
// compile with: /EHsc  
#import "msado15.dll" rename("EOF", "EndOfFile")  
#import "msadox.dll" no_namespace  
  
#include "iostream"  
using namespace std;  
  
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);};  
  
int main() {  
   if ( FAILED(::CoInitialize(NULL)) )  
      return -1;  
  
   HRESULT hr = S_OK;  
  
   // Define and initialize ADOX object pointers. These are in ADODB  namespace.  
   _CatalogPtr m_pCatalog = NULL;  
  
   // Define ADODB object pointers;  
   ADODB::_ConnectionPtr m_pCnn = NULL;  
  
   // Define other variables here.  
   try {  
      TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection)));  
  
      // Opens a connection to the northwind database using the Microsoft Jet 4.0 provider  
      m_pCnn->PutProvider("Microsoft.Jet.OLEDB.4.0");  
      m_pCnn->Open("data source='c:\\Northwind.mdb';jet oledb:system database='c:\\system.mdw'", "", "", NULL);  
  
      TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog)));  
  
      m_pCatalog->PutActiveConnection(_variant_t((IDispatch *)m_pCnn));  
  
      // Retrieve original permissions  
      long lngPerm = m_pCatalog->Users->GetItem("admin")->GetPermissions("Orders",adPermObjTable);  
      long lngOrgPerm = lngPerm;  
      cout << "Original Permissions: " << lngPerm << "\n" << endl;  
  
      // Revoke all permissions  
      m_pCatalog->Users->GetItem("admin")->SetPermissions("Orders",   
                                          adPermObjTable, adAccessRevoke, adRightFull, adInheritNone);  
  
      // Display permissions  
      lngPerm = m_pCatalog->Users->GetItem("admin")->GetPermissions("Orders", adPermObjTable);  
      cout << "Revoked permissions: " << lngPerm << "\n" << endl;  
  
      // Give the Admin user full rights on the orders object  
      m_pCatalog->Users->GetItem("admin")->SetPermissions("Orders",   
                                            adPermObjTable, adAccessSet, adRightFull, adInheritNone);  
  
      // Display permissions  
      lngPerm = m_pCatalog->Users->GetItem("admin")->GetPermissions("Orders", adPermObjTable);  
      cout << "Full permissions: " << lngPerm << "\n" << endl;  
  
      // Restore original permissions  
      m_pCatalog->Users->GetItem("admin")->SetPermissions("Orders", adPermObjTable,  
                                                 adAccessSet, (RightsEnum) lngOrgPerm, adInheritNone);  
  
      // Display permissions  
      lngPerm = m_pCatalog->Users->GetItem("admin")->GetPermissions("Orders",adPermObjTable);  
      cout << "Final permissions: " << lngPerm << "\n" << endl;  
   }  
   catch(_com_error &e) {  
      // Notify the user of errors if any.  
      _bstr_t bstrSource(e.Source());  
      _bstr_t bstrDescription(e.Description());  
  
      printf("\n\tSource :  %s \n\tdescription : %s \n ", (LPCSTR)bstrSource, (LPCSTR)bstrDescription);  
   }  
   catch(...) {  
      cout << "Error occured in GrantPermissionsX...."<< endl;  
   }  
   ::CoUninitialize();  
}  
```
