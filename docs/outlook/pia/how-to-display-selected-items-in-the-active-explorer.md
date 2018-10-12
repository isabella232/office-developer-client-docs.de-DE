---
title: Anzeigen von ausgewählten Elementen im aktiven Explorer
TOCTitle: Display selected items in the active Explorer
ms:assetid: 31bb217b-8b45-4b50-942e-b6c2a7f13c83
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292517(v=office.15)
ms:contentKeyID: 55119844
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d2599aff01afc7cc02797210a260befdfb72be33
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405504"
---
# <a name="display-selected-items-in-the-active-explorer"></a><span data-ttu-id="d3f88-102">Anzeigen von ausgewählten Elementen im aktiven Explorer</span><span class="sxs-lookup"><span data-stu-id="d3f88-102">Display selected items in the active Explorer</span></span>

<span data-ttu-id="d3f88-103">Dieses Beispiel zeigt, wie Sie mit der OutlookItem-Hilfsklasse problemlos alle im aktiven Explorer-Fenster ausgewählten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d3f88-103">This example shows how to use the OutlookItem helper class to conveniently display all the items selected in the active Explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="d3f88-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3f88-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d3f88-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="d3f88-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="d3f88-106">Das [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\))-Objekt enthält die Gruppe von Outlook-Elementen, die aktuell im aktiven Outlook-Explorer ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="d3f88-106">The [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) object contains the set of Outlook items currently selected in the active Outlook explorer.</span></span> <span data-ttu-id="d3f88-107">Weder der aktive Explorer, der durch [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)) dargestellt ist, noch die Gruppe der ausgewählten Elementen gibt den Typ der ausgewählten Elemente an.</span><span class="sxs-lookup"><span data-stu-id="d3f88-107">Neither the active explorer, represented by [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), nor the set of selected items indicates the type of the items that are selected.</span></span> <span data-ttu-id="d3f88-108">In der Regel müssen Sie zunächst den Elementtyp identifizieren und dann die spezifische **Display**-Methode für diesen Typ aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d3f88-108">Normally, you would have to first identify the item type and then call the specific **Display** method for that type.</span></span> <span data-ttu-id="d3f88-109">Da die **Display**-Methode für alle Outlook-Elementobjekte gleich ist und die OutlookItem-Hilfsklasse diese Methode enthält, können Sie die Hilfsklasse nutzen, indem Sie eine Instanz des OutlookItem-Objekts (myItem) deklarieren und myItem.Display zum Anzeigen der jeweiligen Elemente in der Auswahl verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3f88-109">Because the **Display** method is common to all Outlook items objects and the OutlookItem helper class includes this method, you can take advantage of the helper class, by declaring an instance of the OutlookItem object, myItem, and using myItem.Display to display each item in the selection.</span></span> <span data-ttu-id="d3f88-110">Informationen zur Implementierung der OutlookItem-Hilfsklasse finden Sie unter [Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)</span><span class="sxs-lookup"><span data-stu-id="d3f88-110">You can see the implementation of the OutlookItem helper class in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)</span></span>

<span data-ttu-id="d3f88-111">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="d3f88-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="d3f88-112">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d3f88-112">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="d3f88-113">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="d3f88-113">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySelectedItems()
{
    Outlook.Selection selection =
        Application.ActiveExplorer().Selection;
    for (int i = 1; i <= selection.Count; i++)
    {
        OutlookItem myItem = new OutlookItem(selection[i]);
        myItem.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="d3f88-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3f88-114">See also</span></span>

- [<span data-ttu-id="d3f88-115">Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen</span><span class="sxs-lookup"><span data-stu-id="d3f88-115">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="d3f88-116">Allgemeine Outlook-Elemente</span><span class="sxs-lookup"><span data-stu-id="d3f88-116">General Outlook items</span></span>](general-outlook-items.md)

