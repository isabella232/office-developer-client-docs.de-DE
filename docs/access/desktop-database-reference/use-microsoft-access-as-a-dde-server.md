---
title: Verwenden von Microsoft Access als DDE-server
TOCTitle: Use Microsoft Access as a DDE Server
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 84b4e30877488d84e03839764c1996053e76a2e7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475184"
---
# <a name="use-microsoft-access-as-a-dde-server"></a>Verwenden von Microsoft Access als DDE-server

**Betrifft**: Access 2013 | Office 2013 

Microsoft Access unterstützt dynamischem Datenaustausch (DDE) als eine Anwendung Ziel (Client) oder quellanwendung (Server). Beispielsweise kann eine Anwendung wie Microsoft Word, der als ein Client fungiert Daten über DDE aus einer Microsoft Access-Datenbank anfordern, der als Server fungiert.

> [!TIP]
> Wenn Sie Microsoft Access-Objekte aus einer anderen Anwendung bearbeiten müssen, können Sie Automatisierung verwenden möchten.

Eine DDE-Verbindung zwischen einem Client und Server wird zu einem bestimmten Thema eingerichtet. Ein Thema kann entweder eine Datendatei im Format von der Serveranwendung unterstützt werden, oder es kann sein, das Thema "System", die Informationen über die Serveranwendung selbst bereitstellt. Nachdem eine Unterhaltung zu einem bestimmten Thema begonnen hat, kann nur ein mit diesem Thema verbundenes Datenelement übertragen werden.

Nehmen wir beispielsweise bei Microsoft Word ausgeführt werden und Daten aus einer bestimmten Microsoft Access-Datenbank in ein Dokument einfügen möchten. Sie zunächst eine DDE-Verbindung mit Microsoft Access öffnen einen DDE-Kanal mit der **DDEInitiate** -Funktion und der Name der Datenbankdatei als Thema angeben. Sie können dann Daten aus dieser Datenbank an Microsoft Word über den Kanal übertragen.

Als DDE-Server unterstützt Microsoft Access die folgenden Themen:

  - Das Thema "System"

  - Der Name einer Datenbank (Thema*Datenbank* )

  - Der Name einer Tabelle (Thema*Tabellenname* )

  - Der Name einer Abfrage (Thema*Abfragename* )

  - Eine Microsoft Access SQL-Zeichenfolge (Thema*SQLZeichenfolge* )

Nachdem Sie eine DDE-Verbindung hergestellt haben, können Sie die Anweisung **DDEExecute** , einen Befehl vom Client an die Server-Anwendung zu senden. Wenn als DDE-Server verwendet wird, erkennt Microsoft Access die folgenden Befehle als gültig:

  - Der Name eines Makros in der aktuellen Datenbank.

  - Alle Aktionen, die Sie in Visual Basic können mithilfe der Methoden des **DoCmd** -Objekts.

  - Die OpenDatabase und SchließenDatenbank-Aktionen, die nur für DDE-Vorgänge verwendet werden. (Ein Beispiel dafür, wie Sie diese Aktionen verwenden, finden Sie weiter unten in diesem Thema.)


> [!NOTE]
> <P>Wenn Sie eine Makroaktion als Anweisung <STRONG>DDEExecute</STRONG> angeben, die Aktion und Argumenten führen Sie die Syntax der <STRONG>DoCmd</STRONG> -Objekt und müssen in Klammern ([]) eingeschlossen werden. Allerdings erkennen, die DDE unterstützen keine systeminterne Konstanten in DDE-Vorgänge. Darüber hinaus Zeichenfolgenargumente müssen in Anführungszeichen eingeschlossen werden (""), wenn die Zeichenfolge ein Komma enthält. Anderenfalls sind Anführungszeichen nicht erforderlich.</P>



Die Client-Anwendung können Sie die **DDERequest** -Funktion Textdaten aus der Serveranwendung über einen geöffneten DDE-Kanal verwenden. Oder der Client kann die Anweisung **DDEPoke** zum Senden von Daten an die Serveranwendung verwenden. Sobald die Datenübertragung abgeschlossen ist, kann der Client die Anweisung **DDETerminate** zum Schließen des DDE-Kanals oder der **DDETerminateAll** -Anweisung zum Schließen aller geöffneten Kanäle verwenden.


> [!NOTE]
> <P>Wenn die Clientanwendung empfangen von Daten über einen DDE-Kanal beendet wurde, sollte es den Kanal um Speicherressourcen zu sparen schließen.</P>



Im folgenden Beispiel wird veranschaulicht, wie Sie eine Microsoft Word-Prozedur mit Visual Basic erstellen, die Microsoft Access als DDE-Server verwendet. (Für das Beispiel funktioniert, muss Microsoft Access ausgeführt werden.)

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

Die folgenden Abschnitte enthalten Informationen zu den gültigen DDE-Themen, die von Microsoft Access unterstützt.

## <a name="the-system-topic"></a>Das Thema "System"

Das Systemthema befindet sich standard für alle Microsoft Windows-basierten Anwendungen. Es liefert Informationen zu den anderen Themen, die von der Anwendung unterstützt. Zugriff auf diese Informationen muss Code rufen Sie zunächst die **DDEInitiate** -Funktion mit als Argument *Thema* , und klicken Sie dann die **DDERequest** -Anweisung mit einer der folgenden Angaben für das Argument *Element* ausführen.

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
<td><p>"SysItems" verwenden</p></td>
<td><p>Eine Liste der Elemente, die von dem Thema "System" in Microsoft Access unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>Formate</p></td>
<td><p>Eine Liste der Formate können Microsoft Access in die Zwischenablage kopieren.</p></td>
</tr>
<tr class="odd">
<td><p>Status</p></td>
<td><p>&quot;Ausgelastet&quot; oder &quot;bereit&quot;.</p></td>
</tr>
<tr class="even">
<td><p>Topics</p></td>
<td><p>Eine Liste aller geöffneten Datenbanken.</p></td>
</tr>
</tbody>
</table>


Das folgende Beispiel veranschaulicht die Verwendung der Funktionen **DDEInitiate** und **DDERequest** mit dem Thema System:

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

## <a name="the-database-topic"></a>Das Thema Datenbank

Das Thema *Datenbank* ist der Dateiname einer vorhandenen Datenbank. Sie können entweder nur den Namen der (Nordwind) oder den Pfad der Erweiterung eingeben (C:\\Access\\Beispiele\\Nordwind.mdb). Nach dem start einer DDE-Verbindung mit der Datenbank können Sie eine Liste der Objekte in der Datenbank anfordern.


> [!NOTE]
> <P>Sie können keine DDE verwenden, um Microsoft Access-Arbeitsgruppen-Informationsdatei abzufragen.</P>



Das Thema *Datenbank* unterstützt die folgenden Elemente.

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
<td><p>TableList</p></td>
<td><p>Eine Liste der Tabellen.</p></td>
</tr>
<tr class="even">
<td><p>QueryList</p></td>
<td><p>Eine Liste von Abfragen.</p></td>
</tr>
<tr class="odd">
<td><p>FormList</p></td>
<td><p>Eine Liste von Formularen.</p></td>
</tr>
<tr class="even">
<td><p>ReportList</p></td>
<td><p>Eine Liste der Berichte.</p></td>
</tr>
<tr class="odd">
<td><p>MacroList</p></td>
<td><p>Eine Liste mit Makros.</p></td>
</tr>
<tr class="even">
<td><p>ModuleList</p></td>
<td><p>Eine Liste von Modulen.</p></td>
</tr>
<tr class="odd">
<td><p>ViewList</p></td>
<td><p>Eine Liste der Ansichten</p></td>
</tr>
<tr class="even">
<td><p>StoredProcedureList</p></td>
<td><p>Eine Liste von gespeicherten Prozeduren</p></td>
</tr>
<tr class="odd">
<td><p>DatabaseDiagramList</p></td>
<td><p>Eine Liste der Datenbankdiagramme</p></td>
</tr>
</tbody>
</table>


Das folgende Beispiel zeigt, wie Sie das Formular Personal in der Northwind-Beispieldatenbank aus einer Visual Basic-Prozedur öffnen können:

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

## <a name="the-table-topic"></a>Das Thema Tabelle

In diesen Themen verwenden Sie die folgende Syntax:

_Databasename_ ; **Tabelle** _TableName_

_Databasename_ ; **Abfrage** _Abfragename_

_Databasename_ ; **SQL** [ _Sqlstring_ ]

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
<td><p><em>Datenbankname</em></p></td>
<td><p>Der Name der Datenbank, die die Tabelle oder Abfrage in ist oder, die die SQL-Anweisung betrifft, gefolgt von einem Semikolon (;). Der Name der Datenbank kann nur den Namen der (Nordwind) oder der vollständige Pfad und MDB-Erweiterung (C:\Access\Samples\Northwind.mdb) sein.</p></td>
</tr>
<tr class="even">
<td><p><em>TableName</em></p></td>
<td><p>Der Name einer vorhandenen Tabelle.</p></td>
</tr>
<tr class="odd">
<td><p><em>Abfragename</em></p></td>
<td><p>Der Name einer vorhandenen Abfrage.</p></td>
</tr>
<tr class="even">
<td><p><em>SqlString</em></p></td>
<td><p>Eine gültige SQL­Anweisung bis zu 256 Zeichen lang sein, mit einem Semikolon enden. Um mehr als 256 Zeichen austauschen möchten, geben Sie dieses Argument und stattdessen verwenden Sie aufeinander folgenden <strong>DDEPoke</strong> -Anweisungen zum Erstellen einer SQL-Anweisung. Der folgenden Visual Basic-Code wird beispielsweise die Anweisung <strong>DDEPoke</strong> So erstellen eine SQL-Anweisung, und fordern Sie dann die Ergebnisse der Abfrage verwendet.</p></td>
</tr>
</tbody>
</table>

<br/>

In der folgenden Tabelle sind die gültigen Elemente für die Tabelle *Tabellenname*, QUERY *Abfragename*und SQL *SQLZeichenfolge* Themen.

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
<td><p>Die Daten in der Tabelle, einschließlich Feldnamen.</p></td>
</tr>
<tr class="even">
<td><p>Daten</p></td>
<td><p>Alle Zeilen mit Daten, ohne Feldnamen.</p></td>
</tr>
<tr class="odd">
<td><p>FieldNames</p></td>
<td><p>Eine einzeilige Liste von Feldnamen.</p></td>
</tr>
<tr class="even">
<td><p>FieldNames; T</p></td>
<td><p>Eine zwei Zeilen Liste von Feldnamen (erste Zeile) und deren Datentypen (zweite Zeile).</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>Dies sind die zurückgegebenen Werte und die Datentypen, die sie darstellen:</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><b>Wert</b></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>5</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>6</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>7</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>8</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>11</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>12</p></td>
</tr>
<tr class="even">
<td><p>NextRow</p></td>
<td><p>Die Daten in der nächsten Zeile in der Tabelle oder Abfrage. Wenn Sie einen Kanal öffnen, gibt NextRow die Daten in der ersten Zeile. Wenn die aktuelle Zeile der letzte Datensatz ist und Ausführung von NextRow, schlägt die Anforderung fehl.</p></td>
</tr>
<tr class="odd">
<td><p>Fehl</p></td>
<td><p>Die Daten in der vorherigen Zeile in der Tabelle oder Abfrage. Wenn fehl die erste Anforderung über einen neuen Kanal ist, werden die Daten in der letzten Zeile der Tabelle oder Abfrage zurückgegeben. Wenn der erste Datensatz der aktuelle Zeile ist, schlägt die Anforderung fehl.</p></td>
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
<td><p>FieldCount</p></td>
<td><p>Die Anzahl der Felder in der Tabelle oder Abfrage.</p></td>
</tr>
<tr class="odd">
<td><p>SQLText</p></td>
<td><p>Eine SQL-Anweisung, die die Tabelle oder Abfrage darstellt. Für Tabellen, gibt dieses Element eine SQL-Anweisung in der Form &quot;auswählen `*` FROM <em>Tabelle</em>; &quot;.</p></td>
</tr>
<tr class="even">
<td><p>SQLText; <em>n</em></p></td>
<td><p>Eine SQL­Anweisung in <em>n</em>-Segmenten für eine Tabelle oder Abfrage, wobei <em>n</em> eine ganze Zahl bis zu 256 ist Zeichen. Nehmen wir beispielsweise bei eine Abfrage wird durch die folgende SQL-Anweisung dargestellt: das Element &quot;SQLText; 7&quot; gibt die folgenden Abschnitte Tabstopp-getrennt: das Element &quot;SQLText; 7&quot; gibt die folgenden Abschnitte Tabstopp-getrennt:</p></td>
</tr>
</tbody>
</table>


Das folgende Beispiel zeigt, wie Sie DDE in einer Visual Basic-Prozedur das Abrufen von Daten aus einer Tabelle in der Northwind-Beispieldatenbank verwenden und diese Daten in eine Textdatei einfügen:

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
