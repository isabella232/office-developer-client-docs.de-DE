---
title: Delete-Methode (Views) (VB-Beispiel)
TOCTitle: Views Delete method example (VB)
ms:assetid: 423cd4e6-dfa5-8559-b1f3-b789a7aa9590
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249194(v=office.15)
ms:contentKeyID: 48544474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d737f003e02dcf7ffd6cd8dfcac1574f30ec3903
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621563"
---
# <a name="views-delete-method-example-vb"></a>Delete-Methode (Views) (VB-Beispiel)


**Gilt für**: Access 2013, Office 2013

Im folgenden Code wird die Verwendung der [Delete](delete-method-adox-collections.md)-Methode veranschaulicht, um eine Sicht aus dem Katalog zu löschen.

```vb 
 
' BeginDeleteViewVB 
Sub Main() 
 On Error GoTo DeleteViewError 
 
 Dim cat As New ADOX.Catalog 
 
 ' Open the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 'Delete the View 
 cat.Views.Delete "AllCustomers" 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Exit Sub 
 
DeleteViewError: 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndDeleteViewVB 
```

