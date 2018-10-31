---
title: Delete-Methode (Views) (VB-Beispiel)
TOCTitle: Views Delete method example (VB)
ms:assetid: 423cd4e6-dfa5-8559-b1f3-b789a7aa9590
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249194(v=office.15)
ms:contentKeyID: 48544474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 251a8429e11a59d9276c79034c68860375cba7e7
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861071"
---
# <a name="views-delete-method-example-vb"></a><span data-ttu-id="92d11-102">Delete-Methode (Views) (VB-Beispiel)</span><span class="sxs-lookup"><span data-stu-id="92d11-102">Views Delete method example (VB)</span></span>


<span data-ttu-id="92d11-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="92d11-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="92d11-104">Im folgenden Code wird die Verwendung der [Delete](delete-method-adox-collections.md)-Methode veranschaulicht, um eine Sicht aus dem Katalog zu löschen.</span><span class="sxs-lookup"><span data-stu-id="92d11-104">The following code shows how to use the [Delete](delete-method-adox-collections.md) method to delete a view from the catalog.</span></span>

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

