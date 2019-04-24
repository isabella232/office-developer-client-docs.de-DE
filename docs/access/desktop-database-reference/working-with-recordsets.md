---
title: Verwenden von Recordsets
TOCTitle: Working with Recordsets
ms:assetid: 9cd52866-2738-8150-381c-eee0b8a6cd36
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249711(v=office.15)
ms:contentKeyID: 48546608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d4b877b680c80a10067e19065facd4ce9e4819d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305972"
---
# <a name="working-with-recordsets"></a>Arbeiten mit Recordsets

**Gilt für**: Access 2013, Office 2013 

Das **Recordset** -Objekt weist integrierte Features auf, mit denen Sie die Reihenfolge der Daten im Resultset ändern, nach einem bestimmten Datensatz basierend auf eingegebenen Kriterien suchen und sogar diese Suchvorgänge mithilfe von Indizes optimieren können. Die Verfügbarkeit dieser Features hängt vom Anbieter und in manchen Fällen - wie z. B. bei der [Index](index-property-ado.md)-Eigenschaft - von der Struktur der Datenquelle selbst ab.

## <a name="arranging-data"></a>AnOrdnen von Daten

Das Angeben einer ORDER BY-Klausel im SQL-Befehl, mit dem Ergebnisse zurückgegeben werden, ist häufig die effizienteste Methode, um die Daten im **Recordset** -Objekt anzuordnen. Möglicherweise müssen Sie jedoch die Reihenfolge der Daten in einem bereits erstellten **Recordset** -Objekt ändern. Mit der **Sort** -Eigenschaft können Sie die Reihenfolge festlegen, in der Zeilen eines **Recordset** -Objekts traversiert werden. Darüber hinaus bestimmt die **Filter** -Eigenschaft, welche Zeilen beim Traversieren der Zeilen verfügbar sind.

Mit der **Sort** -Eigenschaft wird ein **String** -Wert festgelegt oder zurückgegeben, der die Feldnamen im **Recordset** -Objekt angibt, nach denen sortiert werden soll. Jeder Name wird durch ein Komma getrennt, und optional folgen ein Leerzeichen und das Schlüsselwort **ASC** (mit dem das Feld aufsteigend sortiert wird) oder **DESC** (mit dem das Feld absteigend sortiert wird). Standardmäßig wird ein Feld aufsteigend sortiert, wenn kein Schlüsselwort angegeben wird.

Der Sortiervorgang ist effizient, weil Daten nicht wirklich neu angeordnet werden, sondern lediglich in der von einem Index angegebenen Reihenfolge auf die Daten zugegriffen wird.

Für die **Sort** -Eigenschaft muss die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt werden. Für jedes Feld, das in der **Sort** -Eigenschaft angegeben ist, wird ein temporärer Index erstellt, soweit noch kein Index vorhanden ist.

Durch Festlegen der **Sort** -Eigenschaft auf eine leere Zeichenfolge werden die Zeilen auf die ursprüngliche Reihenfolge zurückgesetzt, und temporäre Indizes werden gelöscht. Vorhandene Indizes werden nicht gelöscht.

Angenommen, ein **Recordset**-Objekt enthält drei Felder mit den Namen *firstName*, *middleInitial* und *lastName*. Legen Sie die **Sort** -Eigenschaft auf die Zeichenfolge "" fest, die das **Recordset** nach dem Nachnamen in absteigender Reihenfolge und dann nach Vornamen in aufsteigender Reihenfolge sortiert. Der Mittelname wird ignoriert.

"ASC" oder "DESC" kann nicht für Felder in Sortierkriterien verwendet werden, weil diese Namen einen Konflikt mit den Schlüsselwörtern **ASC** und **DESC** verursachen. Erstellen Sie für ein Feld mit einem Namen, der einen Konflikt verursachen würde, einen Alias. Verwenden Sie dazu das **AS** -Schlüsselwort in der Abfrage, die das **Recordset** -Objekt zurückgibt.

Weitere Informationen zum Filtern von **Recordset** -Objekten finden Sie im Abschnitt "Filtern der Ergebnisse" weiter unten in diesem Thema.

## <a name="finding-a-specific-record"></a>Suchen eines bestimmten Datensatzes

ADO enthält die Methoden [Find](find-method-ado.md) und [Seek](seek-method-ado.md) für die Suche nach einem bestimmten Datensatz in einem **Recordset** -Objekt. Die **Find** -Methode wird von verschiedenen Anbietern unterstützt, ist jedoch auf ein einzelnes Suchkriterium beschränkt. Die **Seek** -Methode unterstützt die Suche mit mehreren Kriterien, wird jedoch nicht von vielen Anbietern unterstützt.

Indizes für Felder können die Leistung der **Find** -Methode und der **Sort** - und **Filter** -Eigenschaften des **Recordset** -Objekts erheblich beeinträchtigen. Sie können einen internen Index für ein **Field** -Objekt erstellen, indem Sie dessen dynamische Eigenschaft [Optimize](optimize-property-dynamic-ado.md) festlegen. Diese dynamische Eigenschaft wird der **Properties** -Auflistung des **Field** -Objekts hinzugefügt, wenn Sie die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festlegen. Beachten Sie, dass es sich dabei um einen internen Index für ADO handelt. Das heißt, Sie können nicht darauf zugreifen oder ihn für andere Zwecke verwenden. Darüber hinaus unterscheidet sich dieser Index von der **Index**-Eigenschaft des [Recordset](index-property-ado.md) -Objekts.

Mit der **Find** -Methode wird schnell nach einem Wert in einer Spalte (Feld) eines **Recordset** -Objekts gesucht. Oft kann die Verarbeitungsgeschwindigkeit der **Find** -Methode für eine Spalte optimiert werden, indem Sie die **Optimize** -Eigenschaft zum Erstellen eines Indexes verwenden.

Mit der **Find** -Methode wird die Suche auf die Inhalte eines einzigen Felds eingeschränkt. Für die **Seek** -Methode muss ein Index vorhanden sein, und außerdem gelten weitere Einschränkungen. Wenn Sie in mehreren Feldern suchen müssen, die nicht die Basis eines Indexes darstellen, oder wenn der Anbieter keine Indizes unterstützt, können Sie die Ergebnisse mithilfe der **Filter** -Eigenschaft des **Recordset** -Objekts einschränken.

### <a name="find"></a>Suchen

Mit der **Find**-Methode wird in einem **Recordset**-Objekt nach der Zeile gesucht, die ein angegebenes Kriterium erfüllt. Die Suchrichtung, die Startzeile und der Offset von der Startzeile können optional angegeben werden. Wenn das Kriterium erfüllt ist, wird der gefundene Datensatz als aktuelle Zeilenposition festgelegt. Andernfalls wird je nach Suchrichtung das Ende (oder der Anfang) des **Recordset**-Objekts als aktuelle Zeilenposition festgelegt.

Für das Kriterium kann nur ein einspaltiger Name angegeben werden. Mehrspaltige Suchvorgänge werden demnach von dieser Methode nicht unterstützt.

Der Vergleichsoperator**\>** für das Kriterium kann "" (größer als), "**\<**" (kleiner als), "=" (gleich), "\>=" (größer als oder gleich), "\<=" (kleiner als oder gleich)\<\>, "" (ungleich) oder "like" (Mustervergleich) sein.

Der Wert des Kriteriums kann eine Zeichenfolge, eine Gleitkommazahl oder ein Datum sein. Zeichenfolgenwerte werden durch einfache Anführungszeichen\#oder "" (Nummernschilder) gekennzeichnet (beispielsweise "State = ' WA '" oder "State \#=\#WA"). datumswerte sind mit\#"" (nummernzeichen) zeichen (beispielsweise "start\_datum \> \#7/22/97\#") getrennt.

Wenn "like" als Vergleichsoperator verwendet wird, kann der Zeichenfolgenwert ein Sternchen (\*) enthalten, um nach mindestens einem Vorkommnis eines beliebigen Zeichens oder einer beliebigen Teilzeichenfolge zu suchen. Beispielsweise entspricht "state like 'M\*'" Maine sowie Massachusetts. Sie können auch führende und nachstehende Sternchen verwenden, um nach einer Teilzeichenfolge zu suchen, die innerhalb der Werte enthalten ist. Beispielsweise entspricht "state like '\*as\*'" Alaska, Arkansas sowie Massachusetts.

Sternchen können nur am Ende der Kriterienzeichenfolge oder sowohl am Anfang als auch am Ende der Kriterienzeichenfolge (siehe oben) verwendet werden. Ein Sternchen kann nicht als führender Platzhalter ('\*str') oder als eingebetteter Platzhalter ('s\*r') verwendet werden. Dies würde einen Fehler verursachen.

### <a name="seek-and-index"></a>Seek-Methode und Index-Eigenschaft

Verwenden Sie die **Seek**-Methode in Verbindung mit der **Index**-Eigenschaft, falls der zugrunde liegende Anbieter Indizes für das **Recordset**-Objekt unterstützt. Mit der [Supports](supports-method-ado.md)**(adSeek)**-Methode bestimmen Sie, ob der zugrunde liegende Anbieter **Seek** unterstützt, und mit der **Supports(adIndex)**-Methode, ob der Anbieter Indizes unterstützt. (Beispielsweise werden **Seek** und **Index** vom [OLE DB-Anbieter für Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) unterstützt.)

Wenn **Seek** die gewünschte Zeile nicht findet, tritt kein Fehler auf, und die Zeile wird am Ende des **Recordset** -Objekts positioniert. Legen Sie die **Index** -Eigenschaft auf den gewünschten Index fest, bevor Sie diese Methode ausführen.

This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.

Diese Methode kann nur verwendet werden, wenn das **Recordset** -Objekt mit dem Wert [adCmdTableDirect](commandtypeenum.md) für **CommandTypeEnum** geöffnet wurde.

## <a name="filtering-the-results"></a>Filtern der Ergebnisse

Mit der **Find** -Methode wird die Suche auf die Inhalte eines einzigen Felds eingeschränkt. Für die **Seek** -Methode muss ein Index vorhanden sein, und außerdem gelten weitere Einschränkungen. Wenn Sie in mehreren Feldern suchen müssen, die nicht die Basis eines Indexes darstellen, oder wenn der Anbieter keine Indizes unterstützt, können Sie die Ergebnisse mithilfe der **Filter** -Eigenschaft des **Recordset** -Objekts einschränken.

Mit der **Filter** -Eigenschaft filtern Sie Datensätze in einem **Recordset** -Objekt. Das gefilterte **Recordset** -Objekt wird zum aktuellen Cursor. Dies bedeutet, dass Datensätze, die das Kriterium der **Filter** -Eigenschaft nicht erfüllen, erst im **Recordset** -Objekt verfügbar sind, wenn der **Filter** entfernt wird. Andere Eigenschaften, die Werte basierend auf dem aktuellen Cursor zurückgeben, sind davon betroffen, wie z. B. **AbsolutePosition**, **AbsolutePage**, **RecordCount** und **PageCount**. Durch Festlegen der **Filter** -Eigenschaft auf einen bestimmten Wert wird nämlich der aktuelle Datensatz in den ersten Datensatz verschoben, der den neuen Wert erfüllt.

The **Filter** property takes a variant argument. This value represents one of three methods for using the **Filter** property: a criteria string, a **FilterGroupEnum** constant, or an array of bookmarks. For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.

> [!NOTE]
> [!HINWEIS] Wenn Sie die Daten kennen, die Sie auswählen möchten, ist es gewöhnlich effizienter ein **Recordset** -Objekt mit einer SQL-Anweisung zu öffnen, die das Resultset wirksam filtert, anstatt die **Filter** -Eigenschaft zu verwenden.

Verwenden Sie die **adFilterNone** -Konstante, um einen Filter aus einem **Recordset** -Objekt zu entfernen. Das Festlegen der **Filter** -Eigenschaft auf eine leere Zeichenfolge ("") hat dieselbe Wirkung wie das Verwenden der **adFilterNone** -Konstante.

### <a name="filtering-with-a-criteria-string"></a>Filtern mit einer Kriterien-Zeichenfolge

Die Zeichenfolge der Kriterien besteht aus Klauseln im *Wert* des Form FieldName-Operators (beispielsweise "LastName = ' Smith '"). Sie können zusammengesetzte Klauseln erstellen, indem Sie einzelne Klauseln mit AND (beispielsweise "LastName = ' Smith ' und FirstName = ' John '") und oder (beispielsweise) verketten. Sie können zusammengesetzte Klauseln erstellen, indem Sie einzelne Klauseln mit AND (beispielsweise "LastName = ' Smith ' und FirstName = ' John '") und oder (beispielsweise "LastName = ' Smith ' oder LastName = ' Jones '") verknüpfen. Halten Sie sich für Kriterienzeichenfolgen an die folgenden Richtlinien:

- *Feldname* muss ein gültiger Feldname aus dem **Recordset**-Objekt sein. Wenn der Feldname Leerzeichen enthält, müssen Sie ihn in eckige Klammern einschließen.

- Der *Operator* muss einer der folgenden sein: \<, \>, \<=, \>=, \< \>, = oder like.

- *Value* ist der Wert, mit dem Sie die Feldwerte vergleichen (beispielsweise ' Smith ', \#8/24/95\#, 12,345 oder $50,00). Verwenden Sie einfache Anführungszeichen (') mit Zeichenfolgen\#und Zeichen () mit Datumsangaben. Für Zahlen können Sie Dezimalzeichen, Dollarzeichen und die wissenschaftliche Schreibweise verwenden. Wenn *Operator* gleich LIKE ist, können für *Wert* Platzhalterzeichen verwendet werden. Nur das Sternchen (\*) und das Prozentzeichen (%) Platzhalter sind zulässig, und Sie müssen das letzte Zeichen in der Zeichenfolge sein. *Wert* darf nicht NULL sein.
    
  > [!NOTE]
  > Um im Filter einfache Anführungszeichen (') für *Wert* einzuschließen, verwenden Sie zwei einfache Anführungszeichen zur Darstellung eines Anführungszeichens. Um beispielsweise nach *O'Malley*zu filtern, sollte die Kriterien-Zeichenfolge "col1 = ' O ' ' Tempera '" lauten. 
  > 
  > Um einfache Anführungszeichen am Anfang und am Ende des Filterwerts einzuschließen, schließen Sie die Zeichenfolge in Nummernzeichen (#) ein. Um beispielsweise nach *' 1 '* zu filtern, muss die Zeichenfolge "col1 = # ' 1 ' #" sein.

Hinsichtlich AND und OR gibt es keine Rangfolge. Die Klauseln können in Klammern zusammengefasst werden. Sie können jedoch, wie im Folgenden dargestellt, Klauseln nicht gruppieren, die mit OR verknüpft sind, und dann die Gruppe mit einer anderen Klausel mit AND verknüpfen:

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

Sie würden diesen Filter stattdessen wie folgt erstellen:

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

In einer LIKE-Klausel können Sie einen Platzhalter am Anfang und am Ende des Musters verwenden (beispielsweise LastName like '\*mit\*') oder nur am Ende des Musters (beispielsweise) oder nur am Ende des Musters (beispielsweise LastName like "Smit\*").

### <a name="filtering-with-a-constant"></a>Filtern mit einer Konstanten

Die folgenden Konstanten sind für das Filtern von **Recordset**-Objekten verfügbar.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFilterAffectedRecords</strong></p></td>
<td><p>Filter für das Anzeigen aller Datensätze, die vom letzten Aufruf von <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong> oder <strong>CancelBatch</strong> betroffen waren.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterConflictingRecords</strong></p></td>
<td><p>Filter zum Anzeigen der Datensätze, für die bei der letzten Batchaktualisierung ein Fehler erzeugt wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterFetchedRecords</strong></p></td>
<td><p>Filter zum Anzeigen der Datensätze im aktuellen Cache – das heißt, die Ergebnisse des letzten Aufrufs zum Abrufen von Datensätzen aus der Datenbank.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterNone</strong></p></td>
<td><p>Entfernt den aktuellen Filter und stellt alle Datensätze in der Ansicht wieder her.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterPendingRecords</strong></p></td>
<td><p>Filter zum Anzeigen aller Datensätze, die geändert, aber noch nicht an den Server gesendet wurden. Dies betrifft nur den Batchaktualisierungsmodus.</p></td>
</tr>
</tbody>
</table>

<br/>

Die Filterkonstanten erleichtern das Lösen einzelner Datensatzkonflikte im Batchaktualisierungsmodus, indem Sie z. B. nur die Datensätze anzeigen können, die vom letzten Aufruf der **UpdateBatch**-Methode betroffen waren. Dies ist im folgenden Beispiel veranschaulicht:

```vb 
 
'BeginDeleteGroup 
    'add some bogus records 
    With objRs1 
        For i = 0 To 8 
            .AddNew 
            .Fields("CompanyName") = "Shipper Number " & i + 1 
            .Fields("Phone") = "(425) 555-000" & (i + 1) 
            .Update 
        Next i 
         
    're-connect & update 
        .ActiveConnection = GetNewConnection 
        .UpdateBatch 
         
    'filter on newly added records 
        .Filter = adFilterAffectedRecords 
        Debug.Print "Deleting the " & .RecordCount & _ 
                    " records you just added." 
         
    'delete the newly added bogus records 
        .Delete adAffectGroup 
        .Filter = adFilterNone 
        Debug.Print .RecordCount & " records remain." 
         
        .Close 
    End With 
'EndDeleteGroup 
```

### <a name="filtering-with-bookmarks"></a>Filtern mit Lesezeichen

Finally, you can pass a variant array of bookmarks to the **Filter** property. The resulting cursor will contain only those records whose bookmark was passed in to the property. Im folgenden Codebeispiel wird ein Array von Lesezeichen aus den Datensätzen in einem **Recordset** -Objekt erstellt, das über ein "B" im Feld *ProductName* verfügt. It then passes the array to the **Filter** property and displays information about the resulting filtered **Recordset**.

```vb 
 
'BeginFilterBkmk 
    Dim vBkmkArray() As Variant 
    Dim i As Integer 
 
    'Recordset created using "SELECT * FROM Products" as command. 
    'So, we will check to see if ProductName has a capital B, and 
    'if so, add to the array. 
    i = 0 
    Do While Not objRs.EOF 
        If InStr(1, objRs("ProductName"), "B") Then 
            ReDim Preserve vBkmkArray(i) 
            vBkmkArray(i) = objRs.Bookmark 
            i = i + 1 
            Debug.Print objRs("ProductName") 
        End If 
        objRs.MoveNext 
    Loop 
     
    'Filter using the array of bookmarks. 
    objRs.Filter = vBkmkArray 
     
    objRs.MoveFirst 
    Do While Not objRs.EOF 
        Debug.Print objRs("ProductName") 
        objRs.MoveNext 
    Loop 
    'EndFilterBkmk 
```

## <a name="creating-a-clone-of-a-recordset"></a>Erstellen eines Klons eines Recordset-Objekts

Mithilfe der **Clone** -Methode erstellen Sie mehrere doppelte **Recordset** -Objekte, insbesondere wenn Sie mehr als einen aktuellen Datensatz in einem bestimmten Recordset verwalten möchten. Das Verwenden der **Clone** -Methode ist effizienter als das Erstellen und Öffnen eines neuen **Recordset** -Objekts mit der gleichen Definition wie das Original.

Der aktuelle Datensatz eines neu erstellten Klons ist ursprünglich auf den ersten Datensatz festgelegt. Der aktuelle Datensatzzeiger in einem geklonten **Recordset** -Objekt wird nicht mit dem Original synchronisiert, und umgekehrt. Sie können in jedem **Recordset** -Objekt unabhängig navigieren.

An einem **Recordset** -Objekt vorgenommene Änderungen werden unabhängig vom Cursortyp in allen Klonen des Objekts angezeigt. Nach dem Ausführen von [Requery](requery-method-ado.md) für das ursprüngliche **Recordset** -Objekt werden die Klone jedoch nicht mehr mit dem Original synchronisiert.

Durch das Schließen des ursprünglichen **Recordset** -Objekts werden die Kopien nicht geschlossen. Und durch das Schließen einer Kopie werden weder das Original noch andere Kopien geschlossen.

Ein **Recordset** -Objekt kann nur geklont werden, wenn es Leszeichen unterstützt. Textmarkenwerte sind austauschbar. Das heißt, ein Textmarkenverweis von einem **Recordset** -Objekt verweist in den Klonen auf denselben Datensatz.

