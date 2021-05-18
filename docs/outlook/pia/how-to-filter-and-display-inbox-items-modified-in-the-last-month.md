---
title: Filtern und Anzeigen der im letzten Monat geänderten Posteingangselemente
TOCTitle: Filter and display Inbox items modified in the last month
ms:assetid: ef6004dc-0b5a-4d1f-8937-1384d1dfc1ca
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424482(v=office.15)
ms:contentKeyID: 55119886
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77fe6e7df4cf67ed1ca2d62b8cf48f1b2873ccbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320293"
---
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a><span data-ttu-id="eff09-102">Filtern und Anzeigen der im letzten Monat geänderten Posteingangselemente</span><span class="sxs-lookup"><span data-stu-id="eff09-102">Filter and display Inbox items modified in the last month</span></span>

<span data-ttu-id="eff09-103">In diesem Beispiel wird veranschaulicht, wie Posteingangselemente gefiltert und angezeigt werden, die im letzten Monat geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="eff09-103">This example shows how to filter and display Inbox items that were modified in the last month.</span></span>

## <a name="example"></a><span data-ttu-id="eff09-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="eff09-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="eff09-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="eff09-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="eff09-106">Die Abfragesprache DAV Search and Locating (DASL) basiert auf der Microsoft Exchange-Implementierung von DASL in Outlook.</span><span class="sxs-lookup"><span data-stu-id="eff09-106">DAV Searching and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook.</span></span> <span data-ttu-id="eff09-107">Sie kann verwendet werden, um eigenschaftsbasierte Ergebnisse für Suchvorgänge auf Elementebene in Ordnerdaten zurückzugeben, z. B. die von einem [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt dargestellten Daten.</span><span class="sxs-lookup"><span data-stu-id="eff09-107">It can be used to return property-based results for item-level searches in folder data, such as that represented by a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="eff09-108">DASL-Filter unterstützen Zeichenfolgenvergleiche unter Verwendung des Gleichheitszeichens (=), einschließlich Äquivalenz, Präfix-, Ausdrucks- und Teilzeichenfolgenübereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="eff09-108">DASL filters support string comparisons, including equivalence, prefix, phrase, and substring matching, by using the equal (=) operator.</span></span> <span data-ttu-id="eff09-109">DASL-Abfragen können für einen Datums-/Uhrzeitvergleich und zum Filtern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eff09-109">You can use DASL queries to perform date-time comparison and filtering.</span></span>

<span data-ttu-id="eff09-p102">Da DASL-Abfragen **DateTime**-Vergleiche stets in koordinierter Weltzeit (Coordinated Universal Time, UTC) ausführen, müssen Sie den lokalen Zeitwert in UTC konvertieren, damit die Abfrage fehlerfrei funktioniert. Außerdem müssen Sie den **DateTime**-Wert in eine Zeichenfolgendarstellung umwandeln, weil DASL-Filter Zeichenfolgenvergleiche unterstützen. Sie haben zwei Möglichkeiten, die **DateTime**-Konvertierung durchzuführen: mithilfe der [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) -Methode des [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) -Objekts oder mithilfe von Outlook- **DateTime**-Makros.</span><span class="sxs-lookup"><span data-stu-id="eff09-p102">Because DASL queries always perform **DateTime** comparisons in Coordinated Universal Time (UTC), you must convert the local time value to UTC if you want the query to operate correctly. You must also convert the **DateTime** value to a string representation because DASL filters support string comparisons. You can make the **DateTime** conversion in two ways: by using the [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) method of the [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object, or by using Outlook **DateTime** macros to make the conversion.</span></span>

<span data-ttu-id="eff09-113">In der folgenden Codezeile wird die Verwendung der **LocalTimeToUTC**-Methode zum Konvertieren des Werts der **LastModificationTime**-Eigenschaft in UTC gezeigt (diese ist in allen **Item**-Objekten eine Standardspalte).</span><span class="sxs-lookup"><span data-stu-id="eff09-113">The following line of code shows how to use the **LocalTimeToUTC** method to convert the value of the **LastModificationTime** property (which is a default column in all **Item** objects) to UTC.</span></span>

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

<span data-ttu-id="eff09-114">In der folgenden Tabelle werden die **DateTime**-Makros aufgelistet, mit denen Sie gefilterte Zeichenfolgen zurückgeben können, die den Wert einer gegebenen **DateTime**-Eigenschaft mit einem angegebenen relativen Datum oder Datumsbereich in UTC vergleichen.</span><span class="sxs-lookup"><span data-stu-id="eff09-114">The following table lists the **DateTime** macros you can use to return filtered strings that compare the value of a given **DateTime** property with a specified relative date or date range in UTC.</span></span> <span data-ttu-id="eff09-115">Die SchemaName-Eigenschaft stellt eine beliebige gültige **DateTime**-Eigenschaft dar, auf die anhand des Namespace verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="eff09-115">The SchemaName property value represents any valid **DateTime** property referenced by namespace.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eff09-116">Makro</span><span class="sxs-lookup"><span data-stu-id="eff09-116">Macro</span></span></p></th>
<th><p><span data-ttu-id="eff09-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="eff09-117">Syntax</span></span></p></th>
<th><p><span data-ttu-id="eff09-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eff09-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eff09-119">heute</span><span class="sxs-lookup"><span data-stu-id="eff09-119">today</span></span></p></td>
<td><p><span data-ttu-id="eff09-120">%today(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="eff09-120">%today(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="eff09-121">Legt eine Beschränkung auf Elemente fest, deren Wert der SchemaName-Eigenschaft „heute“ lautet.</span><span class="sxs-lookup"><span data-stu-id="eff09-121">Restricts for items with a SchemaName property value equal to today.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff09-122">morgen</span><span class="sxs-lookup"><span data-stu-id="eff09-122">tomorrow</span></span></p></td>
<td><p><span data-ttu-id="eff09-123">%tomorrow(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="eff09-123">%tomorrow(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="eff09-124">Legt eine Beschränkung auf Elemente fest, deren Wert der SchemaName-Eigenschaft „morgen“ lautet.</span><span class="sxs-lookup"><span data-stu-id="eff09-124">Restricts for items with a SchemaName property value equal to tomorrow.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff09-125">gestern</span><span class="sxs-lookup"><span data-stu-id="eff09-125">yesterday</span></span></p></td>
<td><p><span data-ttu-id="eff09-126">%yesterday(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="eff09-126">%yesterday(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="eff09-127">Legt eine Beschränkung auf Elemente fest, deren Wert der SchemaName-Eigenschaft „gestern“ lautet.</span><span class="sxs-lookup"><span data-stu-id="eff09-127">Restricts for items with a SchemaName property value equal to yesterday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff09-128">next7days</span><span class="sxs-lookup"><span data-stu-id="eff09-128">next7days</span></span></p></td>
<td><p><span data-ttu-id="eff09-129">%next7days(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="eff09-129">%next7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="eff09-130">Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der den nächsten sieben Tagen entspricht.</span><span class="sxs-lookup"><span data-stu-id="eff09-130">Restricts for items with SchemaName property values in a range equivalent to the next seven days.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff09-131">last7days</span><span class="sxs-lookup"><span data-stu-id="eff09-131">last7days</span></span></p></td>
<td><p><span data-ttu-id="eff09-132">%last7days(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="eff09-132">%last7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="eff09-133">Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der den letzten sieben Tagen entspricht.</span><span class="sxs-lookup"><span data-stu-id="eff09-133">Restricts for items with SchemaName property values in a range equivalent to the last seven days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff09-134">nextweek</span><span class="sxs-lookup"><span data-stu-id="eff09-134">nextweek</span></span></p></td>
<td><p><span data-ttu-id="eff09-135">%nextweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="eff09-135">%nextweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="eff09-136">Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der der nächsten Woche entspricht.</span><span class="sxs-lookup"><span data-stu-id="eff09-136">Restricts for items with SchemaName property values in a range equivalent to next week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff09-137">thisweek</span><span class="sxs-lookup"><span data-stu-id="eff09-137">thisweek</span></span></p></td>
<td><p><span data-ttu-id="eff09-138">%thisweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="eff09-138">%thisweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="eff09-139">Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der dieser Woche entspricht.</span><span class="sxs-lookup"><span data-stu-id="eff09-139">Restricts for items with SchemaName property values in a range equivalent to this week.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff09-140">lastweek</span><span class="sxs-lookup"><span data-stu-id="eff09-140">lastweek</span></span></p></td>
<td><p><span data-ttu-id="eff09-141">%lastweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="eff09-141">%lastweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="eff09-142">Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der der letzten Woche entspricht.</span><span class="sxs-lookup"><span data-stu-id="eff09-142">Restricts for items with SchemaName property values in a range equivalent to last week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff09-143">nextmonth</span><span class="sxs-lookup"><span data-stu-id="eff09-143">nextmonth</span></span></p></td>
<td><p><span data-ttu-id="eff09-144">%nextmonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="eff09-144">%nextmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="eff09-145">Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der dem nächsten Monat entspricht.</span><span class="sxs-lookup"><span data-stu-id="eff09-145">Restricts for items with SchemaName property values in a range equivalent to next month.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff09-146">thismonth</span><span class="sxs-lookup"><span data-stu-id="eff09-146">thismonth</span></span></p></td>
<td><p><span data-ttu-id="eff09-147">%thismonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="eff09-147">%thismonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="eff09-148">Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte im Bereich dieses Monats hat.</span><span class="sxs-lookup"><span data-stu-id="eff09-148">Restricts for items with SchemaName property values in a range equivalent to this month.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff09-149">lastmonth</span><span class="sxs-lookup"><span data-stu-id="eff09-149">lastmonth</span></span></p></td>
<td><p><span data-ttu-id="eff09-150">%lastmonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="eff09-150">%lastmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="eff09-151">Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte im Bereich des letzten Monats hat.</span><span class="sxs-lookup"><span data-stu-id="eff09-151">Restricts for items with SchemaName property values in a range equivalent to last month.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eff09-152">Im folgenden Beispiel erstellt DemoDASLDateMacro eine DASL-Abfrage, in der mit dem **lastmonthDateTime**-Makro Elemente aus dem Posteingang des Benutzers herausgefiltert werden, die im vergangenen Monat geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="eff09-152">In the following example, DemoDASLDateMacro creates a DASL query that uses the **lastmonthDateTime** macro to filter for items in the user’s Inbox that were modified in the last month.</span></span> <span data-ttu-id="eff09-153">Dann wird ein **Table**-Objekt mit diesen Filter erstellt die Zeilen in dem eingeschränkten **Table**-Objekt aufgezählt und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eff09-153">It then creates a **Table** object with that filter, and enumerates and displays the rows in the restricted **Table** object.</span></span>

<span data-ttu-id="eff09-154">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="eff09-154">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="eff09-155">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="eff09-155">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="eff09-156">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="eff09-156">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoDASLDateMacro()
{
    string filter = "@SQL=" + "%lastmonth(" + "\"" +
        "DAV:getlastmodified" + "\"" + ")%";
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="eff09-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eff09-157">See also</span></span>

- [<span data-ttu-id="eff09-158">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="eff09-158">Search and filter</span></span>](search-and-filter.md)

