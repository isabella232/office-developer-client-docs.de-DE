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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705183"
---
# <a name="working-with-recordsets"></a>Verwenden von Recordsets

**Betrifft**: Access 2013, Office 2013 

Das **Recordset** -Objekt weist integrierte Features auf, mit denen Sie die Reihenfolge der Daten im Resultset ändern, nach einem bestimmten Datensatz basierend auf eingegebenen Kriterien suchen und sogar diese Suchvorgänge mithilfe von Indizes optimieren können. Die Verfügbarkeit dieser Features hängt vom Anbieter und in manchen Fällen - wie z. B. bei der [Index](index-property-ado.md)-Eigenschaft - von der Struktur der Datenquelle selbst ab.

## <a name="arranging-data"></a>Anordnen von Daten

Das Angeben einer ORDER BY-Klausel im SQL-Befehl, mit dem Ergebnisse zurückgegeben werden, ist häufig die effizienteste Methode, um die Daten im **Recordset** -Objekt anzuordnen. Möglicherweise müssen Sie jedoch die Reihenfolge der Daten in einem bereits erstellten **Recordset** -Objekt ändern. Mit der **Sort** -Eigenschaft können Sie die Reihenfolge festlegen, in der Zeilen eines **Recordset** -Objekts traversiert werden. Darüber hinaus bestimmt die **Filter** -Eigenschaft, welche Zeilen beim Traversieren der Zeilen verfügbar sind.

Mit der **Sort** -Eigenschaft wird ein **String** -Wert festgelegt oder zurückgegeben, der die Feldnamen im **Recordset** -Objekt angibt, nach denen sortiert werden soll. Jeder Name wird durch ein Komma getrennt, und optional folgen ein Leerzeichen und das Schlüsselwort **ASC** (mit dem das Feld aufsteigend sortiert wird) oder **DESC** (mit dem das Feld absteigend sortiert wird). Standardmäßig wird ein Feld aufsteigend sortiert, wenn kein Schlüsselwort angegeben wird.

Der Sortiervorgang ist effizient, weil Daten nicht wirklich neu angeordnet werden, sondern lediglich in der von einem Index angegebenen Reihenfolge auf die Daten zugegriffen wird.

Für die **Sort** -Eigenschaft muss die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt werden. Für jedes Feld, das in der **Sort** -Eigenschaft angegeben ist, wird ein temporärer Index erstellt, soweit noch kein Index vorhanden ist.

Durch Festlegen der **Sort** -Eigenschaft auf eine leere Zeichenfolge werden die Zeilen auf die ursprüngliche Reihenfolge zurückgesetzt, und temporäre Indizes werden gelöscht. Vorhandene Indizes werden nicht gelöscht.

Angenommen Sie, ein **Recordset-Objekt** namens *FirstName*, *LastName*und *MiddleInitial*drei Felder enthält. Legen Sie die **Sort** -Eigenschaft auf die Zeichenfolge "", welche Reihenfolge das **Recordset-Objekt** wird, nach dem Nachnamen in absteigender Reihenfolge und dann nach dem Vornamen in aufsteigender Reihenfolge. Der Mittelname wird ignoriert.

"ASC" oder "DESC" kann nicht für Felder in Sortierkriterien verwendet werden, weil diese Namen einen Konflikt mit den Schlüsselwörtern **ASC** und **DESC** verursachen. Erstellen Sie für ein Feld mit einem Namen, der einen Konflikt verursachen würde, einen Alias. Verwenden Sie dazu das **AS** -Schlüsselwort in der Abfrage, die das **Recordset** -Objekt zurückgibt.

Weitere Informationen zum Filtern von **Recordset** -Objekten finden Sie im Abschnitt "Filtern der Ergebnisse" weiter unten in diesem Thema.

## <a name="finding-a-specific-record"></a>Suchen eines bestimmten Datensatzes

ADO enthält die Methoden [Find](find-method-ado.md) und [Seek](seek-method-ado.md) für die Suche nach einem bestimmten Datensatz in einem **Recordset** -Objekt. Die **Find** -Methode wird von verschiedenen Anbietern unterstützt, ist jedoch auf ein einzelnes Suchkriterium beschränkt. Die **Seek** -Methode unterstützt die Suche mit mehreren Kriterien, wird jedoch nicht von vielen Anbietern unterstützt.

Indizes für Felder können die Leistung der **Find** -Methode und der **Sort** - und **Filter** -Eigenschaften des **Recordset** -Objekts erheblich beeinträchtigen. Sie können einen internen Index für ein **Field** -Objekt erstellen, indem Sie dessen dynamische Eigenschaft [Optimize](optimize-property-dynamic-ado.md) festlegen. Diese dynamische Eigenschaft wird der **Properties** -Auflistung des **Field** -Objekts hinzugefügt, wenn Sie die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festlegen. Beachten Sie, dass es sich dabei um einen internen Index für ADO handelt. Das heißt, Sie können nicht darauf zugreifen oder ihn für andere Zwecke verwenden. Darüber hinaus unterscheidet sich dieser Index von der **Index**-Eigenschaft des [Recordset](index-property-ado.md) -Objekts.

Mit der **Find** -Methode wird schnell nach einem Wert in einer Spalte (Feld) eines **Recordset** -Objekts gesucht. Oft kann die Verarbeitungsgeschwindigkeit der **Find** -Methode für eine Spalte optimiert werden, indem Sie die **Optimize** -Eigenschaft zum Erstellen eines Indexes verwenden.

Mit der **Find** -Methode wird die Suche auf die Inhalte eines einzigen Felds eingeschränkt. Für die **Seek** -Methode muss ein Index vorhanden sein, und außerdem gelten weitere Einschränkungen. Wenn Sie in mehreren Feldern suchen müssen, die nicht die Basis eines Indexes darstellen, oder wenn der Anbieter keine Indizes unterstützt, können Sie die Ergebnisse mithilfe der **Filter** -Eigenschaft des **Recordset** -Objekts einschränken.

### <a name="find"></a>Find-Methode

Mit der **Find** -Methode wird in einem **Recordset** -Objekt nach der Zeile gesucht, die ein angegebenes Kriterium erfüllt. Die Suchrichtung, die Startzeile und der Offset von der Startzeile können optional angegeben werden. Wenn das Kriterium erfüllt ist, wird der gefundene Datensatz als aktuelle Zeilenposition festgelegt. Andernfalls wird je nach Suchrichtung das Ende (oder der Anfang) des **Recordset** -Objekts als aktuelle Zeilenposition festgelegt.

Für das Kriterium kann nur ein einspaltiger Name angegeben werden. Mehrspaltige Suchvorgänge werden demnach von dieser Methode nicht unterstützt.

Der Vergleichsoperator für das Kriterium möglicherweise "**\>**"(größer als),"**\<**"(kleiner als), "=" (gleich),"\>=" (größer als oder gleich), "\<=" (kleiner als oder gleich), "\<\>" (nicht gleich) oder "LIKE" (Mustervergleich).

Der Wert des Kriteriums kann eine Zeichenfolge, eine Gleitkommazahl oder ein Datum sein. String-Werte werden in einfache Anführungszeichen getrennt oder "\#" (Nummernzeichen) markiert (beispielsweise "State = 'WA'" oder "Zustand = \#WA\#"). Datumswerte sind mit getrennt "\#" (Nummernzeichen) markiert (beispielsweise "starten\_Datum \> \#7/22/97\#").

Wenn "like" als Vergleichsoperator verwendet wird, kann der Zeichenfolgenwert ein Sternchen (\*) enthalten, um nach mindestens einem Vorkommnis eines beliebigen Zeichens oder einer beliebigen Teilzeichenfolge zu suchen. Beispielsweise entspricht "state like 'M\*'" Maine sowie Massachusetts. Sie können auch führende und nachstehende Sternchen verwenden, um nach einer Teilzeichenfolge zu suchen, die innerhalb der Werte enthalten ist. Beispielsweise entspricht "state like '\*as\*'" Alaska, Arkansas sowie Massachusetts.

Sternchen können nur am Ende der Kriterienzeichenfolge oder sowohl am Anfang als auch am Ende der Kriterienzeichenfolge (siehe oben) verwendet werden. Ein Sternchen kann nicht als führender Platzhalter ('\*str') oder als eingebetteter Platzhalter ('s\*r') verwendet werden. Dies würde einen Fehler verursachen.

### <a name="seek-and-index"></a>Seek-Methode und Index-Eigenschaft

Verwenden Sie die **Seek**-Methode in Verbindung mit der **Index**-Eigenschaft, falls der zugrunde liegende Anbieter Indizes für das **Recordset**-Objekt unterstützt. Mit der [Supports](supports-method-ado.md)**(adSeek)**-Methode bestimmen Sie, ob der zugrunde liegende Anbieter **Seek** unterstützt, und mit der **Supports(adIndex)**-Methode, ob der Anbieter Indizes unterstützt. (Beispielsweise werden **Seek** und **Index** vom [OLE DB-Anbieter für Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) unterstützt.)

Wenn **Seek** die gewünschte Zeile nicht findet, tritt kein Fehler auf, und die Zeile wird am Ende des **Recordset** -Objekts positioniert. Legen Sie die **Index** -Eigenschaft auf den gewünschten Index fest, bevor Sie diese Methode ausführen.

Diese Methode wird nur bei serverseitigen Cursors unterstützt. Seek wird nicht unterstützt, wenn der Wert der CursorLocation-Eigenschaft des Recordset-Objekts adUseClient lautet.

Diese Methode kann nur verwendet werden, wenn das **Recordset** -Objekt mit dem Wert [adCmdTableDirect](commandtypeenum.md) für **CommandTypeEnum** geöffnet wurde.

## <a name="filtering-the-results"></a>Filtern der Ergebnisse

Mit der **Find** -Methode wird die Suche auf die Inhalte eines einzigen Felds eingeschränkt. Für die **Seek** -Methode muss ein Index vorhanden sein, und außerdem gelten weitere Einschränkungen. Wenn Sie in mehreren Feldern suchen müssen, die nicht die Basis eines Indexes darstellen, oder wenn der Anbieter keine Indizes unterstützt, können Sie die Ergebnisse mithilfe der **Filter** -Eigenschaft des **Recordset** -Objekts einschränken.

Mit der **Filter** -Eigenschaft filtern Sie Datensätze in einem **Recordset** -Objekt. Das gefilterte **Recordset** -Objekt wird zum aktuellen Cursor. Dies bedeutet, dass Datensätze, die das Kriterium der **Filter** -Eigenschaft nicht erfüllen, erst im **Recordset** -Objekt verfügbar sind, wenn der **Filter** entfernt wird. Andere Eigenschaften, die Werte basierend auf dem aktuellen Cursor zurückgeben, sind davon betroffen, wie z. B. **AbsolutePosition**, **AbsolutePage**, **RecordCount** und **PageCount**. Durch Festlegen der **Filter** -Eigenschaft auf einen bestimmten Wert wird nämlich der aktuelle Datensatz in den ersten Datensatz verschoben, der den neuen Wert erfüllt.

Für die Filter-Eigenschaft wird ein Argument vom Typ Variant angegeben. Dieser Wert stellt eine von drei Verwendungsmethoden der Filter-Eigenschaft dar: eine Kriterienzeichenfolge, eine FilterGroupEnum-Konstante oder eine Textmarke. Weitere Informationen finden Sie unter "Filtern mit einer Kriterienzeichenfolge", "Filtern mit einer Konstante" und "Filtern mit Textmarken" weiter unten in diesem Thema.

> [!NOTE]
> [!HINWEIS] Wenn Sie die Daten kennen, die Sie auswählen möchten, ist es gewöhnlich effizienter ein **Recordset** -Objekt mit einer SQL-Anweisung zu öffnen, die das Resultset wirksam filtert, anstatt die **Filter** -Eigenschaft zu verwenden.

Verwenden Sie die **adFilterNone** -Konstante, um einen Filter aus einem **Recordset** -Objekt zu entfernen. Das Festlegen der **Filter** -Eigenschaft auf eine leere Zeichenfolge ("") hat dieselbe Wirkung wie das Verwenden der **adFilterNone** -Konstante.

### <a name="filtering-with-a-criteria-string"></a>Filtern mit einer Kriterienzeichenfolge

Die Kriterienzeichenfolge besteht aus Klauseln in der Form *Feldname Operatorwert* (z. B. "LastName = 'Smith'"). Können zusammengesetzte Klauseln durch Verketten einzelne Klauseln mit AND (z. B. "LastName = 'Smith'" und "FirstName"John"=") und oder (z. b). Können zusammengesetzte Klauseln durch Verketten einzelne Klauseln mit AND (beispielsweise "LastName = 'Smith'" und "FirstName"John"=") und oder (beispielsweise "LastName = 'Smith' oder LastName = 'Jones'"). Halten Sie sich für Kriterienzeichenfolgen an die folgenden Richtlinien:

- *FieldName* muss ein gültiger Feldname aus dem **Recordset-Objekt**sein. Wenn der Feldname Leerzeichen enthält, müssen Sie ihn in eckige Klammern einschließen.

- *Operator* muss einer der folgenden sein: \<, \>, \<= \>=, \< \>, = oder LIKE.

- *Wert* ist der Wert, mit denen Sie die Feldwerte vergleichen (z. B. "Smith", \#8/24/95\#, 12.345 oder $50,00). Verwenden Sie einfache Anführungszeichen (') mit Zeichenfolgen und Nummernzeichen (\#) mit einem Datum. Zahlen können Sie die Dezimalstellen, Dollarzeichen und die wissenschaftliche Schreibweise. Wenn *Operator* ist wie *Wert* Platzhalter verwenden können. Nur das Sternchen (\*) und Prozentzeichen (%) sind Platzhalter zulässig, und sie müssen das letzte Zeichen in der Zeichenfolge sein. *Wert* darf nicht null sein.
    
  > [!NOTE]
  > Einfache Anführungszeichen (') in *den Filterwert*aufnehmen möchten, verwenden Sie zwei einfache Anführungszeichen zur Darstellung. Beispielsweise *lautet*filtern, die Kriterienzeichenfolge sollte "SP1 = ' O'' Malley'". 
  > 
  > Einfache Anführungszeichen am Anfang und Ende des Filterwerts aufnehmen möchten, setzen Sie die Zeichenfolge in Nummernzeichen (#). Beispielsweise auf *'1'* Sie zum Filtern die Kriterienzeichenfolge sollte "SP1 = #"1"#".

Hinsichtlich AND und OR gibt es keine Rangfolge. Die Klauseln können in Klammern zusammengefasst werden. Sie können jedoch, wie im Folgenden dargestellt, Klauseln nicht gruppieren, die mit OR verknüpft sind, und dann die Gruppe mit einer anderen Klausel mit AND verknüpfen:

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

Sie würden diesen Filter stattdessen wie folgt erstellen:

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

In einer LIKE-Klausel können Sie einen Platzhalter am Anfang und Ende des Musters verwenden (beispielsweise LastName Like '\*Mit\*") oder nur am Ende des Musters (z. B.) oder nur am Ende des Musters (beispielsweise LastName Like" Smit\*").

### <a name="filtering-with-a-constant"></a>Filtern mit einer Konstante

Die folgenden Konstanten sind für das Filtern von **Recordset** -Objekten verfügbar.

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
<td><p><strong>vorliegt</strong></p></td>
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

Die Filterkonstanten erleichtern das Lösen einzelner Datensatzkonflikte im Batchaktualisierungsmodus, indem Sie z. B. nur die Datensätze anzeigen können, die vom letzten Aufruf der **UpdateBatch** -Methode betroffen waren. Dies ist im folgenden Beispiel veranschaulicht:

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

### <a name="filtering-with-bookmarks"></a>Filtern mit Textmarken

Schließlich können Sie ein Textmarkenarray vom Datentyp Variant an die Filter-Eigenschaft übergeben. Der resultierende Cursor enthält nur die Datensätze, deren Textmarken an die Eigenschaft übergeben wurde. Im folgenden Codebeispiel wird ein Textmarkenarray von den Datensätzen in einem Recordset-Objekt erstellt, die ein "B" im Feld ProductName aufweisen. Danach wird das Array an die Filter-Eigenschaft übergeben, und es werden Informationen zum resultierenden gefilterten Recordset-Objekt angezeigt.

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

## <a name="creating-a-clone-of-a-recordset"></a>Erstellen eines Klons von einem Recordset-Objekt

Mithilfe der **Clone** -Methode erstellen Sie mehrere doppelte **Recordset** -Objekte, insbesondere wenn Sie mehr als einen aktuellen Datensatz in einem bestimmten Recordset verwalten möchten. Das Verwenden der **Clone** -Methode ist effizienter als das Erstellen und Öffnen eines neuen **Recordset** -Objekts mit der gleichen Definition wie das Original.

Der aktuelle Datensatz eines neu erstellten Klons ist ursprünglich auf den ersten Datensatz festgelegt. Der aktuelle Datensatzzeiger in einem geklonten **Recordset** -Objekt wird nicht mit dem Original synchronisiert, und umgekehrt. Sie können in jedem **Recordset** -Objekt unabhängig navigieren.

An einem **Recordset** -Objekt vorgenommene Änderungen werden unabhängig vom Cursortyp in allen Klonen des Objekts angezeigt. Nach dem Ausführen von [Requery](requery-method-ado.md) für das ursprüngliche **Recordset** -Objekt werden die Klone jedoch nicht mehr mit dem Original synchronisiert.

Durch das Schließen des ursprünglichen **Recordset** -Objekts werden die Kopien nicht geschlossen. Und durch das Schließen einer Kopie werden weder das Original noch andere Kopien geschlossen.

Ein **Recordset** -Objekt kann nur geklont werden, wenn es Leszeichen unterstützt. Textmarkenwerte sind austauschbar. Das heißt, ein Textmarkenverweis von einem **Recordset** -Objekt verweist in den Klonen auf denselben Datensatz.

