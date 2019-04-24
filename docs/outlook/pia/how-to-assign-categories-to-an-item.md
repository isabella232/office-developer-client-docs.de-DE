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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359732"
---
# <a name="assign-categories-to-an-item"></a>Zuweisen von Kategorien zu einem Element

Dieses Beispiel zeigt, wie Sie Kategorien mithilfe der **Categories**-Eigenschaft zu einem Element hinzufügen können.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Verwenden Sie zum Zuweisen von Kategorien zu einem Element die **Categories**-Eigenschaft des jeweiligen Elements. In diesem Codebeispiel wird die OutlookItem-Hilfsklasse verwendet, die unter [Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) definiert ist, um die OutlookItem.**Categories**-Methode aufzurufen, ohne das Element zunächst umwandeln zu müssen. Die **Categories**-Eigenschaft dient zum Abrufen oder Festlegen von Kategorien, die von einer Zeichenfolge mit Kommas als Trennzeichen und maximal 255 Zeichen dargestellt wird. Die Kommas und Leerzeichen werden verwendet, um die Kategoriewerte voneinander zu trennen. Wenn Sie eine Kategorie zuweisen, die sich nicht in der [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\))-Sammlung des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts befindet, führt dies dazu, dass die Kategorie keine Farbe angezeigt.

Im folgenden Codebeispiel erstellt AssignCategories eine Einschränkung für Elemente mit "ISV" im Betreff, indem zuerst eine DASL-Abfrage (DAV Searching and Locating) zum Filtern von Elementen im Posteingang ausgeführt wird, die "ISV" im Betreff enthalten. AssignCategories durchläuft anschließend die gefilterten Elemente mithilfe der **OutlookItem**-Klasse. Wenn die von **item.Categories** zurückgegebene Zeichenfolge kein NULL-Verweis ist oder bereits dem ISV zugewiesen wurde, wird die Kategorie "ISV" dem Element zugewiesen.

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

## <a name="see-also"></a>Siehe auch

- [Farbkategorien](color-categories.md)

