---
title: Verwenden von SetColumns zum effizienten Aufzählen von Elementen in einem Ordner
TOCTitle: Use SetColumns to efficiently enumerate items in a folder
ms:assetid: cd7c7758-8a9c-4f1c-a49c-9305d75be341
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184641(v=office.15)
ms:contentKeyID: 55119921
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bdfccc6432d35b6f39564e4c87404cc57b6ea27e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708088"
---
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a>Verwenden von SetColumns zum effizienten Aufzählen von Elementen in einem Ordner

In diesem Beispiel wird gezeigt, wie Sie eine Leistungssteigerung bei der Erstellung der [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) -Auflistung erzielen, indem Sie mithilfe der [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) -Methode bestimmte Eigenschaften der einzelnen Elemente in der Auflistung zwischenspeichern.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Zum Aufzählen der Elemente in einer Auflistung verwenden Sie die **SetColumns**-Methode, um die Eigenschaften für die **Items**-Auflistung zwischenzuspeichern. **SetColumns** nimmt als Argument eine Zeichenfolge mit durch Trennzeichen getrennten Werten an, die Eigenschaftennamen darstellt. Nachdem alle Elemente in der Auflistung aufgezählt worden sind, rufen Sie die [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) -Methode auf, um den Eigenschaftencache zu leeren.

Im folgenden Codebeispiel verwendet EnumerateContactsWithSetColumns die **SetColumns**-Methode, um die Eigenschaften [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) und [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) der Elemente im Ordner „Kontakte“ zwischenzuspeichern. Beachten Sie, dass Sie auf leere Zeichenfolgen oder einen NULL-Verweis in der Einschränkung testen müssen.

Ein Outlook-Ordner kann möglicherweise Elemente unterschiedlicher Typen enthalten. In diesem Codebeispiel wird die OutlookItem-Hilfsklasse verwendet, die unter [Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) definiert ist, um die OutlookItem.Class-Eigenschaft aufzurufen, um die Nachrichtenklasse jedes Elements in der gefilterten Untergruppe von Elementen im Ordner zu prüfen, ohne anzunehmen, dass es sich bei dem Element um ein Kontaktelement handelt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateContactsWithSetColumns()
{
    // Obtain Contacts folder
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    string filter = "Not([CompanyName] Is Null)" +
        " AND Not([JobTitle] Is Null)";
    Outlook.Items items = folder.Items.Restrict(filter);
    items.SetColumns("FileAs, CompanyName, JobTitle");
    for (int i = 1; i <= items.Count; i++)
    {
        // Create an instance of OutlookItem
        OutlookItem myItem = new OutlookItem(items[i]);
        if (myItem.Class == Outlook.OlObjectClass.olContact)
        {
            // Use InnerObject to return ContactItem
            Outlook.ContactItem contact =
                myItem.InnerObject as Outlook.ContactItem;
            StringBuilder sb = new StringBuilder();
            sb.AppendLine(contact.FileAs);
            sb.AppendLine(contact.CompanyName);
            sb.AppendLine(contact.JobTitle);
            sb.AppendLine();
            Debug.WriteLine(sb.ToString());
        }
    }
    items.ResetColumns();
}
```

## <a name="see-also"></a>Siehe auch

- [Suchen und Filtern](search-and-filter.md)

