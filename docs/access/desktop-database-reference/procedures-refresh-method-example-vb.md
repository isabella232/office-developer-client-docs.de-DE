---
title: Refresh-Methode (Procedures) (VB-Beispiel)
TOCTitle: Procedures Refresh method example (VB)
ms:assetid: fd6d71cf-7a6b-49d7-220b-dd5b815a92ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250300(v=office.15)
ms:contentKeyID: 48548916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b75b7de4e63c9083dff550c5362e48bf171ee5e2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887567"
---
# <a name="procedures-refresh-method-example-vb"></a><span data-ttu-id="47ee5-102">Refresh-Methode (Procedures) (VB-Beispiel)</span><span class="sxs-lookup"><span data-stu-id="47ee5-102">Procedures Refresh method example (VB)</span></span>


<span data-ttu-id="47ee5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47ee5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47ee5-p101">Im folgenden Code wird die Aktualisierung der [Procedures](procedures-collection-adox.md)-Auflistung eines [Catalog](catalog-object-adox.md)-Objekts veranschaulicht. Dies ist erforderlich, bevor auf [Procedure](procedure-object-adox.md)-Objekte im **Catalog** -Objekt zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="47ee5-p101">The following code shows how to refresh the [Procedures](procedures-collection-adox.md) collection of a [Catalog](catalog-object-adox.md). This is required before [Procedure](procedure-object-adox.md) objects from the **Catalog** can be accessed.</span></span>

```vb 
 
' BeginProceduresRefreshVB 
Sub Main() 
 On Error GoTo ProcedureRefreshError 
 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog 
 cat.ActiveConnection = _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Refresh the Procedures collection 
 cat.Procedures.Refresh 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Exit Sub 
 
ProcedureRefreshError: 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndProceduresRefreshVB 
```

