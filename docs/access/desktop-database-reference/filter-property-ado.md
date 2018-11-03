---
title: Filter-Eigenschaft (ADO)
TOCTitle: Filter property (ADO)
ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15)
ms:contentKeyID: 48545053
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d067d26120e694975c662c3d018443e325e75119
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937134"
---
# <a name="filter-property-ado"></a><span data-ttu-id="04c31-102">Filter-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="04c31-102">Filter property (ADO)</span></span>


<span data-ttu-id="04c31-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04c31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04c31-104">Gibt einen Filter für Daten in einem [Recordset](recordset-object-ado.md) an.</span><span class="sxs-lookup"><span data-stu-id="04c31-104">Indicates a filter for data in a [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="04c31-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="04c31-105">Settings and return values</span></span>

<span data-ttu-id="04c31-106">Legt einen **Variant** -Wert fest oder gibt ihn zurück, der Folgendes enthalten kann:</span><span class="sxs-lookup"><span data-stu-id="04c31-106">Sets or returns a **Variant** value, which can contain one of the following:</span></span>

  - <span data-ttu-id="04c31-107">**Kriterienzeichenfolge** - eine Zeichenfolge aus einer oder mehreren Klauseln, die mit **AND** - oder **OR** -Operatoren verkettet sind.</span><span class="sxs-lookup"><span data-stu-id="04c31-107">**Criteria string** — a string made up of one or more individual clauses concatenated with **AND** or **OR** operators.</span></span>

  - <span data-ttu-id="04c31-108">**Textmarkenarray** - ein Array mit eindeutigen Textmarkenwerten, die auf Datensätze im **Recordset** -Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="04c31-108">**Array of bookmarks** — an array of unique bookmark values that point to records in the **Recordset** object.</span></span>

  - <span data-ttu-id="04c31-109">Ein [FilterGroupEnum](filtergroupenum.md)-Wert.</span><span class="sxs-lookup"><span data-stu-id="04c31-109">A [FilterGroupEnum](filtergroupenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04c31-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04c31-110">Remarks</span></span>

<span data-ttu-id="04c31-p101">Verwenden Sie die **Filter** -Eigenschaft, um Datensätze in einem **Recordset** -Objekt gezielt herauszufiltern. Das gefilterte **Recordset** -Objekt wird zum aktuellen Cursor. Andere Eigenschaften, deren Rückgabewerte auf dem aktuellen Cursor basieren, werden dadurch beeinflusst, wie z. B. [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md) und [PageCount](pagecount-property-ado.md). Das liegt daran, dass der aktuelle Datensatz durch das Festlegen der **Filter** -Eigenschaft auf einen bestimmten Wert zum ersten Datensatz wechselt, der dem neuen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="04c31-p101">Use the **Filter** property to selectively screen out records in a **Recordset** object. The filtered **Recordset** becomes the current cursor. Other properties that return values based on the current cursor are affected, such as [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md), and [PageCount](pagecount-property-ado.md). This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="04c31-115">Die Kriterienzeichenfolge besteht aus Klauseln in der Form *FieldName-Operator-Wert* (beispielsweise "LastName = 'Smith'").</span><span class="sxs-lookup"><span data-stu-id="04c31-115">The criteria string is made up of clauses in the form *FieldName-Operator-Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="04c31-116">Sie können zusammengesetzte Klauseln erstellen, indem Sie einzelne Klauseln mit **AND** verketten (beispielsweise "LastName = 'Smith'" und "FirstName ="John"") oder **OR** (z. B. ").</span><span class="sxs-lookup"><span data-stu-id="04c31-116">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, ").</span></span> <span data-ttu-id="04c31-117">Sie können zusammengesetzte Klauseln erstellen, indem Sie einzelne Klauseln mit **AND** verketten (beispielsweise "LastName = 'Smith'" und "FirstName ="John"") oder **OR** (beispielsweise "LastName = 'Smith' oder LastName = 'Jones'").</span><span class="sxs-lookup"><span data-stu-id="04c31-117">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="04c31-118">Halten Sie sich für Kriterienzeichenfolgen an die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="04c31-118">Use the following guidelines for criteria strings:</span></span>

  - <span data-ttu-id="04c31-119">*FieldName* muss ein gültiger Feldname aus dem **Recordset-Objekt**sein.</span><span class="sxs-lookup"><span data-stu-id="04c31-119">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="04c31-120">Wenn der Feldname Leerzeichen enthält, müssen Sie ihn in eckige Klammern einschließen.</span><span class="sxs-lookup"><span data-stu-id="04c31-120">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

  - <span data-ttu-id="04c31-121">*Operator* muss einer der folgenden sein: \<, \>, \<=, \>=, \< \>, = oder **LIKE**.</span><span class="sxs-lookup"><span data-stu-id="04c31-121">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or **LIKE**.</span></span>

  - <span data-ttu-id="04c31-122">*Wert* ist der Wert, mit denen Sie die Feldwerte vergleichen (z. B. "Smith", \#8/24/95\#, 12.345 oder $50,00).</span><span class="sxs-lookup"><span data-stu-id="04c31-122">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="04c31-123">Verwenden Sie einfache Anführungszeichen mit Zeichenfolgen und Nummernzeichen (\#) mit einem Datum.</span><span class="sxs-lookup"><span data-stu-id="04c31-123">Use single quotes with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="04c31-124">Zahlen können Sie die Dezimalstellen, Dollarzeichen und die wissenschaftliche Schreibweise.</span><span class="sxs-lookup"><span data-stu-id="04c31-124">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="04c31-125">Wenn der *Operator* **wie**ist, können *Wert* Platzhalter verwenden.</span><span class="sxs-lookup"><span data-stu-id="04c31-125">If *Operator* is **LIKE**, *Value* can use wildcards.</span></span> <span data-ttu-id="04c31-126">Nur das Sternchen (\*) und Prozentzeichen (%) sind Platzhalter zulässig, und sie müssen das letzte Zeichen in der Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="04c31-126">Only the asterisk (\*) and percent sign (%) wild cards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="04c31-127">*Wert* darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="04c31-127">*Value* cannot be null.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="04c31-p105">[!HINWEIS] Wenn einzelne Anführungszeichen in den Filterwert eingeschlossen werden sollen, verwenden Sie zwei einzelne Anführungszeichen zur Darstellung. Soll beispielsweise nach "O'Malley" gefiltert werden, lautet die Kriterienzeichenfolge "col1 = 'O''Malley'". Setzen Sie die Zeichenfolge zwischen Nummernzeichen (#), um einzelne Anführungszeichen am Anfang und am Ende des Filterwerts einzuschließen. Wenn Sie z. B. nach '1' filtern möchten, muss die Kriterienzeichenfolge "col1 = #'1'#" lauten.</span><span class="sxs-lookup"><span data-stu-id="04c31-p105">To include single quotation marks (') in the filter Value, use two single quotation marks to represent one. For example, to filter on O'Malley, the criteria string should be "col1 = 'O''Malley'". To include single quotation marks at both the beginning and the end of the filter value, enclose the string with pound signs (#). For example, to filter on '1', the criteria string should be "col1 = #'1'#".</span></span>



  - <span data-ttu-id="04c31-p106">Es gibt keine Rangfolge zwischen **AND** und **OR**. Klauseln können in Klammern zusammengefasst werden. Sie können jedoch durch **OR** verbundene Klauseln nicht gruppieren und dann die Gruppe durch **AND** mit einer weiteren Klausel verbinden. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="04c31-p106">There is no precedence between **AND** and **OR**. Clauses can be grouped within parentheses. However, you cannot group clauses joined by an **OR** and then join the group to another clause with an **AND**, like this:</span></span>

  - <span data-ttu-id="04c31-135">Diesen Filter müssten Sie stattdessen folgendermaßen erstellen:</span><span class="sxs-lookup"><span data-stu-id="04c31-135">Instead, you would construct this filter as</span></span>

  - <span data-ttu-id="04c31-136">In einer Klausel **wie** Sie einen Platzhalter am Anfang und Ende des Musters verwenden (beispielsweise LastName Like '\*Mit\*"), oder nur am Ende des Musters (beispielsweise LastName Like" Smit\*").</span><span class="sxs-lookup"><span data-stu-id="04c31-136">In a **LIKE** clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*'), or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

<span data-ttu-id="04c31-137">Die Filterkonstanten vereinfachen das Lösen einzelner Datensatzkonflikte bei der Batchaktualisierung, indem Sie beispielsweise nur die Datensätze anzeigen, die durch den letzten Aufruf der [UpdateBatch](updatebatch-method-ado.md)-Methode beeinflusst wurden.</span><span class="sxs-lookup"><span data-stu-id="04c31-137">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last [UpdateBatch](updatebatch-method-ado.md) method call.</span></span>

<span data-ttu-id="04c31-p107">Die **Filter** -Eigenschaft direkt festzulegen schlägt möglicherweise wegen Konflikten mit den zugrunde liegenden Daten fehl (z. B. wenn ein Datensatz bereits von einem anderen Benutzer gelöscht wurde). In diesem Fall gibt der Anbieter Warnungen an die [Errors](errors-collection-ado.md)-Auflistung zurück, beendet die Ausführung des Programms jedoch nicht. Ein Laufzeitfehler tritt nur dann auf, wenn bei allen angeforderten Datensätzen Konflikte bestehen. Suchen Sie mithilfe der [Status](status-property-ado-recordset.md)-Eigenschaft nach Datensätzen mit Konflikten.</span><span class="sxs-lookup"><span data-stu-id="04c31-p107">Setting the **Filter** property itself may fail because of a conflict with the underlying data (for example, a record has already been deleted by another user). In such a case, the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records. Use the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="04c31-142">Das Festlegen der **Filter** -Eigenschaft auf eine leere Zeichenfolge ("") hat denselben Effekt wie die Verwendung der Konstante **adFilterNone**.</span><span class="sxs-lookup"><span data-stu-id="04c31-142">Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

<span data-ttu-id="04c31-p108">Sobald die **Filter** -Eigenschaft festgelegt wird, wechselt die aktuelle Datensatzposition zum ersten Datensatz in der gefilterten Teilmenge der Datensätze im **Recordset** -Objekt. Wird die **Filter** -Eigenschaft deaktiviert, wechselt dementsprechend die aktuelle Datensatzposition zum ersten Datensatz im **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="04c31-p108">Whenever the **Filter** property is set, the current record position moves to the first record in the filtered subset of records in the **Recordset**. Similarly, when the **Filter** property is cleared, the current record position moves to the first record in the **Recordset**.</span></span>

<span data-ttu-id="04c31-145">Unter der [Bookmark](bookmark-property-ado.md)-Eigenschaft finden Sie eine Erklärung der Textmarkenwerte, aus denen Sie ein Array zur Verwendung mit der **Filter** -Eigenschaft erstellen können.</span><span class="sxs-lookup"><span data-stu-id="04c31-145">See the [Bookmark](bookmark-property-ado.md) property for an explanation of bookmark values from which you can build an array to use with the **Filter** property.</span></span>

<span data-ttu-id="04c31-146">Nur **Filter** in der Form von Kriterienzeichenfolgen (z. B. Bestelldatum \> ' 12/31/1999 ') wirken sich auf den Inhalt eines permanenten **Recordset-Objekt**.</span><span class="sxs-lookup"><span data-stu-id="04c31-146">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="04c31-147">**Filter** mit einem Array von **Lesezeichen** erstellt oder mithilfe eines Werts aus der **FilterGroupEnum** wirkt sich nicht auf den Inhalt des gespeicherten Recordset-Objekts.</span><span class="sxs-lookup"><span data-stu-id="04c31-147">**Filters** created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted Recordset.</span></span> <span data-ttu-id="04c31-148">Diese Regeln gelten für **Recordsets** mit clientseitige oder serverseitige Cursor erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="04c31-148">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

> [!NOTE]
> <span data-ttu-id="04c31-p110">[!HINWEIS] Angenommen, Sie wenden das Kennzeichen **adFilterPendingRecords** auf ein gefiltertes und geändertes **Recordset** -Objekt im Batchaktualisierungsmodus an. In diesem Fall ist das resultierende **Recordset** -Objekt leer, wenn der Filter auf dem Schlüsselfeld einer Tabelle mit einem Schlüssel basierte und die Änderung zu den Schlüsselfeldwerten vorgenommen wurden. Das resultierende **Recordset** -Objekt ist nicht leer, wenn eine der folgenden Aussagen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="04c31-p110">When you apply the **adFilterPendingRecords** flag to a filtered and modified **Recordset** in the batch update mode, the resultant **Recordset** is empty if the filtering was based on the key field of a single-keyed table and the modification was made on the key field values. The resultant **Recordset** will be non-empty if one of the following is true:</span></span>
> - <span data-ttu-id="04c31-151">Die Filterung basierte in einer Tabelle mit einem Schlüssel auf Nichtschlüsselfeldern.</span><span class="sxs-lookup"><span data-stu-id="04c31-151">The filtering was based on non-key fields in a single-keyed table.</span></span>
> - <span data-ttu-id="04c31-152">Die Filterung basierte in einer Tabelle mit mehreren Schlüsseln auf allen Feldern.</span><span class="sxs-lookup"><span data-stu-id="04c31-152">The filtering was based on any fields in a multiple-keyed table.</span></span>
> - <span data-ttu-id="04c31-153">Änderungen wurden in einer Tabelle mit einem Schlüssel zu Nichtschlüsselfeldern vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="04c31-153">Modifications were made on non-key fields in a single-keyed table.</span></span>
> - <span data-ttu-id="04c31-154">Änderungen wurden in einer Tabelle mit mehreren Schlüsseln zu allen Feldern vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="04c31-154">Modifications were made on any fields in a multiple-keyed table.</span></span>

<span data-ttu-id="04c31-p111">In der folgenden Tabelle werden die Ergebnisse von **adFilterPendingRecords** in verschiedenen Filter- und Änderungskombinationen zusammengefasst. Die linke Spalte zeigt die möglichen Änderungen. Änderungen können für alle Nichtschlüsselfelder, für das Schlüsselfeld in einer Tabelle mit einem Schlüssel oder für alle Schlüsselfelder in einer Tabelle mit mehreren Schlüsseln erfolgen. Die obere Zeile enthält das Filterkriterium. Die Filterung kann auf allen Nichtschlüsselfeldern, dem Schlüsselfeld in einer Tabelle mit einem Schlüssel oder allen Schlüsselfeldern in einer Tabelle mit mehreren Schlüsseln basieren. Die sich überschneidenden Zellen enthalten die Ergebnisse: + bedeutet, dass **adFilterPendingRecords** ein nicht leeres **Recordset** -Objekt ergibt; **-** zeigt ein leeres **Recordset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="04c31-p111">The following table summarizes the effects of **adFilterPendingRecords** in different combinations of filtering and modifications. The left column shows the possible modifications; modifications can be made on any of the non-keyed fields, on the key field in a single-keyed table, or on any of the key fields in a multiple-keyed table. The top row shows the filtering criterion; filtering can be based on any of the non-keyed fields, the key field in a single-keyed table, or any of the key fields in a multiple-keyed table. The intersecting cells show the results: + means that applying **adFilterPendingRecords** results in a non-empty **Recordset**; **-** means an empty **Recordset**.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
</p></th>
<th><p><span data-ttu-id="04c31-159">Nichtschlüssel</span><span class="sxs-lookup"><span data-stu-id="04c31-159">Non keys</span></span></p></th>
<th><p><span data-ttu-id="04c31-160">Ein Schlüssel</span><span class="sxs-lookup"><span data-stu-id="04c31-160">Single Key</span></span></p></th>
<th><p><span data-ttu-id="04c31-161">Mehrere Schlüssel</span><span class="sxs-lookup"><span data-stu-id="04c31-161">Multiple Keys</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04c31-162">Nichtschlüssel</span><span class="sxs-lookup"><span data-stu-id="04c31-162">Non keys</span></span></p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04c31-163">Ein Schlüssel</span><span class="sxs-lookup"><span data-stu-id="04c31-163">Single Key</span></span></p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="04c31-164">n/v</span><span class="sxs-lookup"><span data-stu-id="04c31-164">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04c31-165">Mehrere Schlüssel</span><span class="sxs-lookup"><span data-stu-id="04c31-165">Multiple Keys</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="04c31-166">N/V</span><span class="sxs-lookup"><span data-stu-id="04c31-166">N/A</span></span></p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>

