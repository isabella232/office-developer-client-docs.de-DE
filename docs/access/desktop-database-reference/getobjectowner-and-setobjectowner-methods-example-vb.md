---
title: GetObjectOwner- und SetObjectOwner-Methode (Beispiel) (VB)
TOCTitle: GetObjectOwner and SetObjectOwner methods example (VB)
ms:assetid: 0a30cce1-7626-8db3-4af4-84098c284db0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248833(v=office.15)
ms:contentKeyID: 48543146
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec71ee93a0c513b9a613c9f1c1a8a6b7d39a6d4e
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025889"
---
# <a name="getobjectowner-and-setobjectowner-methods-example-vb"></a><span data-ttu-id="1a855-102">GetObjectOwner- und SetObjectOwner-Methode (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="1a855-102">GetObjectOwner and SetObjectOwner methods example (VB)</span></span>


<span data-ttu-id="1a855-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a855-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a855-104">Dieses Beispiel veranschaulicht die Methoden [GetObjectOwner](getobjectowner-method-adox.md) und [SetObjectOwner verwenden](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) .</span><span class="sxs-lookup"><span data-stu-id="1a855-104">This example demonstrates the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) methods.</span></span> <span data-ttu-id="1a855-105">Dieser Code wird vorausgesetzt, dass die Gruppe Accounting (siehe die [Gruppen und Benutzer anzufügen, ChangePassword-Methoden (Beispiel) (VB)](groups-and-users-append-changepassword-methods-example-vb.md) wie das System dieser Gruppe hinzugefügt angezeigt).</span><span class="sxs-lookup"><span data-stu-id="1a855-105">This code assumes the existence of the group Accounting (see the [Groups and Users Append, ChangePassword methods example (VB)](groups-and-users-append-changepassword-methods-example-vb.md) to see how to add this group to the system).</span></span> <span data-ttu-id="1a855-106">Der Besitzer der Kategorientabelle wird auf Buchhaltung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1a855-106">The owner of the Categories table is set to Accounting.</span></span>

```vb 
 
' BeginOwnersVB 
Sub Main() 
 On Error GoTo OwnersXError 
 
 Dim tblLoop As New ADOX.Table 
 Dim cat As New ADOX.Catalog 
 Dim strOwner As String 
 
 ' Open the Catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" & _ 
 "jet oledb:system database=" & _ 
 "'c:\Program Files\Microsoft Office\Office\system.mdw'" 
 
 ' Print the original owner of Categories 
 strOwner = cat.GetObjectOwner("Categories", adPermObjTable) 
 Debug.Print "Owner of Categories: " & strOwner 
 
 ' Set the owner of Categories to Accounting 
 cat.SetObjectOwner "Categories", adPermObjTable, "Accounting" 
 
 ' List the owners of all tables and columns in the catalog. 
 For Each tblLoop In cat.Tables 
 Debug.Print "Table: " & tblLoop.Name 
 Debug.Print " Owner: " & _ 
 cat.GetObjectOwner(tblLoop.Name, adPermObjTable) 
 Next tblLoop 
 
 ' Restore the original owner of Categories 
 cat.SetObjectOwner "Categories", adPermObjTable, strOwner 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Exit Sub 
 
OwnersXError: 
 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndOwnersVB 
```

