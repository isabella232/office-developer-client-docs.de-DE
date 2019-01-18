---
title: Recordset2.CopyQueryDef-Methode (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: 36689ac0-f8a6-1f3e-4170-799141373777
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192474(v=office.15)
ms:contentKeyID: 48544170
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053073
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 8a643dae0b67cf4f2a2a0148619d9a8f4df7e6f0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703489"
---
# <a name="recordset2copyquerydef-method-dao"></a>Recordset2.CopyQueryDef-Methode (DAO)


**Betrifft**: Access 2013, Office 2013 

Gibt ein **[QueryDef](querydef-object-dao.md)** -Objekt, das eine Kopie des **QueryDef-Objekt** ist verwendeten zum Erstellen des **[Recordset](recordset-object-dao.md)** -Objekts, dargestellt durch das Recordset-Objekt-Platzhalter (nur Microsoft Access-Arbeitsbereiche). .

## <a name="syntax"></a>Syntax

*Ausdruck* . CopyQueryDef

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="return-value"></a>Rückgabewert

QueryDef

## <a name="remarks"></a>Bemerkungen

Mithilfe der **CopyQueryDef**-Methode können Sie ein neues **QueryDef**-Objekt erstellen, welches ein Duplikat des **QueryDef**-Objekts darstellt, das zum Erstellen des **Recordset**-Objekts dient.

Wurde zum Erstellen dieses **Recordset**-Objekts kein **QueryDef**-Objekt verwendet, tritt ein Fehler auf. Sie müssen zuerst ein **Recordset**-Objekt mithilfe der **OpenRecordset**-Methode öffnen, bevor Sie die **CopyQueryDef**-Methode verwenden.

Diese Methode ist hilfreich, wenn Sie ein **Recordset**-Objekt aus einem **QueryDef**-Objekt erstellen und das **Recordset**-Objekt an eine Funktion übergeben, die die SQL-Entsprechung der Abfrage erneut erstellen muss, beispielsweise um sie zu ändern.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **CopyQueryDef**-Methode zum Erstellen der Kopie eines **QueryDef**-Objekts aus einem vorhandenen **Recordset**-Objekt verwendet. Die Kopie wird durch das Hinzufügen einer Klausel zur SQL-Eigenschaft geändert. Beim Erstellen eines permanenten **QueryDef**-Objekts können Sie der SQL-Eigenschaft Leerzeichen, Semikolon und Zeilenvorschub hinzufügen. Diese zusätzlichen Zeichen müssen entfernt werden, bevor neue Klauseln an die SQL-Anweisung angehängt werden können.

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
     strAdd As String) As QueryDef 
     
     Dim strSQL As String 
     Dim strRightSQL As String 
     
     Set CopyQueryNew = rstTemp.CopyQueryDef 
     With CopyQueryNew 
     ' Strip extra characters. 
     strSQL = .SQL 
     strRightSQL = Right(strSQL, 1) 
     Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
     strRightSQL = Chr(10) Or strRightSQL = vbCr 
     strSQL = Left(strSQL, Len(strSQL) - 1) 
     strRightSQL = Right(strSQL, 1) 
     Loop 
     .SQL = strSQL & strAdd 
     End With 
     
    End Function 
```     

<br/>

Dieses Beispiel zeigt eine mögliche Verwendung von CopyQueryNew().

```vb
Sub CopyQueryDefX() 
 
 Dim dbsNorthwind As Database 
 Dim qdfEmployees As QueryDef 
 Dim rstEmployees As Recordset2 
 Dim intCommand As Integer 
 Dim strOrderBy As String 
 Dim qdfCopy As QueryDef 
 Dim rstCopy As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
 "NewQueryDef", "SELECT FirstName, LastName, " & _ 
 "BirthDate FROM Employees") 
 Set rstEmployees = qdfEmployees.OpenRecordset( _ 
 dbOpenForwardOnly) 
 
 Do While True 
 intCommand = Val(InputBox( _ 
 "Choose field on which to order a new " & _ 
 "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
 "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
 "[Cancel - exit]")) 
 Select Case intCommand 
 Case 1 
 strOrderBy = " ORDER BY FirstName" 
 Case 2 
 strOrderBy = " ORDER BY LastName" 
 Case 3 
 strOrderBy = " ORDER BY BirthDate" 
 Case Else 
 Exit Do 
 End Select 
 Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
 Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
 dbForwardOnly) 
 With rstCopy 
 Do While Not .EOF 
 Debug.Print !LastName & ", " & !FirstName & _ 
 " - " & !BirthDate 
 .MoveNext 
 Loop 
 .Close 
 End With 
 Exit Do 
 Loop 
 
 rstEmployees.Close 
 ' Delete new QueryDef because this is a demonstration. 
 dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

