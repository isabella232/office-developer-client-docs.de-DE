---
title: Filtern und Anzeigen von mehrwertigen Eigenschaften beim Aufzählen von Elementen in einem Ordner
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d6242506bac081ee16d125ea92fbed69939c6abc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542625"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="a310e-102">Filtern und Anzeigen von mehrwertigen Eigenschaften beim Aufzählen von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="a310e-102">Filter and display multivalued properties when enumerating items in a folder</span></span>

<span data-ttu-id="a310e-103">In diesem Beispiel wird gezeigt, wie Sie beim Aufzählen von Elementen in einem Ordner Eigenschaften mit mehreren Werten filtern und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a310e-103">This example shows how to filter and display multivalued properties while enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="a310e-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a310e-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a310e-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="a310e-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a310e-p101">Das [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) -Objekt stellt eine Gruppe von Elementdaten aus einem [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) - oder einem [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) -Objekt dar. Wird eine binäre, eine Datums- oder eine mehrwertige Eigenschaft das erste Mal einem **Table**-Objekt hinzugefügt, beeinflusst die Art und Weise, wie die Eigenschaft referenziert wird, ihren Typ und ihr Format. Da ein Verweis mit integriertem Namen manchmal einen anderen Spaltenwert zurückgibt als ein Namespaceverweis, sollten Sie bestimmen, ob die Eigenschaft durch ihren expliziten integrierten Namen (sofern vorhanden) referenziert wird oder durch den Namespace (unabhängig vom Vorhandensein eines expliziten integrierten Namens). In der folgenden Tabelle wird der Unterschied in der Darstellung des Eigenschaftswerts (hinsichtlich Typ und Format) für die verschiedenen Ursprungstypen von Eigenschaften gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a310e-p101">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object. When a binary, date, or multivalued property is first added to a **Table** object, the way the property is referenced affects its type and format. Because built-in name references sometimes return a different column value than a namespace reference, you should determine whether the property is referenced by its explicit built-in name (if it has one), or by namespace (regardless of the existence of an explicit built-in name). The following table shows the difference in the property value representation (in terms of type and format) per original property type.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a310e-110">Typ</span><span class="sxs-lookup"><span data-stu-id="a310e-110">Type</span></span></p></th>
<th><p><span data-ttu-id="a310e-111">Rückgabetyp, wenn für die angegebene Eigenschaft ein integrierter Namen verwendet wird</span><span class="sxs-lookup"><span data-stu-id="a310e-111">Return type if the specified property uses a built-in name</span></span></p></th>
<th><p><span data-ttu-id="a310e-112">Rückgabetyp, wenn die angegebene Eigenschaft einen Namespace verwendet</span><span class="sxs-lookup"><span data-stu-id="a310e-112">Return type if the specified property uses a namespace</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a310e-113">Binär (<b>PT_BINARY</b>)</span><span class="sxs-lookup"><span data-stu-id="a310e-113">Binary <b>(PT_BINARY)</b></span></span></p></td>
<td><p><span data-ttu-id="a310e-114">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a310e-114">String</span></span></p></td>
<td><p><span data-ttu-id="a310e-115">Bytearray</span><span class="sxs-lookup"><span data-stu-id="a310e-115">Byte array</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a310e-116">Datum (<b>PT_SYSTIME</b>)</span><span class="sxs-lookup"><span data-stu-id="a310e-116">Date <b>(PT_SYSTIME)</b></span></span></p></td>
<td><p><span data-ttu-id="a310e-117">Lokal <b>DateTime</b></span><span class="sxs-lookup"><span data-stu-id="a310e-117">Local <b>DateTime</b></span></span></p></td>
<td><p><span data-ttu-id="a310e-118">UTC <b>DateTime</b></span><span class="sxs-lookup"><span data-stu-id="a310e-118">UTC <b>DateTime</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a310e-119">Mehrwertig (auch als Schlüsselworttyp bezeichnet), z. B. <b>Categories</b>-Eigenschaft (<b>PT_MV_STRING8</b>)</span><span class="sxs-lookup"><span data-stu-id="a310e-119">Multivalued (also known as keyword type) such as <b>Categories</b> property <b>(PT_MV_STRING8)</b></span></span></p></td>
<td><p><span data-ttu-id="a310e-120">Zeichenfolge, die durch Trennzeichen getrennte Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="a310e-120">String that contains comma-separated values</span></span></p></td>
<td><p><span data-ttu-id="a310e-121">Eindimensionales Array, das für jedes Schlüsselwort ein Element enthält.</span><span class="sxs-lookup"><span data-stu-id="a310e-121">One-dimensional array that contains one element for each keyword</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a310e-122">Im folgenden Codebeispiel wird veranschaulicht, wie Sie dem **Table**-Objekt eine Eigenschaft mit einem MAPI-Zeichenfolgennamespace hinzufügen und wie sich mehrwertige Eigenschaften auf die in einem [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) -Objekt zurückgegebenen Werte auswirken.</span><span class="sxs-lookup"><span data-stu-id="a310e-122">The following code example illustrates how to add a MAPI string namespace property to the **Table** object and how multivalued properties affect the values returned in a [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object.</span></span> <span data-ttu-id="a310e-123">Die TableMultiValuedProperties-Prozedur filtert das **Table**-Objekt nach Zeilen, in denen die [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\))-Eigenschaft kein Nullverweis ist.</span><span class="sxs-lookup"><span data-stu-id="a310e-123">The TableMultiValuedProperties procedure filters the **Table** object for rows where the [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) property is not a null reference.</span></span> <span data-ttu-id="a310e-124">Die **Categories**-Eigenschaft wird durch eine Eigenschaft dargestellt, die den MAPI-Zeichenfolgennamespace verwendet.</span><span class="sxs-lookup"><span data-stu-id="a310e-124">The **Categories** property is represented by a property that uses the MAPI string namespace.</span></span> <span data-ttu-id="a310e-125">Ein DASL-Filter (DAV Searching and Locating) wird für Elemente erstellt, die Kategorien aufweisen (der tatsächliche Filter gibt Kategorien zurück, die keinen Nullverweise haben).</span><span class="sxs-lookup"><span data-stu-id="a310e-125">A DAV Searching and Locating (DASL) filter is constructed for items that have categories (the actual filter returns categories that do not have a null reference).</span></span> <span data-ttu-id="a310e-126">Anschließend wird dem **Table**-Objekt durch Verketten des Typbezeichners, 0000001f, mit der categoriesProperty-Konstanten eine **Categories**-Spalte hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a310e-126">A **Categories** column is then added to the **Table** object by concatenating the type specifier, 0000001f, with the categoriesProperty constant.</span></span> <span data-ttu-id="a310e-127">Das **Column**-Objekt schließlich, das die **Categories**-Eigenschaft darstellt, enthält ein eindimensionales Zeichenfolgenarray, wobei jedes Element des Arrays eine dem Element zugeordnete Kategorie darstellt.</span><span class="sxs-lookup"><span data-stu-id="a310e-127">Finally, the **Column** object that represents the **Categories** property contains a one-dimensional string array where each element of the array represents a category assigned to the item.</span></span> <span data-ttu-id="a310e-128">Sowohl die **Categories**- als auch die **Subject**-Eigenschaft des Elements werden in die Listener der Ablaufverfolgung der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung geschrieben.</span><span class="sxs-lookup"><span data-stu-id="a310e-128">Both the item’s **Categories** and **Subject** properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="a310e-129">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="a310e-129">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a310e-130">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a310e-130">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a310e-131">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a310e-131">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableMultiValuedProperties()
{
    const string categoriesProperty =
        "http://schemas.microsoft.com/mapi/string/"
        + "{00020329-0000-0000-C000-000000000046}/Keywords";
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with filter for categories
    string filter = "@SQL="
        + "Not(" + "\"" + categoriesProperty
        + "\"" + " Is Null)";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Add categories column and append type specifier
    table.Columns.Add(categoriesProperty + "/0000001F");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        string[] categories =
            (string[])nextRow[categoriesProperty + "/0000001F"];
        Debug.WriteLine("Subject: " + nextRow["Subject"]);
        Debug.Write("Categories: ");
        foreach (string category in categories)
        {
            Debug.Write("\t" + category);
        }
        Debug.WriteLine("\n");
    }
}
```

## <a name="see-also"></a><span data-ttu-id="a310e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a310e-132">See also</span></span>

- [<span data-ttu-id="a310e-133">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="a310e-133">Search and filter</span></span>](search-and-filter.md)

