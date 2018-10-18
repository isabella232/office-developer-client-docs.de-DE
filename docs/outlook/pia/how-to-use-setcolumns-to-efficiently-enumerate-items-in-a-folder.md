---
title: Verwenden von SetColumns zum effizienten Aufzählen von Elementen in einem Ordner
TOCTitle: Use SetColumns to efficiently enumerate items in a folder
ms:assetid: cd7c7758-8a9c-4f1c-a49c-9305d75be341
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184641(v=office.15)
ms:contentKeyID: 55119921
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2e75a0cb06420f5072805cdf03ad8f7925670e67
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407471"
---
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="72a31-102">Verwenden von SetColumns zum effizienten Aufzählen von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="72a31-102">Use SetColumns to efficiently enumerate items in a folder</span></span>

<span data-ttu-id="72a31-103">In diesem Beispiel wird gezeigt, wie Sie eine Leistungssteigerung bei der Erstellung der [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) -Auflistung erzielen, indem Sie mithilfe der [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) -Methode bestimmte Eigenschaften der einzelnen Elemente in der Auflistung zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="72a31-103">This example shows how to improve the performance of enumerating the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection by using the [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) method to cache certain properties of each item in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="72a31-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="72a31-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="72a31-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="72a31-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="72a31-p101">Zum Aufzählen der Elemente in einer Auflistung verwenden Sie die **SetColumns**-Methode, um die Eigenschaften für die **Items**-Auflistung zwischenzuspeichern. **SetColumns** nimmt als Argument eine Zeichenfolge mit durch Trennzeichen getrennten Werten an, die Eigenschaftennamen darstellt. Nachdem alle Elemente in der Auflistung aufgezählt worden sind, rufen Sie die [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) -Methode auf, um den Eigenschaftencache zu leeren.</span><span class="sxs-lookup"><span data-stu-id="72a31-p101">To enumerate items in a collection, use the **SetColumns** method to cache properties on the **Items** collection. **SetColumns** takes an argument that is a comma-delimited string that represents property names. Once all items in the collection have been enumerated, call the [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) method to clear the property cache.</span></span>

<span data-ttu-id="72a31-109">Im folgenden Codebeispiel verwendet EnumerateContactsWithSetColumns die **SetColumns**-Methode, um die Eigenschaften [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) und [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) der Elemente im Ordner „Kontakte“ zwischenzuspeichern.</span><span class="sxs-lookup"><span data-stu-id="72a31-109">In the following code example, EnumerateContactsWithSetColumns uses the **SetColumns** method to cache the [P:Microsoft.Office.Interop.Outlook._ContactItem.FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [P:Microsoft.Office.Interop.Outlook._ContactItem.CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), and [P:Microsoft.Office.Interop.Outlook._ContactItem.JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) properties of items in the Contacts folder. Note that you must test for empty strings or a null reference in the restriction.</span></span> <span data-ttu-id="72a31-110">Beachten Sie, dass Sie auf leere Zeichenfolgen oder einen NULL-Verweis in der Einschränkung testen müssen.</span><span class="sxs-lookup"><span data-stu-id="72a31-110">Note that you must test for empty strings or a null reference in the restriction.</span></span>

<span data-ttu-id="72a31-111">Ein Outlook-Ordner kann möglicherweise Elemente unterschiedlicher Typen enthalten.</span><span class="sxs-lookup"><span data-stu-id="72a31-111">Note that an Outlook folder can possibly contain items of different types.</span></span> <span data-ttu-id="72a31-112">In diesem Codebeispiel wird die OutlookItem-Hilfsklasse verwendet, die unter [Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) definiert ist, um die OutlookItem.Class-Eigenschaft aufzurufen, um die Nachrichtenklasse jedes Elements in der gefilterten Untergruppe von Elementen im Ordner zu prüfen, ohne anzunehmen, dass es sich bei dem Element um ein Kontaktelement handelt.</span><span class="sxs-lookup"><span data-stu-id="72a31-112">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.Class property to verify the message class of each item in the filtered subset of items in the folder, before assuming the item is a contact item.</span></span>

<span data-ttu-id="72a31-113">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="72a31-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="72a31-114">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="72a31-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="72a31-115">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="72a31-115">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="72a31-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72a31-116">See also</span></span>

- [<span data-ttu-id="72a31-117">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="72a31-117">Search and Filter</span></span>](search-and-filter.md)

