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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281956"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a>Zugreifen auf Zeilen in einem hierarchischen Recordset

**Gilt für**: Access 2013, Office 2013

Das folgende Beispiel zeigt die notwendigen Schritte zum Zugreifen auf Zeilen in einem hierarchischen [Recordset](recordset-object-ado.md):

1. **Recordset** objects from the authors and titleauthor tables are related by author ID.

2. In der äußeren Schleife werden der Vor- und Nachname, der Status und die Identifikation jedes Autors angezeigt.

3. Das angefügte **Recordset** für jede Zeile wird aus der **Fields**-Auflistung abgerufen und *rstTitleAuthor* zugewiesen.

4. In der inneren Schleife werden vier Felder aus jeder Zeile im angefügten **Recordset** angezeigt.

> [!NOTE] 
> Die [StayInSync](stayinsync-property-ado.md) -Eigenschaft ist für Zwecke der Illustration auf false festgelegt, sodass Sie die Kapitel Änderung explizit in jeder Iteration der äußeren Schleife sehen können. Das Beispiel ist jedoch effizienter, wenn die Zuweisung in Schritt 3 vor die erste Zeile in Schritt 2 verschoben wird, sodass die Zuweisung nur ein Mal ausgeführt wird. Legen Sie die **StayInSync** -Eigenschaft auf true fest, sodass *rstTitleAuthor* implizit und automatisch in das entsprechende Kapitel wechselt, wenn *RST* zu einer neuen Zeile wechselt.

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

