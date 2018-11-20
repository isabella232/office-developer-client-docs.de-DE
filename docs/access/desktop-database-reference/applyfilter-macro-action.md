---
title: ApplyFilter-Makroaktion
TOCTitle: ApplyFilter macro action
ms:assetid: c63988c4-4506-cc51-98f7-478d1f3fe668
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823130(v=office.15)
ms:contentKeyID: 48547623
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm79035
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f6f0511a1358e8d9b0d0ee820e83cf59d2400345
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025967"
---
# <a name="applyfilter-macro-action"></a><span data-ttu-id="5a641-102">ApplyFilter-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="5a641-102">ApplyFilter macro action</span></span>

<span data-ttu-id="5a641-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a641-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a641-p101">Sie können die **AnwendenFilter** -Aktion verwenden, um einen Filter, eine Abfrage oder eine SQL WHERE-Klausel auf eine Tabelle, ein Formular oder einen Bericht anzuwenden, wenn Sie die Datensätze in der Tabelle bzw. die Datensätze der zugrunde liegenden Tabelle oder Abfrage des Formulars oder Berichts einschränken oder sortieren möchten. Für Berichte können Sie diese Aktion nur in einem Makro verwenden, das in der **BeimÖffnen** -Ereigniseigenschaft des Berichts angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5a641-p101">You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report. For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.</span></span>

> [!NOTE]
> <span data-ttu-id="5a641-p102">[!HINWEIS] Sie können diese Aktion zum Anwenden einer SQL WHERE-Klausel nur dann verwenden, wenn Sie einen Serverfilter anwenden. Ein Serverfilter kann nicht auf die gespeicherte Datensatzquelle einer Prozedur angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a641-p102">You can use this action to apply an SQL WHERE clause only when applying a server filter. A server filter cannot be applied to a stored procedure's record source.</span></span>

## <a name="setting"></a><span data-ttu-id="5a641-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="5a641-108">Setting</span></span>

<span data-ttu-id="5a641-109">Die **AnwendenFilter** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="5a641-109">The **ApplyFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a641-110">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="5a641-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5a641-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a641-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a641-112">Filtername</span><span class="sxs-lookup"><span data-stu-id="5a641-112">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="5a641-113">Der Name eines Filters oder einer Abfrage, die die Datensätze der Tabelle, Formular oder Bericht einschränkt oder sortiert.</span><span class="sxs-lookup"><span data-stu-id="5a641-113">The name of a filter or query that restricts or sorts the records of the table, form, or report.</span></span> <span data-ttu-id="5a641-114">Sie können den Namen einer vorhandenen Abfrage oder eines Filters, das als eine Abfrage im Feld <strong>Name des Filters</strong> im <strong>Abschnitt</strong> Bereich des <strong>Makro-Generators</strong> gespeichert wurde, eingeben.</span><span class="sxs-lookup"><span data-stu-id="5a641-114">You can enter the name of either an existing query or a filter that has been saved as a query in the <strong>Filter Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane.</span></span></p><p><span data-ttu-id="5a641-115"><strong>Hinweis</strong>: Wenn Sie diese Aktion verwenden, um einen Serverfilter anzuwenden, muss das Argument Filtername leer sein.</span><span class="sxs-lookup"><span data-stu-id="5a641-115"><strong>NOTE</strong>: When you are using this action to apply a server filter, the Filter Name argument must be blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a641-116">Where Condition</span><span class="sxs-lookup"><span data-stu-id="5a641-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="5a641-117">Eine gültige SQL WHERE-Klausel (ohne das Wort WHERE) oder ein Ausdruck, der die Datensätze der Tabelle, des Formulars oder des Berichts einschränkt. 

</span><span class="sxs-lookup"><span data-stu-id="5a641-117">A valid SQL WHERE clause (without the word WHERE) or an expression that restricts the records of the table, form, or report.</span></span></p>
<p><span data-ttu-id="5a641-118"><b>Hinweis</b>: In einer Bedingung-Argumentausdruck, der linken Seite des Ausdrucks in der Regel enthält einen Feldnamen aus der zugrunde liegenden Tabelle oder Abfrage für das Formular oder Bericht.</span><span class="sxs-lookup"><span data-stu-id="5a641-118"><b>NOTE</b>: In a Where Condition argument expression, the left side of the expression typically contains a field name from the underlying table or query for the form or report.</span></span> <span data-ttu-id="5a641-119">Die rechte Seite des Ausdrucks enthält in der Regel die Kriterien, die Sie in dieses Feld einschränken oder Sortieren der Datensätze anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="5a641-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span></span> <span data-ttu-id="5a641-120">Die Kriterien können beispielsweise den Namen eines Steuerelements oder eines anderen Formulars sein, die den Wert enthält, den die Datensätze in der ersten Formular übereinstimmen sollen.</span><span class="sxs-lookup"><span data-stu-id="5a641-120">For example, the criteria can be the name of a control on another form that contains the value you want the records in the first form to match.</span></span> <span data-ttu-id="5a641-121">Der Name des Steuerelements sollte beispielsweise vollständig qualifizierte sein:</span><span class="sxs-lookup"><span data-stu-id="5a641-121">The name of the control should be fully qualified, for example:</span></span></p>
<p><span data-ttu-id="5a641-122"><strong>Formulare</strong>! <em>Formularname</em>! <em>Steuerelementname</em> Feldnamen sollten von doppelten Anführungszeichen umgeben sein und Zeichenfolgenliterale von Hochkommas umgeben sein sollte.</span><span class="sxs-lookup"><span data-stu-id="5a641-122"><strong>Forms</strong>!<em>formname</em>!<em>controlname</em> Field names should be surrounded by double quotation marks and string literals should be surrounded by single quotation marks.</span></span> <span data-ttu-id="5a641-123">Das Argument Bedingung die maximale Länge beträgt 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5a641-123">The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="5a641-124">Wenn Sie eine längere SQL WHERE-Klausel eingeben müssen, verwenden Sie die <strong>ApplyFilter</strong> -Methode des <strong>DoCmd</strong> -Objekts in einem Visual Basic für Applikationen (VBA)-Modul.</span><span class="sxs-lookup"><span data-stu-id="5a641-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="5a641-125">Sie können in VBA SQL WHERE-Klausel Anweisungen von bis zu 32.768 Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="5a641-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5a641-p106">[!HINWEIS] Sie können das Argument Filtername verwenden, wenn Sie bereits einen Filter definiert haben, der die entsprechenden Daten bereitstellt. Sie können das Argument Bedingung verwenden, um die Einschränkungskriterien direkt einzugeben. Wenn Sie beide Argumente verwenden, wendet Microsoft Office Access 2007 die WHERE-Klausel auf die Ergebnisse des Filtervorgangs an. Sie müssen mindestens eines der Argumente verwenden.</span><span class="sxs-lookup"><span data-stu-id="5a641-p106">You can use the Filter Name argument if you have already defined a filter that provides the appropriate data. You can use the Where Condition argument to enter the restriction criteria directly. If you use both arguments, Microsoft Office Access 2007 applies the WHERE clause to the results of the filter. You must use one or both arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a641-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a641-130">Remarks</span></span>

<span data-ttu-id="5a641-131">Sie können einen Filter oder eine Abfrage auf ein Formular in der Formularansicht oder in der Datenblattansicht anwenden.</span><span class="sxs-lookup"><span data-stu-id="5a641-131">You can apply a filter or query to a form in Form view or Datasheet view.</span></span>

<span data-ttu-id="5a641-132">Der angewendete Filter und die WHERE-Bedingung werden zur Einstellung der **Filter**- oder **Serverfilter**-Eigenschaft des Formulars oder des Berichts.</span><span class="sxs-lookup"><span data-stu-id="5a641-132">The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.</span></span>

<span data-ttu-id="5a641-p107">Für Tabellen und Formulare ist diese Aktion mit dem Klicken auf **Filter/Sortierung anwenden** oder **Serverfilter anwenden** im Menü **Datensätze** vergleichbar. Der Menübefehl wendet den zuletzt erstellten Filter auf die Tabelle oder das Formular an, wohingegen die **AnwendenFilter** -Aktion einen angegebenen Filter oder eine angegebene Abfrage anwendet.</span><span class="sxs-lookup"><span data-stu-id="5a641-p107">For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu. The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.</span></span>

<span data-ttu-id="5a641-135">Wenn Sie in einer Access-Datenbank im Menü Datensätze auf Filter zeigen und nach dem Ausführen der AnwendenFilter-Aktion auf Spezialfilter/-sortierung klicken, werden im Fenster Spezialfilter/-sortierung die Filterkriterien angezeigt, die Sie mit dieser Aktion ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="5a641-135">In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.</span></span>

<span data-ttu-id="5a641-p108">Sie können die AnzeigenAlleDatensätze-Aktion oder den Befehl Filter/Sortierung entfernen im Menü Datensätze verwenden, um einen Filter zu entfernen und alle Datensätze einer Tabelle oder eines Formulars in einer Office Access 2007-Datenbank anzuzeigen. Wenn Sie einen Filter aus einem Access-Projekt (ADP) entfernen möchten, können Sie zum Fenster Formularbasierter Serverfilter zurückkehren, alle Filterkriterien entfernen und dann im Menü Datensätze auf der Symbolleiste auf Serverfilter anwenden klicken. Oder Sie können die FormularbasierterServerFilter-Eigenschaft auf Falsch (0) festlegen.</span><span class="sxs-lookup"><span data-stu-id="5a641-p108">To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu. To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).</span></span>

<span data-ttu-id="5a641-p109">Beim Speichern einer Tabelle oder eines Formulars speichert Access alle Filter, die in dem Objekt derzeit definiert sind, wendet die Filter jedoch das nächste Mal, wenn das Objekt geöffnet wird, nicht an (wobei jedoch eine vor dem Speichern auf das Objekt angewendete Sortierung automatisch angewendet wird). Wenn ein Filter automatisch beim ersten Öffnen des Formulars angewendet werden soll, geben Sie ein Makro, das die **AnwendenFilter** -Aktion enthält, oder eine Ereignisprozedur mit der **ApplyFilter** -Methode des **DoCmd** -Objekts als Einstellung für die **BeimÖffnen** -Ereigniseigenschaft des Formulars an. Sie können einen Filter auch anwenden, indem Sie die **ÖffnenFormular** - oder die **ÖffnenBericht** -Aktion oder die entsprechenden Methoden verwenden. Sie können die Tabelle öffnen, indem Sie ein Makro, das die **ÖffnenTabelle** -Aktion enthält, und anschließend die **AnwendenFilter** -Aktion verwenden. Auf diese Weise wird ein Filter automatisch beim ersten Öffnen einer Tabelle angewendet.</span><span class="sxs-lookup"><span data-stu-id="5a641-p109">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved). If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form. You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods. To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span></span>

## <a name="example"></a><span data-ttu-id="5a641-142">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5a641-142">Example</span></span>

<span data-ttu-id="5a641-143">Das folgende Beispiel veranschaulicht die ApplyFilter-Aktion verwenden, um das Formular FrmFoods filtern, während es geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5a641-143">The following example shows how to use the ApplyFilter action to filter the frmFoods form as it is opened.</span></span>

<span data-ttu-id="5a641-144">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="5a641-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    ApplyFilter
        Filter Name
        Where Condition=[display_name] Link "*cheese*"
        Control Name
```



