---
title: Filtern und Anzeigen von mehrwertigen Eigenschaften beim Aufzählen von Elementen in einem Ordner
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: acb6f6807f956ee6d468d3fcefc2cdd27732ab9b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320321"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a>Filtern und Anzeigen von mehrwertigen Eigenschaften beim Aufzählen von Elementen in einem Ordner

In diesem Beispiel wird gezeigt, wie Sie beim Aufzählen von Elementen in einem Ordner Eigenschaften mit mehreren Werten filtern und anzeigen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Das [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) -Objekt stellt eine Gruppe von Elementdaten aus einem [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) - oder einem [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) -Objekt dar. Wird eine binäre, eine Datums- oder eine mehrwertige Eigenschaft das erste Mal einem **Table**-Objekt hinzugefügt, beeinflusst die Art und Weise, wie die Eigenschaft referenziert wird, ihren Typ und ihr Format. Da ein Verweis mit integriertem Namen manchmal einen anderen Spaltenwert zurückgibt als ein Namespaceverweis, sollten Sie bestimmen, ob die Eigenschaft durch ihren expliziten integrierten Namen (sofern vorhanden) referenziert wird oder durch den Namespace (unabhängig vom Vorhandensein eines expliziten integrierten Namens). In der folgenden Tabelle wird der Unterschied in der Darstellung des Eigenschaftswerts (hinsichtlich Typ und Format) für die verschiedenen Ursprungstypen von Eigenschaften gezeigt.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Typ</p></th>
<th><p>Rückgabetyp, wenn für die angegebene Eigenschaft ein integrierter Namen verwendet wird</p></th>
<th><p>Rückgabetyp, wenn die angegebene Eigenschaft einen Namespace verwendet</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Binär (<b>PT_BINARY</b>)</p></td>
<td><p>Zeichenfolge</p></td>
<td><p>Bytearray</p></td>
</tr>
<tr class="even">
<td><p>Datum (<b>PT_SYSTIME</b>)</p></td>
<td><p>Lokal <b>DateTime</b></p></td>
<td><p>UTC <b>DateTime</b></p></td>
</tr>
<tr class="odd">
<td><p>Mehrwertig (auch als Schlüsselworttyp bezeichnet), z. B. <b>Categories</b>-Eigenschaft (<b>PT_MV_STRING8</b>)</p></td>
<td><p>Zeichenfolge, die durch Trennzeichen getrennte Werte enthält.</p></td>
<td><p>Eindimensionales Array, das für jedes Schlüsselwort ein Element enthält.</p></td>
</tr>
</tbody>
</table>


Im folgenden Codebeispiel wird veranschaulicht, wie Sie dem **Table**-Objekt eine Eigenschaft mit einem MAPI-Zeichenfolgennamespace hinzufügen und wie sich mehrwertige Eigenschaften auf die in einem [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) -Objekt zurückgegebenen Werte auswirken. Die TableMultiValuedProperties-Prozedur filtert das **Table**-Objekt nach Zeilen, in denen die [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\))-Eigenschaft kein Nullverweis ist. Die **Categories**-Eigenschaft wird durch eine Eigenschaft dargestellt, die den MAPI-Zeichenfolgennamespace verwendet. Ein DASL-Filter (DAV Searching and Locating) wird für Elemente erstellt, die Kategorien aufweisen (der tatsächliche Filter gibt Kategorien zurück, die keinen Nullverweise haben). Anschließend wird dem **Table**-Objekt durch Verketten des Typbezeichners, 0000001f, mit der categoriesProperty-Konstanten eine **Categories**-Spalte hinzugefügt. Das **Column**-Objekt schließlich, das die **Categories**-Eigenschaft darstellt, enthält ein eindimensionales Zeichenfolgenarray, wobei jedes Element des Arrays eine dem Element zugeordnete Kategorie darstellt. Sowohl die **Categories**- als auch die **Subject**-Eigenschaft des Elements werden in die Listener der Ablaufverfolgung der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung geschrieben.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableMultiValuedProperties()
{
    const string categoriesProperty =
        "https://schemas.microsoft.com/mapi/string/"
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

## <a name="see-also"></a>Siehe auch

- [Suchen und Filtern](search-and-filter.md)

