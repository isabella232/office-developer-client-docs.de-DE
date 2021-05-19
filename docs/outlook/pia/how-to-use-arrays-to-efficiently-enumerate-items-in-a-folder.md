---
title: Verwenden von Arrays zum effizienten Aufzählen von Elementen in einem Ordner
TOCTitle: Use arrays to efficiently enumerate items in a folder
ms:assetid: 05a73225-ad0d-4d52-90b6-448d220348df
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184588(v=office.15)
ms:contentKeyID: 55119885
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be65e2818f22e6da289ef8b8da483c2747f941a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335385"
---
# <a name="use-arrays-to-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="3617f-102">Verwenden von Arrays zum effizienten Aufzählen von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="3617f-102">Use arrays to efficiently enumerate items in a folder</span></span>

<span data-ttu-id="3617f-103">In diesem Beispiel wird gezeigt, wie Elemente in einem [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekt mithilfe der [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\))-Methode effizient aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="3617f-103">This example shows how to efficiently enumerate items in a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object by using the [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="3617f-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3617f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="3617f-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="3617f-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="3617f-106">Im folgenden Codebeispiel ruft DemoGetArrayForTable mit der [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\))-Methode ein [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt aus einem **Folder**-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="3617f-106">In the following code example, DemoGetArrayForTable gets a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object from a **Folder** object by using the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method.</span></span> <span data-ttu-id="3617f-107">DemoGetArrayForTable gibt anschließend mithilfe der **GetArray**-Methode ein [Array](https://msdn.microsoft.com/library/system.array.aspx)-Objekt zurück, das Elemente für jede Zeile in der Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="3617f-107">DemoGetArrayForTable then uses the **GetArray** method to return an [Array](https://msdn.microsoft.com/library/system.array.aspx) object that contains elements for every row in the table.</span></span> <span data-ttu-id="3617f-108">Das zurückgegebene **Array**-Objekt ist ein zweidimensionales Array, das eine Gruppe von Zeilen- und Werten aus der **Tabelle** darstellt.</span><span class="sxs-lookup"><span data-stu-id="3617f-108">The returned **Array** object is a two-dimensional array that represents a set of row and column values from the **Table**.</span></span> <span data-ttu-id="3617f-109">Das Array ist nullbasiert (nicht einsbasiert wie bei Outlook-Auflistungen).</span><span class="sxs-lookup"><span data-stu-id="3617f-109">The array is zero-based, instead of one-based as is the case with Outlook collections.</span></span> <span data-ttu-id="3617f-110">Nach Abrufen des **Array**-Objekts verwendet der Code eine for-Schleife zum Auflisten der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3617f-110">Once the **Array** object is obtained, the code uses a for loop to enumerate through the table.</span></span>

<span data-ttu-id="3617f-111">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="3617f-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3617f-112">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3617f-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3617f-113">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="3617f-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoGetArrayForTable()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Table table =
        folder.GetTable("", Outlook.OlTableContents.olUserItems);
    Array tableArray = table.GetArray(table.GetRowCount()) as Array;
    for (int i = 0; i <= tableArray.GetUpperBound(0); i++)
    {
        for (int j = 0; j <= tableArray.GetUpperBound(1); j++)
        {
            Debug.WriteLine(tableArray.GetValue(i, j));
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3617f-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3617f-114">See also</span></span>

- [<span data-ttu-id="3617f-115">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="3617f-115">Search and filter</span></span>](search-and-filter.md)

