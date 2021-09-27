---
title: Workspace.OpenDatabase-Methode (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: f7edb66a036c986f1e1d7ed52dcb5985743f930c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621507"
---
# <a name="workspaceopendatabase-method-dao"></a>Workspace.OpenDatabase-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Öffnet eine bestimmte Datenbank in einem **[Workspace](workspace-object-dao.md)**-Objekt und gibt einen Verweis auf das **[Database](database-object-dao.md)**-Objekt zurück, das es darstellt.

## <a name="syntax"></a>Syntax

*expression* .OpenDatabase(***Name** _, _*_Options_*_, _*_ReadOnly_*_, _*_Connect_**)

*Ausdruck* Eine Variable, die ein **Workspace**-Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>der Name einer vorhandenen Microsoft Access-Datenbankmoduldatei, oder der Dastenquellname (DSN) einer ODBC-Datenquelle. Weitere Informationen zum Festlegen dieses Werts finden Sie in der <strong><a href="connection-name-property-dao.md">Name</a></strong>-Eigenschaft.</p></td>
</tr>
<tr class="even">
<td><p><em>Optionen</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Legt entsprechend der Angaben unter den Hinweisen verschiedene Optionen für die Datenbank fest.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong>, wenn Sie eine Datenbank nur mit Lesezugriff öffnen möchten, oder <strong>False</strong> (Standard), wenn Sie die Datenbank mit Lese-/Schreibzugriff öffnen möchten.</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Gibt verschiedene Verbindungsinformationen an, einschließlich der Kenntwörter.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Datenbank

## <a name="remarks"></a>Bemerkungen

Sie können für das Options-Argument folgende Werte verwenden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Einstellung</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>True</strong></p></td>
<td><p>Öffnet die Datenbank im Exklusivmodus.</p></td>
</tr>
<tr class="even">
<td><p><strong>False</strong></p></td>
<td><p>(Standard) Öffnet die Datenbank im Freigabemodus.</p></td>
</tr>
</tbody>
</table>

<br/>

Wenn Sie eine Datenbank öffnen, wird sie automatisch zur **Databases**-Sammlung hinzugefügt.

Einige Aspekte sollten bei der Verwendung von dbname berücksichtigt werden:

- Wenn er sich auf eine Datenbank bezieht, die bereits für den Zugriff durch einen anderen Benutzer geöffnet wurde, tritt ein Fehler auf.

- Wenn er sich nicht auf eine vorhandene Datenbank oder einen gültigen ODBC-Datenquellennamen bezieht, tritt ein Fehler auf.

- Wenn es sich um eine Zeichenfolge mit der Länge null handelt ("") und *connect* gleich "ODBC;" ist, wird ein Dialogfeld mit allen registrierten ODBC-Datenquellennamen angezeigt, sodass der Benutzer eine Datenbank auswählen kann.

Um eine Datenbank zu schließen und so das **Database**-Objekt aus der **Databases**-Auflistung zu entfernen, verwenden Sie für das Objekt die **[Close](connection-close-method-dao.md)**-Methode.

> [!NOTE]
> Wenn Sie auf eine ODBC-Datenquelle zugreifen, die mit einem Microsoft Access-Datenbankmodul verbunden ist, können Sie die Leistung der Anwendung verbessern, indem Sie ein **Database**-Objekt öffnen, das mit der ODBC-Datenquelle verbunden ist, anstatt einzelne **[TableDef](tabledef-object-dao.md)**-Objekte mit bestimmten Tabellen in der ODBC-Datenquelle zu verknüpfen.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **OpenDatabase** Methode zum Öffnen einer Microsoft Access-Datenbank und zwei mit dem Microsoft Access-Datenbankmodul verbundenen ODBC-Datenbanken verwendet.

```vb 
Sub OpenDatabaseX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsPubs As Database 
 Dim dbsPubs2 As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 ' Open Database object from saved Microsoft Access database 
 ' for exclusive use. 
 MsgBox "Opening Northwind..." 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb", _ 
 True) 
 
 ' Open read-only Database object based on information in 
 ' the connect string. 
 MsgBox "Opening pubs..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set dbsPubs = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverNoPrompt, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Database object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening second copy of pubs..." 
 Set dbsPubs2 = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 Debug.Print "Database properties for " & _ 
 dbsLoop.Name & ":" 
 
 On Error Resume Next 
 ' Enumerate the Properties collection of each Database 
 ' object. 
 For Each prpLoop In dbsLoop.Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 dbsLoop.Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 Next dbsLoop 
 
 dbsNorthwind.Close 
 dbsPubs.Close 
 dbsPubs2.Close 
 wrkAcc.Close 
 
End Sub 
 
```

