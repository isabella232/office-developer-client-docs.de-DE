---
title: Recordset2.Bookmarkable-Eigenschaft (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 9c93d04d-ca10-acf5-122a-58625ed93424
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198125(v=office.15)
ms:contentKeyID: 48546601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052888
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: f92bcb53fe9ab93d877b008b7646a609fa65541f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596946"
---
# <a name="recordset2bookmarkable-property-dao"></a>Recordset2.Bookmarkable-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der angibt, ob ein **Recordset**-Objekt Textmarken unterstützt, die Sie unter Verwendung der **[Bookmark](recordset2-bookmark-property-dao.md)**-Eigenschaft festlegen können.

## <a name="syntax"></a>Syntax

*Ausdruck* . Bookmarkable

*Ausdruck* Eine Variable, die ein **Recordset2-Objekt** darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

Überprüfen Sie den Wert der **Bookmarkable**-Eigenschaft eines **Recordset**-Objekts, bevor Sie versuchen, die **Bookmark**-Eigenschaft festzulegen oder zu überprüfen.

Für **Recordset-Objekte,** die vollständig auf Tabellen des Microsoft Access-Datenbankmoduls basieren, lautet der Wert der **Bookmarkable-Eigenschaft** "True", und Sie können Lesezeichen verwenden. Andere Datenbank-Produkte unterstützen Textmarken möglicherweise nicht. Sie können Textmarken nicht in beliebigen **Recordset** -Objekten verwenden, die auf einer verknüpften Paradox-Tabelle basieren, die keinen primären Schlüssel besitzt.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Eigenschaften **Bookmark** und **Bookmarkable** verwendet, damit der Benutzer einen Datensatz in einer Datensatzgruppe kennzeichnen und später zu ihm zurückkehren kann.

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset2 
     Dim strMessage As String 
     Dim intCommand As Integer 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenSnapshot) 
     
     With rstCategories 
     
     If .Bookmarkable = False Then 
     Debug.Print "Recordset is not Bookmarkable!" 
     Else 
     ' Populate Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show information about current record and get 
     ' user input. 
     strMessage = "Category: " & !CategoryName & _ 
     " (record " & (.AbsolutePosition + 1) & _ 
     " of " & .RecordCount & ")" & vbCr & _ 
     "Enter command:" & vbCr & _ 
     "[1 - next / 2 - previous /" & vbCr & _ 
     "3 - set bookmark / 4 - go to bookmark]" 
     intCommand = Val(InputBox(strMessage)) 
     
     Select Case intCommand 
     ' Move forward or backward, trapping for BOF 
     ' or EOF. 
     Case 1 
     .MoveNext 
     If .EOF Then .MoveLast 
     Case 2 
     .MovePrevious 
     If .BOF Then .MoveFirst 
     
     ' Store the bookmark of the current record. 
     Case 3 
     varBookmark = .Bookmark 
     
     ' Go to the record indicated by the stored 
     ' bookmark. 
     Case 4 
     If IsEmpty(varBookmark) Then 
     MsgBox "No Bookmark set!" 
     Else 
     .Bookmark = varBookmark 
     End If 
     
     Case Else 
     Exit Do 
     End Select 
     
     Loop 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
