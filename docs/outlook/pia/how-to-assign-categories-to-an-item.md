---
title: Zuweisen von Kategorien zu einem Element
TOCTitle: Assign categories to an item
ms:assetid: 4070801b-994a-46df-91fe-4efca834886e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424469(v=office.15)
ms:contentKeyID: 55119828
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8b94d03a1aea447c4dba859659f044d8ec11994
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713296"
---
# <a name="assign-categories-to-an-item"></a><span data-ttu-id="163a1-102">Zuweisen von Kategorien zu einem Element</span><span class="sxs-lookup"><span data-stu-id="163a1-102">Assign categories to an item</span></span>

<span data-ttu-id="163a1-103">Dieses Beispiel zeigt, wie Sie Kategorien mithilfe der **Categories**-Eigenschaft zu einem Element hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="163a1-103">This example shows how to assign categories to an item by using its **Categories** property.</span></span>

## <a name="example"></a><span data-ttu-id="163a1-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="163a1-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="163a1-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="163a1-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="163a1-106">Verwenden Sie zum Zuweisen von Kategorien zu einem Element die **Categories**-Eigenschaft des jeweiligen Elements.</span><span class="sxs-lookup"><span data-stu-id="163a1-106">To assign categories to an item, use the particular item's **Categories** property.</span></span> <span data-ttu-id="163a1-107">In diesem Codebeispiel wird die OutlookItem-Hilfsklasse verwendet, die unter [Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) definiert ist, um die OutlookItem.**Categories**-Methode aufzurufen, ohne das Element zunächst umwandeln zu müssen.</span><span class="sxs-lookup"><span data-stu-id="163a1-107">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.**Categories** property without having to first cast the item.</span></span> <span data-ttu-id="163a1-108">Die **Categories**-Eigenschaft dient zum Abrufen oder Festlegen von Kategorien, die von einer Zeichenfolge mit Kommas als Trennzeichen und maximal 255 Zeichen dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="163a1-108">The **Categories** property gets or sets categories that are represented by a comma-delimited string that can contain a maximum of 255 characters.</span></span> <span data-ttu-id="163a1-109">Die Kommas und Leerzeichen werden verwendet, um die Kategoriewerte voneinander zu trennen.</span><span class="sxs-lookup"><span data-stu-id="163a1-109">The commas and spaces are used to separate the category values.</span></span> <span data-ttu-id="163a1-110">Wenn Sie eine Kategorie zuweisen, die sich nicht in der [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\))-Sammlung des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts befindet, führt dies dazu, dass die Kategorie keine Farbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="163a1-110">Assigning a category that is not in the [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) collection of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object will result in the category not displaying a color.</span></span>

<span data-ttu-id="163a1-p102">Im folgenden Codebeispiel erstellt AssignCategories eine Einschränkung für Elemente mit "ISV" im Betreff, indem zuerst eine DASL-Abfrage (DAV Searching and Locating) zum Filtern von Elementen im Posteingang ausgeführt wird, die "ISV" im Betreff enthalten. AssignCategories durchläuft anschließend die gefilterten Elemente mithilfe der **OutlookItem**-Klasse. Wenn die von **item.Categories** zurückgegebene Zeichenfolge kein NULL-Verweis ist oder bereits dem ISV zugewiesen wurde, wird die Kategorie "ISV" dem Element zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="163a1-p102">In the following code example, AssignCategories creates a restriction for items that contain “ISV” in the subject by first using a DAV Searching and Locating (DASL) query to filter items in the Inbox that contain “ISV” in the subject. AssignCategories then iterates through the filtered items by using the **OutlookItem** class and, if the string returned by **item.Categories** is not a null reference or was already assigned to the ISV, the ISV category is assigned to the item.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AssignCategories()
{
    string filter = "@SQL=" + "\"" + "urn:schemas:httpmail:subject"
        + "\"" + " ci_phrasematch 'ISV'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Restrict(filter);
    for (int i = 1; i <= items.Count; i++)
    {
        OutlookItem item = new OutlookItem(items[i]);
        string existingCategories = item.Categories;
        if (String.IsNullOrEmpty(existingCategories))
        {
            item.Categories = "ISV";
        }
        else
        {
            if (item.Categories.Contains("ISV") == false)
            {
                item.Categories = existingCategories + ", ISV";
            }
        }
        item.Save();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="163a1-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="163a1-113">See also</span></span>

- [<span data-ttu-id="163a1-114">Farbkategorien</span><span class="sxs-lookup"><span data-stu-id="163a1-114">Color categories</span></span>](color-categories.md)

