---
title: Zugreifen auf Zeilen in einem hierarchischen Recordset
TOCTitle: Accessing rows in a hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a80b089fa72ef01eb1b4b2f1dae494e002c6a6fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698239"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a>Zugreifen auf Zeilen in einem hierarchischen Recordset

**Betrifft**: Access 2013, Office 2013

Das folgende Beispiel zeigt die notwendigen Schritte zum Zugreifen auf Zeilen in einem hierarchischen [Recordset](recordset-object-ado.md):

1. Recordset-Objekte aus den Tabellen authors und titleauthor werden nach Autor-Nr. miteinander in Beziehung gesetzt.

2. In der äußeren Schleife werden der Vor- und Nachname, der Status und die Identifikation jedes Autors angezeigt.

3. Das angefügte **Recordset** für jede Zeile wird aus der **Fields**-Auflistung abgerufen und *rstTitleAuthor* zugewiesen.

4. In der inneren Schleife werden vier Felder aus jeder Zeile im angefügten **Recordset** angezeigt.

> [!NOTE] 
> [StayInSync](stayinsync-property-ado.md) -Eigenschaft wird zur Veranschaulichung, auf FALSE festgelegt, damit Sie sehen können, das Kapitel in jeder Iteration der äußeren Schleife explizit ändern. Das Beispiel ist jedoch effizienter, wenn die Zuweisung in Schritt 3 vor die erste Zeile in Schritt 2 verschoben wird, sodass die Zuweisung nur ein Mal ausgeführt wird. **StayInSync** -Eigenschaft auf TRUE festgelegt, sodass *RstTitleAuthor* implizit und automatisch in das entsprechende Kapitel geändert wird, wenn *Rst* an eine neue Zeile verschoben wird.

**Beispiel**

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

