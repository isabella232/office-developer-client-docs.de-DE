---
title: Verwenden von Microsoft Access als DDE-Server
TOCTitle: Use Microsoft Access as a DDE Server
description: Microsoft Access unterstützt den dynamischen Datenaustausch (Dynamic Data Exchange, DDE) als Zielanwendung (Clientanwendung) oder als Quellanwendung (Serveranwendung).
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 0de1c6e053b57fa5ba4c69ba2a999ab35e541f5c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593362"
---
# <a name="use-microsoft-access-as-a-dde-server"></a>Verwenden von Microsoft Access als DDE-Server

**Gilt für**: Access 2013, Office 2013 

Microsoft Access unterstützt den dynamischen Datenaustausch (Dynamic Data Exchange, DDE) als Zielanwendung (Clientanwendung) oder als Quellanwendung (Serveranwendung). Beispielsweise kann eine Anwendung wie Microsoft Word, die als Client fungiert, Daten über DDE von einer Microsoft Access-Datenbank anfordern, die als Server fungiert.

> [!TIP]
> Wenn Sie Microsoft Access-Objekte aus einer anderen Anwendung bearbeiten müssen, sollten Sie die Automatisierung in Betracht ziehen.

In einem bestimmten Thema wird eine DDE-Unterhaltung zwischen einem Client und einem Server eingerichtet. Ein Thema kann entweder eine Datendatei in dem format sein, das von der Serveranwendung unterstützt wird, oder es kann das Thema "System" sein, das Informationen über die Serveranwendung selbst bereitstellt. Nachdem eine Unterhaltung zu einem bestimmten Thema begonnen hat, kann nur ein diesem Thema zugeordnetes Datenelement übertragen werden.

Angenommen, Sie führen Microsoft Word aus und möchten Daten aus einer bestimmten Microsoft Access-Datenbank in ein Dokument einfügen. Sie beginnen eine DDE-Unterhaltung mit Microsoft Access, indem Sie einen DDE-Kanal mit der **DDEInitiate-Funktion** öffnen und den Namen der Datenbankdatei als Thema angeben. Anschließend können Sie Daten aus dieser Datenbank über diesen Kanal an Microsoft Word übertragen.

Als DDE-Server unterstützt Microsoft Access die folgenden Themen:

- Das Thema "System"

- Der Name einer Datenbank (*Datenbankthema)*

- Der Name einer Tabelle (*Thema "Tabellenname")*

- Der Name einer Abfrage (*Thema "Abfragename")*

- Eine Microsoft Access-SQL zeichenfolge *(SqlString-Thema)*

Nachdem Sie eine DDE-Unterhaltung eingerichtet haben, können Sie die **DDEExecute-Anweisung** verwenden, um einen Befehl vom Client an die Serveranwendung zu senden. Bei Verwendung als DDE-Server erkennt Microsoft Access Folgendes als gültigen Befehl:

- Der Name eines Makros in der aktuellen Datenbank.

- Jede Aktion, die Sie in Visual Basic ausführen können, indem Sie eine der Methoden des **DoCmd-Objekts** verwenden.

- Die OpenDatabase- und CloseDatabase-Aktionen, die nur für DDE-Vorgänge verwendet werden. (Ein Beispiel für die Verwendung dieser Aktionen finden Sie im Beispiel weiter unten in diesem Thema.)

> [!NOTE]
> Wenn Sie eine Makroaktion als **DDEExecute-Anweisung** angeben, folgen die Aktion und alle Argumente der DoCmd-Objektsyntax und müssen in Klammern ([ ]) eingeschlossen werden.  Anwendungen, die DDE unterstützen, erkennen jedoch keine systeminternen Konstanten in DDE-Vorgängen. Außerdem müssen Zeichenfolgenargumente in Anführungszeichen (" ") eingeschlossen werden, wenn die Zeichenfolge ein Komma enthält. Andernfalls sind Anführungszeichen nicht erforderlich.

Die Clientanwendung kann die **DDERequest-Funktion** verwenden, um Textdaten von der Serveranwendung über einen geöffneten DDE-Kanal anzufordern. Oder der Client kann die **DDEPoke-Anweisung** verwenden, um Daten an die Serveranwendung zu senden. Nach Abschluss der Datenübertragung kann der Client die **DDETerminate-Anweisung** verwenden, um den DDE-Kanal zu schließen, oder die **DDETerminateAll-Anweisung,** um alle geöffneten Kanäle zu schließen.

> [!NOTE]
> Wenn ihre Clientanwendung den Empfang von Daten über einen DDE-Kanal abgeschlossen hat, sollte sie diesen Kanal schließen, um Speicherressourcen zu sparen.

Im folgenden Beispiel wird veranschaulicht, wie Sie eine Microsoft Word Prozedur mit Visual Basic erstellen, die Microsoft Access als DDE-Server verwendet. (Damit dieses Beispiel funktioniert, muss Microsoft Access ausgeführt werden.)

```vb
    Sub AccessDDE() 
        Dim intChan1 As Integer, intChan2 As Integer 
        Dim strQueryData As String 
     
        ' Use System topic to open Northwind sample database. 
        ' Database must be open before using other DDE topics. 
        intChan1 = DDEInitiate("MSAccess", "System") 
        ' You may need to change this path to point to actual location 
        ' of Northwind sample database. 
        DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]" 
     
        ' Get all data from Ten Most Expensive Products query. 
        intChan2 = DDEInitiate("MSAccess", "Northwind.mdb;" _ 
            & "QUERY Ten Most Expensive Products") 
        strQueryData = DDERequest(intChan2, "All") 
        DDETerminate intChan2 
     
        ' Close database. 
        DDEExecute intChan1, "[CloseDatabase]" 
        DDETerminate intChan1 
     
        ' Print retrieved data to Debug Window. 
        Debug.Print strQueryData 
    End Sub
```

<br/>

Die folgenden Abschnitte enthalten Informationen zu den gültigen DDE-Themen, die von Microsoft Access unterstützt werden.

## <a name="the-system-topic"></a>Das Thema "System"

Das Thema "System" ist ein Standardthema für alle Microsoft Windows-basierten Anwendungen. Es liefert Informationen zu den anderen Themen, die von der Anwendung unterstützt werden. Um auf diese Informationen zugreifen zu können, muss der Code zuerst die **DDEInitiate-Funktion** mit dem *Argument "topic"* aufrufen und dann die **DDERequest-Anweisung** mit einer der folgenden Für das *Elementargument* angegebenen Anweisungen ausführen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Element</p></th>
<th><p>Rückgabewerte</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SysItems</p></td>
<td><p>Eine Liste der Elemente, die vom Thema "System" in Microsoft Access unterstützt werden.</p></td>
</tr>
<tr class="even">
<td><p>Formate</p></td>
<td><p>Eine Liste der Formate, die Microsoft Access in die Zwischenablage kopieren kann.</p></td>
</tr>
<tr class="odd">
<td><p>Status</p></td>
<td><p>&quot;Ausgelastet &quot; oder &quot; &quot; bereit.</p></td>
</tr>
<tr class="even">
<td><p>Viva Topics</p></td>
<td><p>Eine Liste aller geöffneten Datenbanken.</p></td>
</tr>
</tbody>
</table>

<br/>

Im folgenden Beispiel wird die Verwendung der Funktionen **DDEInitiate** und **DDERequest** mit dem Thema "System" veranschaulicht:

```vb
    ' In Visual Basic, initiate DDE conversation with Microsoft Access. 
    Dim intChan1 As Integer, strResults As String 
    intChan1 = DDEInitiate("MSAccess", "System") 
    ' Request list of topics supported by System topic. 
    strResults = DDERequest(intChan1, "SysItems") 
    ' Run OpenDatabase action to open Northwind.mdb. 
    ' You may need to change this path to point to actual location 
    ' of Northwind sample database. 
    DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]"
```

## <a name="the-database-topic"></a>Das Thema "Datenbank"

Das *Datenbankthema* ist der Dateiname einer vorhandenen Datenbank. Sie können entweder nur den Basisnamen (Northwind) oder den Pfad und die MDB-Erweiterung (C: \\ Access \\ Samples \\ Northwind.mdb) eingeben. Nachdem Sie eine DDE-Unterhaltung mit der Datenbank gestartet haben, können Sie eine Liste der Objekte in dieser Datenbank anfordern.

> [!NOTE]
> Sie können DDE nicht zum Abfragen der Informationsdatei der Microsoft Access-Arbeitsgruppe verwenden.

Das *Datenbankthema* unterstützt die folgenden Elemente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Element</p></th>
<th><p>Rückgabewerte</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Tablelist</p></td>
<td><p>Eine Liste von Tabellen</p></td>
</tr>
<tr class="even">
<td><p>QueryList</p></td>
<td><p>Eine Liste von Abfragen</p></td>
</tr>
<tr class="odd">
<td><p>FormList</p></td>
<td><p>Eine Liste von Formularen</p></td>
</tr>
<tr class="even">
<td><p>ReportList</p></td>
<td><p>Eine Liste von Berichten</p></td>
</tr>
<tr class="odd">
<td><p>MacroList</p></td>
<td><p>Eine Liste von Makros</p></td>
</tr>
<tr class="even">
<td><p>ModuleList</p></td>
<td><p>Eine Liste von Modulen</p></td>
</tr>
<tr class="odd">
<td><p>ViewList</p></td>
<td><p>Eine Liste von Ansichten</p></td>
</tr>
<tr class="even">
<td><p>StoredProcedureList</p></td>
<td><p>Eine Liste der gespeicherten Prozeduren</p></td>
</tr>
<tr class="odd">
<td><p>DatabaseDiagramList</p></td>
<td><p>Eine Liste von Datenbankdiagrammen</p></td>
</tr>
</tbody>
</table>

<br/>

Das folgende Beispiel zeigt, wie Sie das Formular Employees in der Northwind-Beispieldatenbank über eine Visual Basic Prozedur öffnen können:

```vb
    ' In Visual Basic, initiate DDE conversation with 
    ' Northwind sample database. 
    ' Make sure database is open. 
    intChan2 = DDEInitiate("MSAccess", "Northwind") 
    ' Request list of forms in Northwind sample database. 
    strResponse = DDERequest(intChan2, "FormList") 
    ' Run OpenForm action and arguments to open Employees form. 
    DDEExecute intChan2, "[OpenForm Employees,0,,,1,0]"
```

## <a name="the-table-topic"></a>Das TABLE-Thema

Diese Themen verwenden die folgende Syntax:

_databasename_ ; **TABLE-Tabellenname** 

_databasename_ ; **QUERY-Abfragename** 

_databasename_ ; **SQL** [ _sqlstring_ ]

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Teil</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Databasename</em></p></td>
<td><p>Der Name der Datenbank, in der sich die Tabelle oder Abfrage befindet oder auf die sich die SQL-Anweisung bezieht, gefolgt von einem Semikolon (;). Der Datenbankname kann nur der Basisname (Northwind) oder der vollständige Pfad und die MDB-Erweiterung (C:\Access\Samples\Northwind.mdb) sein.</p></td>
</tr>
<tr class="even">
<td><p><em>Tablename</em></p></td>
<td><p>Der Name einer vorhandenen Tabelle.</p></td>
</tr>
<tr class="odd">
<td><p><em>queryname</em></p></td>
<td><p>Der Name einer vorhandenen Abfrage.</p></td>
</tr>
<tr class="even">
<td><p><em>Sqlstring</em></p></td>
<td><p>Eine gültige SQL Anweisung mit einer Länge von bis zu 256 Zeichen, die mit einem Semikolon endet. Wenn Sie mehr als 256 Zeichen austauschen möchten, lassen Sie dieses Argument aus, und verwenden Sie stattdessen aufeinander folgende <strong>DDEPoke-Anweisungen,</strong> um eine SQL Anweisung zu erstellen. Im folgenden Visual Basic Code wird beispielsweise die <strong>DDEPoke</strong> -Anweisung verwendet, um eine SQL Anweisung zu erstellen und dann die Ergebnisse der Abfrage anzufordern.</p></td>
</tr>
</tbody>
</table>

<br/>

In der folgenden Tabelle sind die gültigen Elemente für die Themen TABLE *tablename,* QUERY *queryname* und SQL *sqlstring* aufgeführt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Element</p></th>
<th><p>Rückgabewerte</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Alle</p></td>
<td><p>Alle Daten in der Tabelle, einschließlich Feldnamen.</p></td>
</tr>
<tr class="even">
<td><p>Daten</p></td>
<td><p>Alle Datenzeilen ohne Feldnamen.</p></td>
</tr>
<tr class="odd">
<td><p>FieldNames</p></td>
<td><p>Eine einzeilige Liste von Feldnamen.</p></td>
</tr>
<tr class="even">
<td><p>FieldNames; T</p></td>
<td><p>Eine aus zwei Zeilen bestehenden Liste der Feldnamen (erste Zeile) und deren Datentypen (zweite Zeile).</p>
<p>Dies sind die zurückgegebenen Werte:</p>
<p>Wert</p>
<p><ul>
<li>0</li>
<li>1</li>
<li>2</li>
<li>3</li>
<li>4 </li>
<li>5</li>
<li>6 </li>
<li>7 </li>
<li>8 </li>
<li>9 </li>
<li>10</li>
<li>11</li>
<li>12 </li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p>NextRow</p></td>
<td><p>Die Daten in der nächsten Zeile in der Tabelle oder Abfrage. Wenn Sie einen Kanal öffnen, gibt NextRow die Daten in der ersten Zeile zurück. Wenn die aktuelle Zeile der letzte Datensatz ist und Sie NextRow ausführen, schlägt die Anforderung fehl.</p></td>
</tr>
<tr class="odd">
<td><p>PrevRow</p></td>
<td><p>Die Daten in der vorherigen Zeile in der Tabelle oder Abfrage. Wenn PrevRow die erste Anforderung in einem neuen Kanal ist, werden die Daten in der letzten Zeile der Tabelle oder Abfrage zurückgegeben. Wenn der erste Datensatz die aktuelle Zeile ist, schlägt die Anforderung für PrevRow fehl.</p></td>
</tr>
<tr class="even">
<td><p>FirstRow</p></td>
<td><p>Die Daten in der ersten Zeile der Tabelle oder Abfrage.</p></td>
</tr>
<tr class="odd">
<td><p>LastRow</p></td>
<td><p>Die Daten in der letzten Zeile der Tabelle oder Abfrage.</p></td>
</tr>
<tr class="even">
<td><p>Fieldcount</p></td>
<td><p>Die Anzahl der Felder in der Tabelle oder Abfrage.</p></td>
</tr>
<tr class="odd">
<td><p>SQLText</p></td>
<td><p>Eine SQL Anweisung, die die Tabelle oder Abfrage darstellt. Bei Tabellen gibt dieses Element eine SQL Anweisung im Formular &quot; SELECT `*` <em>FROM-Tabelle</em>zurück; &quot; .</p></td>
</tr>
<tr class="even">
<td><p>SQLText; <em>n</em></p></td>
<td><p>Eine SQL Anweisung in <em>n-Zeichen-Blöcken,</em>die die Tabelle oder Abfrage darstellt, wobei <em>n</em> eine ganze Zahl von bis zu 256 ist. Angenommen, eine Abfrage wird durch die folgende SQL Anweisung dargestellt: Das Element &quot; SQLText;7 &quot; gibt die folgenden durch Tabstopps getrennten Blöcke zurück: Das Element &quot; SQLText;7 &quot; gibt die folgenden durch Tabstopps getrennten Blöcke zurück:</p></td>
</tr>
</tbody>
</table>

<br/>

Das folgende Beispiel zeigt, wie Sie DDE in einer Visual Basic-Prozedur verwenden können, um Daten aus einer Tabelle in der Northwind-Beispieldatenbank anzufordern und diese Daten in eine Textdatei einzufügen:

```vb
    Sub NorthwindDDE 
        Dim intChan1 As Integer, intChan2 As Integer, intChan3 As Integer 
        Dim strResp1 As Variant, strResp2 As Variant, strResp3 As Variant 
     
        ' In a Visual Basic module, get data from Categories table, 
        ' Catalog query, and Orders table in Northwind.mdb. 
        ' Make sure database is open first. 
        intChan1 = DDEInitiate("MSAccess", "Northwind;TABLE Shippers") 
        intChan2 = DDEInitiate("MSAccess", "Northwind;QUERY Catalog") 
        intChan3 = DDEInitiate("MSAccess", "Northwind;SQL SELECT * " _ 
            & "FROM Orders " _ 
            & "WHERE OrderID > 10050;") 
     
        strResp1 = DDERequest(intChan1, "All") 
        strResp2 = DDERequest(intChan2, "FieldNames;T") 
        strResp3 = DDERequest(intChan3, "FieldNames;T") 
        DDETerminate intChan1 
        DDETerminate intChan2 
        DDETerminate intChan3 
     
        ' Insert data into text file. 
        Open "C:\DATA.TXT" For Append As #1 
        Print #1, strResp1 
        Print #1, strResp2 
        Print #1, strResp3 
        Close #1 
    End Sub
```
