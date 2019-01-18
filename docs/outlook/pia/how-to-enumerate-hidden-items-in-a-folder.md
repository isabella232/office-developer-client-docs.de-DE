---
title: Aufzählen von ausgeblendeten Elementen in einem Ordner
TOCTitle: Enumerate hidden items in a folder
ms:assetid: dafad1fb-94ce-4584-b5d1-2de5fad2f72a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184645(v=office.15)
ms:contentKeyID: 55119888
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6508ea955ad74b49b5fef73352b4a1706d8e338c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713198"
---
# <a name="enumerate-hidden-items-in-a-folder"></a><span data-ttu-id="a4be0-102">Aufzählen von ausgeblendeten Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="a4be0-102">Enumerate hidden items in a folder</span></span>

<span data-ttu-id="a4be0-103">Dieses Beispiel zeigt, wie Sie ausgeblendete Elemente in einem Ordner suchen und aufzählen.</span><span class="sxs-lookup"><span data-stu-id="a4be0-103">This example shows how to find and enumerate hidden items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="a4be0-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a4be0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a4be0-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="a4be0-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a4be0-106">Ein Feature des [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekts, das eine Gruppe von Elementen in einem Ordner darstellt, besteht darin, dass es ausgeblendete Elemente aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="a4be0-106">One feature of the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, which represents a set of items in a folder, is that it may have hidden items.</span></span> <span data-ttu-id="a4be0-107">Wenn ausgeblendete Elemente in einem Ordner zurückgegeben werden sollen, legen Sie den *TableContents*-Parameter in der [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\))-Methode des [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\))-Objekts auf [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)) fest.</span><span class="sxs-lookup"><span data-stu-id="a4be0-107">To return hidden items in a folder, set the *TableContents* parameter in the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object to [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)).</span></span> <span data-ttu-id="a4be0-108">Im folgenden Codebeispiel ruft TableForInboxHiddenItems die ausgeblendeten Elemente eines Posteingangsordners ab und schreibt die Werte der [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\))- und der [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\))-Eigenschaft für jedes ausgeblendete Element in die Listener der Ablaufverfolgung für die [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="a4be0-108">In the following code example, TableForInboxHiddenItems obtains the hidden items of an Inbox folder, and writes the values of the [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) and [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\)) properties for each hidden item to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="a4be0-109">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="a4be0-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a4be0-110">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a4be0-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a4be0-111">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a4be0-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableForInboxHiddenItems()
{
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with OlTableContents.olHiddenItems
    Outlook.Table table =
        folder.GetTable("",
        Outlook.OlTableContents.olHiddenItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        // Test for null subject
        if (nextRow["Subject"] == null)
        {
            Debug.WriteLine(nextRow["MessageClass"]);
        }
        else
        {
            Debug.WriteLine(nextRow["Subject"] + " "
                + nextRow["MessageClass"]);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="a4be0-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4be0-112">See also</span></span>

<span data-ttu-id="a4be0-113">-[Suchen und Filtern](search-and-filter.md)</span><span class="sxs-lookup"><span data-stu-id="a4be0-113">-[Search and filter](search-and-filter.md)</span></span>

