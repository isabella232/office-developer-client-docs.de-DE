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
# <a name="working-with-recordsets"></a><span data-ttu-id="810ab-102">Arbeiten mit Recordsets</span><span class="sxs-lookup"><span data-stu-id="810ab-102">Working with Recordsets</span></span>

<span data-ttu-id="810ab-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="810ab-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="810ab-p101">Das **Recordset** -Objekt weist integrierte Features auf, mit denen Sie die Reihenfolge der Daten im Resultset ändern, nach einem bestimmten Datensatz basierend auf eingegebenen Kriterien suchen und sogar diese Suchvorgänge mithilfe von Indizes optimieren können. Die Verfügbarkeit dieser Features hängt vom Anbieter und in manchen Fällen - wie z. B. bei der [Index](index-property-ado.md)-Eigenschaft - von der Struktur der Datenquelle selbst ab.</span><span class="sxs-lookup"><span data-stu-id="810ab-p101">The **Recordset** object has built-in features that make it possible for you to rearrange the order of the data in the result set, to search for a specific record based on criteria that you supply, and even to optimize those search operations using indexes. Whether these features are available for use depends on the provider and in some cases — such as that of the [Index](index-property-ado.md) property — the structure of the data source itself.</span></span>

## <a name="arranging-data"></a><span data-ttu-id="810ab-106">AnOrdnen von Daten</span><span class="sxs-lookup"><span data-stu-id="810ab-106">Arranging data</span></span>

<span data-ttu-id="810ab-p102">Das Angeben einer ORDER BY-Klausel im SQL-Befehl, mit dem Ergebnisse zurückgegeben werden, ist häufig die effizienteste Methode, um die Daten im **Recordset** -Objekt anzuordnen. Möglicherweise müssen Sie jedoch die Reihenfolge der Daten in einem bereits erstellten **Recordset** -Objekt ändern. Mit der **Sort** -Eigenschaft können Sie die Reihenfolge festlegen, in der Zeilen eines **Recordset** -Objekts traversiert werden. Darüber hinaus bestimmt die **Filter** -Eigenschaft, welche Zeilen beim Traversieren der Zeilen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="810ab-p102">Often, the most efficient way to order the data in your **Recordset** is by specifying an ORDER BY clause in the SQL command used to return results to it. However, you might need to change the order of the data in a **Recordset** that has already been created. You can use the **Sort** property to establish the order in which rows of a **Recordset** are traversed. Furthermore, the **Filter** property determines which rows are accessible when traversing rows.</span></span>

<span data-ttu-id="810ab-p103">Mit der **Sort** -Eigenschaft wird ein **String** -Wert festgelegt oder zurückgegeben, der die Feldnamen im **Recordset** -Objekt angibt, nach denen sortiert werden soll. Jeder Name wird durch ein Komma getrennt, und optional folgen ein Leerzeichen und das Schlüsselwort **ASC** (mit dem das Feld aufsteigend sortiert wird) oder **DESC** (mit dem das Feld absteigend sortiert wird). Standardmäßig wird ein Feld aufsteigend sortiert, wenn kein Schlüsselwort angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="810ab-p103">The **Sort** property sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort. Each name is separated by a comma and is optionally followed by a space and the keyword **ASC** (which sorts the field in ascending order) or **DESC** (which sorts the field in descending order). By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

<span data-ttu-id="810ab-114">Der Sortiervorgang ist effizient, weil Daten nicht wirklich neu angeordnet werden, sondern lediglich in der von einem Index angegebenen Reihenfolge auf die Daten zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="810ab-114">The sort operation is efficient because data is not physically rearranged but is simply accessed in the order specified by an index.</span></span>

<span data-ttu-id="810ab-p104">Für die **Sort** -Eigenschaft muss die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt werden. Für jedes Feld, das in der **Sort** -Eigenschaft angegeben ist, wird ein temporärer Index erstellt, soweit noch kein Index vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="810ab-p104">The **Sort** property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**. A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="810ab-p105">Durch Festlegen der **Sort** -Eigenschaft auf eine leere Zeichenfolge werden die Zeilen auf die ursprüngliche Reihenfolge zurückgesetzt, und temporäre Indizes werden gelöscht. Vorhandene Indizes werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="810ab-p105">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes. Existing indexes will not be deleted.</span></span>

<span data-ttu-id="810ab-119">Angenommen, ein **Recordset**-Objekt enthält drei Felder mit den Namen *firstName*, *middleInitial* und *lastName*.</span><span class="sxs-lookup"><span data-stu-id="810ab-119">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="810ab-120">Legen Sie die **Sort** -Eigenschaft auf die Zeichenfolge "" fest, die das **Recordset** nach dem Nachnamen in absteigender Reihenfolge und dann nach Vornamen in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="810ab-120">Set the **Sort** property to the string "", which will order the **Recordset** by last name in descending order and then by first name in ascending order.</span></span> <span data-ttu-id="810ab-121">Der Mittelname wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="810ab-121">The middle initial is ignored.</span></span>

<span data-ttu-id="810ab-p107">"ASC" oder "DESC" kann nicht für Felder in Sortierkriterien verwendet werden, weil diese Namen einen Konflikt mit den Schlüsselwörtern **ASC** und **DESC** verursachen. Erstellen Sie für ein Feld mit einem Namen, der einen Konflikt verursachen würde, einen Alias. Verwenden Sie dazu das **AS** -Schlüsselwort in der Abfrage, die das **Recordset** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="810ab-p107">No field referenced in a sort criteria string can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**. Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

<span data-ttu-id="810ab-124">Weitere Informationen zum Filtern von **Recordset** -Objekten finden Sie im Abschnitt "Filtern der Ergebnisse" weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="810ab-124">For more details about **Recordset** filtering, see Filtering the Results later in this topic.</span></span>

## <a name="finding-a-specific-record"></a><span data-ttu-id="810ab-125">Suchen eines bestimmten Datensatzes</span><span class="sxs-lookup"><span data-stu-id="810ab-125">Finding a specific record</span></span>

<span data-ttu-id="810ab-p108">ADO enthält die Methoden [Find](find-method-ado.md) und [Seek](seek-method-ado.md) für die Suche nach einem bestimmten Datensatz in einem **Recordset** -Objekt. Die **Find** -Methode wird von verschiedenen Anbietern unterstützt, ist jedoch auf ein einzelnes Suchkriterium beschränkt. Die **Seek** -Methode unterstützt die Suche mit mehreren Kriterien, wird jedoch nicht von vielen Anbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="810ab-p108">ADO provides the [Find](find-method-ado.md) and [Seek](seek-method-ado.md) methods for locating a particular record in a **Recordset**. The **Find** method is supported by a variety of providers but is limited to a single search criterion. The **Seek** method supports searching on multiple criteria, but is not supported by many providers.</span></span>

<span data-ttu-id="810ab-p109">Indizes für Felder können die Leistung der **Find** -Methode und der **Sort** - und **Filter** -Eigenschaften des **Recordset** -Objekts erheblich beeinträchtigen. Sie können einen internen Index für ein **Field** -Objekt erstellen, indem Sie dessen dynamische Eigenschaft [Optimize](optimize-property-dynamic-ado.md) festlegen. Diese dynamische Eigenschaft wird der **Properties** -Auflistung des **Field** -Objekts hinzugefügt, wenn Sie die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festlegen. Beachten Sie, dass es sich dabei um einen internen Index für ADO handelt. Das heißt, Sie können nicht darauf zugreifen oder ihn für andere Zwecke verwenden. Darüber hinaus unterscheidet sich dieser Index von der **Index**-Eigenschaft des [Recordset](index-property-ado.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="810ab-p109">Indexes on fields can greatly enhance the performance of the **Recordset** object's **Find** method and **Sort** and **Filter** properties. You can create an internal index for a **Field** object by setting its dynamic [Optimize](optimize-property-dynamic-ado.md) property. This dynamic property is added to the **Field** object's **Properties** collection when you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**. Remember that this index is internal to ADO — you cannot gain access to it or use it for any other purpose. Also, this index is distinct from the **Recordset** object's [Index](index-property-ado.md) property.</span></span>

<span data-ttu-id="810ab-p110">Mit der **Find** -Methode wird schnell nach einem Wert in einer Spalte (Feld) eines **Recordset** -Objekts gesucht. Oft kann die Verarbeitungsgeschwindigkeit der **Find** -Methode für eine Spalte optimiert werden, indem Sie die **Optimize** -Eigenschaft zum Erstellen eines Indexes verwenden.</span><span class="sxs-lookup"><span data-stu-id="810ab-p110">The **Find** method quickly locates a value within a column (field) of a **Recordset**. You can often improve the speed of the **Find** method's operation on a column by using the **Optimize** property to create an index on it.</span></span>

<span data-ttu-id="810ab-p111">Mit der **Find** -Methode wird die Suche auf die Inhalte eines einzigen Felds eingeschränkt. Für die **Seek** -Methode muss ein Index vorhanden sein, und außerdem gelten weitere Einschränkungen. Wenn Sie in mehreren Feldern suchen müssen, die nicht die Basis eines Indexes darstellen, oder wenn der Anbieter keine Indizes unterstützt, können Sie die Ergebnisse mithilfe der **Filter** -Eigenschaft des **Recordset** -Objekts einschränken.</span><span class="sxs-lookup"><span data-stu-id="810ab-p111">The **Find** method limits your search to the contents of one field. The **Seek** method requires that you have an index and has other limitations as well. If you need to search on multiple fields that aren't the basis of an index, or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

### <a name="find"></a><span data-ttu-id="810ab-139">Suchen</span><span class="sxs-lookup"><span data-stu-id="810ab-139">Find</span></span>

<span data-ttu-id="810ab-p112">Mit der **Find**-Methode wird in einem **Recordset**-Objekt nach der Zeile gesucht, die ein angegebenes Kriterium erfüllt. Die Suchrichtung, die Startzeile und der Offset von der Startzeile können optional angegeben werden. Wenn das Kriterium erfüllt ist, wird der gefundene Datensatz als aktuelle Zeilenposition festgelegt. Andernfalls wird je nach Suchrichtung das Ende (oder der Anfang) des **Recordset**-Objekts als aktuelle Zeilenposition festgelegt.</span><span class="sxs-lookup"><span data-stu-id="810ab-p112">The **Find** method searches a **Recordset** for the row that satisfies a specified criterion. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criterion is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**, depending on search direction.</span></span>

<span data-ttu-id="810ab-p113">Für das Kriterium kann nur ein einspaltiger Name angegeben werden. Mehrspaltige Suchvorgänge werden demnach von dieser Methode nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="810ab-p113">Only a single-column name may be specified for the criterion. In other words, this method does not support multi-column searches.</span></span>

<span data-ttu-id="810ab-145">Der Vergleichsoperator**\>** für das Kriterium kann "" (größer als), "**\<**" (kleiner als), "=" (gleich), "\>=" (größer als oder gleich), "\<=" (kleiner als oder gleich)\<\>, "" (ungleich) oder "like" (Mustervergleich) sein.</span><span class="sxs-lookup"><span data-stu-id="810ab-145">The comparison operator for the criterion may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "LIKE" (pattern matching).</span></span>

<span data-ttu-id="810ab-146">Der Wert des Kriteriums kann eine Zeichenfolge, eine Gleitkommazahl oder ein Datum sein.</span><span class="sxs-lookup"><span data-stu-id="810ab-146">The criterion value may be a string, floating-point number, or date.</span></span> <span data-ttu-id="810ab-147">Zeichenfolgenwerte werden durch einfache Anführungszeichen\#oder "" (Nummernschilder) gekennzeichnet (beispielsweise "State = ' WA '" oder "State \#=\#WA").</span><span class="sxs-lookup"><span data-stu-id="810ab-147">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="810ab-148">datumswerte sind mit\#"" (nummernzeichen) zeichen (beispielsweise "start\_datum \> \#7/22/97\#") getrennt.</span><span class="sxs-lookup"><span data-stu-id="810ab-148">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#").</span></span>

<span data-ttu-id="810ab-p115">Wenn "like" als Vergleichsoperator verwendet wird, kann der Zeichenfolgenwert ein Sternchen (\*) enthalten, um nach mindestens einem Vorkommnis eines beliebigen Zeichens oder einer beliebigen Teilzeichenfolge zu suchen. Beispielsweise entspricht "state like 'M\*'" Maine sowie Massachusetts. Sie können auch führende und nachstehende Sternchen verwenden, um nach einer Teilzeichenfolge zu suchen, die innerhalb der Werte enthalten ist. Beispielsweise entspricht "state like '\*as\*'" Alaska, Arkansas sowie Massachusetts.</span><span class="sxs-lookup"><span data-stu-id="810ab-p115">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="810ab-p116">Sternchen können nur am Ende der Kriterienzeichenfolge oder sowohl am Anfang als auch am Ende der Kriterienzeichenfolge (siehe oben) verwendet werden. Ein Sternchen kann nicht als führender Platzhalter ('\*str') oder als eingebetteter Platzhalter ('s\*r') verwendet werden. Dies würde einen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="810ab-p116">Asterisks can be used only at the end of a criteria string or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str') or embedded wildcard ('s\*r'). This will cause an error.</span></span>

### <a name="seek-and-index"></a><span data-ttu-id="810ab-156">Seek-Methode und Index-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="810ab-156">Seek and Index</span></span>

<span data-ttu-id="810ab-p117">Verwenden Sie die **Seek**-Methode in Verbindung mit der **Index**-Eigenschaft, falls der zugrunde liegende Anbieter Indizes für das **Recordset**-Objekt unterstützt. Mit der [Supports](supports-method-ado.md)**(adSeek)**-Methode bestimmen Sie, ob der zugrunde liegende Anbieter **Seek** unterstützt, und mit der **Supports(adIndex)**-Methode, ob der Anbieter Indizes unterstützt. (Beispielsweise werden **Seek** und **Index** vom [OLE DB-Anbieter für Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="810ab-p117">Use the **Seek** method in conjunction with the **Index** property if the underlying provider supports indexes on the **Recordset** object. Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes. (For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="810ab-p118">Wenn **Seek** die gewünschte Zeile nicht findet, tritt kein Fehler auf, und die Zeile wird am Ende des **Recordset** -Objekts positioniert. Legen Sie die **Index** -Eigenschaft auf den gewünschten Index fest, bevor Sie diese Methode ausführen.</span><span class="sxs-lookup"><span data-stu-id="810ab-p118">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="810ab-p119">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="810ab-p119">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="810ab-164">Diese Methode kann nur verwendet werden, wenn das **Recordset** -Objekt mit dem Wert [adCmdTableDirect](commandtypeenum.md) für **CommandTypeEnum** geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="810ab-164">This method can be used only when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

## <a name="filtering-the-results"></a><span data-ttu-id="810ab-165">Filtern der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="810ab-165">Filtering the results</span></span>

<span data-ttu-id="810ab-p120">Mit der **Find** -Methode wird die Suche auf die Inhalte eines einzigen Felds eingeschränkt. Für die **Seek** -Methode muss ein Index vorhanden sein, und außerdem gelten weitere Einschränkungen. Wenn Sie in mehreren Feldern suchen müssen, die nicht die Basis eines Indexes darstellen, oder wenn der Anbieter keine Indizes unterstützt, können Sie die Ergebnisse mithilfe der **Filter** -Eigenschaft des **Recordset** -Objekts einschränken.</span><span class="sxs-lookup"><span data-stu-id="810ab-p120">The **Find** method limits your search to the contents of one field. The **Seek** method requires that you have an index and has other limitations as well. If you need to search on multiple fields that are not the basis of an index or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

<span data-ttu-id="810ab-p121">Mit der **Filter** -Eigenschaft filtern Sie Datensätze in einem **Recordset** -Objekt. Das gefilterte **Recordset** -Objekt wird zum aktuellen Cursor. Dies bedeutet, dass Datensätze, die das Kriterium der **Filter** -Eigenschaft nicht erfüllen, erst im **Recordset** -Objekt verfügbar sind, wenn der **Filter** entfernt wird. Andere Eigenschaften, die Werte basierend auf dem aktuellen Cursor zurückgeben, sind davon betroffen, wie z. B. **AbsolutePosition**, **AbsolutePage**, **RecordCount** und **PageCount**. Durch Festlegen der **Filter** -Eigenschaft auf einen bestimmten Wert wird nämlich der aktuelle Datensatz in den ersten Datensatz verschoben, der den neuen Wert erfüllt.</span><span class="sxs-lookup"><span data-stu-id="810ab-p121">Use the **Filter** property to selectively screen out records in a **Recordset** object. The filtered **Recordset** becomes the current cursor, which means that records that do not satisfy the **Filter** criteria are not available in the **Recordset** until the **Filter** is removed. Other properties that return values based on the current cursor are affected, such as **AbsolutePosition**, **AbsolutePage**, **RecordCount**, and **PageCount**. This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="810ab-p122">The **Filter** property takes a variant argument. This value represents one of three methods for using the **Filter** property: a criteria string, a **FilterGroupEnum** constant, or an array of bookmarks. For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</span><span class="sxs-lookup"><span data-stu-id="810ab-p122">The **Filter** property takes a variant argument. This value represents one of three methods for using the **Filter** property: a criteria string, a **FilterGroupEnum** constant, or an array of bookmarks. For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="810ab-176">[!HINWEIS] Wenn Sie die Daten kennen, die Sie auswählen möchten, ist es gewöhnlich effizienter ein **Recordset** -Objekt mit einer SQL-Anweisung zu öffnen, die das Resultset wirksam filtert, anstatt die **Filter** -Eigenschaft zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="810ab-176">When you know the data you want to select, it is usually more efficient to open a **Recordset** with a SQL statement that effectively filters the result set, rather than relying on the **Filter** property.</span></span>

<span data-ttu-id="810ab-p123">Verwenden Sie die **adFilterNone** -Konstante, um einen Filter aus einem **Recordset** -Objekt zu entfernen. Das Festlegen der **Filter** -Eigenschaft auf eine leere Zeichenfolge ("") hat dieselbe Wirkung wie das Verwenden der **adFilterNone** -Konstante.</span><span class="sxs-lookup"><span data-stu-id="810ab-p123">To remove a filter from a **Recordset**, use the **adFilterNone** constant. Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

### <a name="filtering-with-a-criteria-string"></a><span data-ttu-id="810ab-179">Filtern mit einer Kriterien-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="810ab-179">Filtering with a criteria string</span></span>

<span data-ttu-id="810ab-180">Die Zeichenfolge der Kriterien besteht aus Klauseln im *Wert* des Form FieldName-Operators (beispielsweise "LastName = ' Smith '").</span><span class="sxs-lookup"><span data-stu-id="810ab-180">The criteria string is made up of clauses in the form *FieldName Operator Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="810ab-181">Sie können zusammengesetzte Klauseln erstellen, indem Sie einzelne Klauseln mit AND (beispielsweise "LastName = ' Smith ' und FirstName = ' John '") und oder (beispielsweise) verketten.</span><span class="sxs-lookup"><span data-stu-id="810ab-181">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, ).</span></span> <span data-ttu-id="810ab-182">Sie können zusammengesetzte Klauseln erstellen, indem Sie einzelne Klauseln mit AND (beispielsweise "LastName = ' Smith ' und FirstName = ' John '") und oder (beispielsweise "LastName = ' Smith ' oder LastName = ' Jones '") verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="810ab-182">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="810ab-183">Halten Sie sich für Kriterienzeichenfolgen an die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="810ab-183">Use the following guidelines for criteria strings:</span></span>

- <span data-ttu-id="810ab-p125">*Feldname* muss ein gültiger Feldname aus dem **Recordset**-Objekt sein. Wenn der Feldname Leerzeichen enthält, müssen Sie ihn in eckige Klammern einschließen.</span><span class="sxs-lookup"><span data-stu-id="810ab-p125">*FieldName* must be a valid field name from the **Recordset**. If the field name contains spaces, you must enclose the name in square brackets.</span></span>

- <span data-ttu-id="810ab-186">Der *Operator* muss einer der folgenden sein: \<, \>, \<=, \>=, \< \>, = oder like.</span><span class="sxs-lookup"><span data-stu-id="810ab-186">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or LIKE.</span></span>

- <span data-ttu-id="810ab-187">*Value* ist der Wert, mit dem Sie die Feldwerte vergleichen (beispielsweise ' Smith ', \#8/24/95\#, 12,345 oder $50,00).</span><span class="sxs-lookup"><span data-stu-id="810ab-187">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="810ab-188">Verwenden Sie einfache Anführungszeichen (') mit Zeichenfolgen\#und Zeichen () mit Datumsangaben.</span><span class="sxs-lookup"><span data-stu-id="810ab-188">Use single quotation marks (') with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="810ab-189">Für Zahlen können Sie Dezimalzeichen, Dollarzeichen und die wissenschaftliche Schreibweise verwenden.</span><span class="sxs-lookup"><span data-stu-id="810ab-189">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="810ab-190">Wenn *Operator* gleich LIKE ist, können für *Wert* Platzhalterzeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="810ab-190">If *Operator* is LIKE, *Value* can use wildcards.</span></span> <span data-ttu-id="810ab-191">Nur das Sternchen (\*) und das Prozentzeichen (%) Platzhalter sind zulässig, und Sie müssen das letzte Zeichen in der Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="810ab-191">Only the asterisk (\*) and percent sign (%) wildcards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="810ab-192">*Wert* darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="810ab-192">*Value* cannot be null.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="810ab-193">Um im Filter einfache Anführungszeichen (') für *Wert* einzuschließen, verwenden Sie zwei einfache Anführungszeichen zur Darstellung eines Anführungszeichens.</span><span class="sxs-lookup"><span data-stu-id="810ab-193">To include single quotation marks (') in the filter *Value*, use two single quotation marks to represent one.</span></span> <span data-ttu-id="810ab-194">Um beispielsweise nach *O'Malley*zu filtern, sollte die Kriterien-Zeichenfolge "col1 = ' O ' ' Tempera '" lauten.</span><span class="sxs-lookup"><span data-stu-id="810ab-194">For example, to filter on *O'Malley*, the criteria string should be "col1 = 'O''Malley'".</span></span> 
  > 
  > <span data-ttu-id="810ab-195">Um einfache Anführungszeichen am Anfang und am Ende des Filterwerts einzuschließen, schließen Sie die Zeichenfolge in Nummernzeichen (#) ein.</span><span class="sxs-lookup"><span data-stu-id="810ab-195">To include single quotation marks at both the beginning and the end of the filter value, enclose the string in pound signs (#).</span></span> <span data-ttu-id="810ab-196">Um beispielsweise nach *' 1 '* zu filtern, muss die Zeichenfolge "col1 = # ' 1 ' #" sein.</span><span class="sxs-lookup"><span data-stu-id="810ab-196">For example, to filter on *'1'*, the criteria string should be "col1 = #'1'#".</span></span>

<span data-ttu-id="810ab-p129">Hinsichtlich AND und OR gibt es keine Rangfolge. Die Klauseln können in Klammern zusammengefasst werden. Sie können jedoch, wie im Folgenden dargestellt, Klauseln nicht gruppieren, die mit OR verknüpft sind, und dann die Gruppe mit einer anderen Klausel mit AND verknüpfen:</span><span class="sxs-lookup"><span data-stu-id="810ab-p129">There is no precedence between AND and OR. Clauses can be grouped within parentheses. However, you cannot group clauses joined by an OR and then join the group to another clause with an AND, like this:</span></span>

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

<span data-ttu-id="810ab-200">Sie würden diesen Filter stattdessen wie folgt erstellen:</span><span class="sxs-lookup"><span data-stu-id="810ab-200">Instead, you would construct this filter as:</span></span>

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

<span data-ttu-id="810ab-201">In einer LIKE-Klausel können Sie einen Platzhalter am Anfang und am Ende des Musters verwenden (beispielsweise LastName like '\*mit\*') oder nur am Ende des Musters (beispielsweise) oder nur am Ende des Musters (beispielsweise LastName like "Smit\*").</span><span class="sxs-lookup"><span data-stu-id="810ab-201">In a LIKE clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*') or only at the end of the pattern (for example, ) or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

### <a name="filtering-with-a-constant"></a><span data-ttu-id="810ab-202">Filtern mit einer Konstanten</span><span class="sxs-lookup"><span data-stu-id="810ab-202">Filtering with a constant</span></span>

<span data-ttu-id="810ab-203">Die folgenden Konstanten sind für das Filtern von **Recordset**-Objekten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="810ab-203">The following constants are available for filtering **Recordsets**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="810ab-204">Konstante</span><span class="sxs-lookup"><span data-stu-id="810ab-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="810ab-205">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="810ab-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="810ab-206"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="810ab-206"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="810ab-207">Filter für das Anzeigen aller Datensätze, die vom letzten Aufruf von <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong> oder <strong>CancelBatch</strong> betroffen waren.</span><span class="sxs-lookup"><span data-stu-id="810ab-207">Filters for viewing only records effected by the last <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong>, or <strong>CancelBatch</strong> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="810ab-208"><strong>adFilterConflictingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="810ab-208"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="810ab-209">Filter zum Anzeigen der Datensätze, für die bei der letzten Batchaktualisierung ein Fehler erzeugt wurde.</span><span class="sxs-lookup"><span data-stu-id="810ab-209">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="810ab-210"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="810ab-210"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="810ab-211">Filter zum Anzeigen der Datensätze im aktuellen Cache – das heißt, die Ergebnisse des letzten Aufrufs zum Abrufen von Datensätzen aus der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="810ab-211">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="810ab-212"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="810ab-212"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="810ab-213">Entfernt den aktuellen Filter und stellt alle Datensätze in der Ansicht wieder her.</span><span class="sxs-lookup"><span data-stu-id="810ab-213">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="810ab-214"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="810ab-214"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="810ab-215">Filter zum Anzeigen aller Datensätze, die geändert, aber noch nicht an den Server gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="810ab-215">Filters for viewing only records that have changed but have not yet been sent to the server.</span></span> <span data-ttu-id="810ab-216">Dies betrifft nur den Batchaktualisierungsmodus.</span><span class="sxs-lookup"><span data-stu-id="810ab-216">Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="810ab-217">Die Filterkonstanten erleichtern das Lösen einzelner Datensatzkonflikte im Batchaktualisierungsmodus, indem Sie z. B. nur die Datensätze anzeigen können, die vom letzten Aufruf der **UpdateBatch**-Methode betroffen waren. Dies ist im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="810ab-217">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were effected during the last **UpdateBatch** method call, as shown in the following example:</span></span>

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

### <a name="filtering-with-bookmarks"></a><span data-ttu-id="810ab-218">Filtern mit Lesezeichen</span><span class="sxs-lookup"><span data-stu-id="810ab-218">Filtering with bookmarks</span></span>

<span data-ttu-id="810ab-219">Finally, you can pass a variant array of bookmarks to the **Filter** property.</span><span class="sxs-lookup"><span data-stu-id="810ab-219">Finally, you can pass a variant array of bookmarks to the **Filter** property.</span></span> <span data-ttu-id="810ab-220">The resulting cursor will contain only those records whose bookmark was passed in to the property.</span><span class="sxs-lookup"><span data-stu-id="810ab-220">The resulting cursor will contain only those records whose bookmark was passed in to the property.</span></span> <span data-ttu-id="810ab-221">Im folgenden Codebeispiel wird ein Array von Lesezeichen aus den Datensätzen in einem **Recordset** -Objekt erstellt, das über ein "B" im Feld *ProductName* verfügt.</span><span class="sxs-lookup"><span data-stu-id="810ab-221">The following code example creates an array of bookmarks from the records in a **Recordset** which have a "B" in the *ProductName* field.</span></span> <span data-ttu-id="810ab-222">It then passes the array to the **Filter** property and displays information about the resulting filtered **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="810ab-222">It then passes the array to the **Filter** property and displays information about the resulting filtered **Recordset**.</span></span>

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

## <a name="creating-a-clone-of-a-recordset"></a><span data-ttu-id="810ab-223">Erstellen eines Klons eines Recordset-Objekts</span><span class="sxs-lookup"><span data-stu-id="810ab-223">Creating a clone of a Recordset</span></span>

<span data-ttu-id="810ab-p132">Mithilfe der **Clone** -Methode erstellen Sie mehrere doppelte **Recordset** -Objekte, insbesondere wenn Sie mehr als einen aktuellen Datensatz in einem bestimmten Recordset verwalten möchten. Das Verwenden der **Clone** -Methode ist effizienter als das Erstellen und Öffnen eines neuen **Recordset** -Objekts mit der gleichen Definition wie das Original.</span><span class="sxs-lookup"><span data-stu-id="810ab-p132">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="810ab-p133">Der aktuelle Datensatz eines neu erstellten Klons ist ursprünglich auf den ersten Datensatz festgelegt. Der aktuelle Datensatzzeiger in einem geklonten **Recordset** -Objekt wird nicht mit dem Original synchronisiert, und umgekehrt. Sie können in jedem **Recordset** -Objekt unabhängig navigieren.</span><span class="sxs-lookup"><span data-stu-id="810ab-p133">The current record of a newly created clone is originally set to the first record. The current record pointer in a cloned **Recordset** is not synchronized with the original or vice versa. You can navigate independently in each **Recordset**.</span></span>

<span data-ttu-id="810ab-p134">An einem **Recordset** -Objekt vorgenommene Änderungen werden unabhängig vom Cursortyp in allen Klonen des Objekts angezeigt. Nach dem Ausführen von [Requery](requery-method-ado.md) für das ursprüngliche **Recordset** -Objekt werden die Klone jedoch nicht mehr mit dem Original synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="810ab-p134">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="810ab-231">Durch das Schließen des ursprünglichen **Recordset** -Objekts werden die Kopien nicht geschlossen. Und durch das Schließen einer Kopie werden weder das Original noch andere Kopien geschlossen.</span><span class="sxs-lookup"><span data-stu-id="810ab-231">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="810ab-p135">Ein **Recordset** -Objekt kann nur geklont werden, wenn es Leszeichen unterstützt. Textmarkenwerte sind austauschbar. Das heißt, ein Textmarkenverweis von einem **Recordset** -Objekt verweist in den Klonen auf denselben Datensatz.</span><span class="sxs-lookup"><span data-stu-id="810ab-p135">You can clone a **Recordset** object only if it supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

