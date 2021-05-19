---
title: Aufzählen von Ordnern
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fe79f78ba1aab1e54df0b0bc88fa0c55c73e187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357400"
---
# <a name="enumerate-folders"></a><span data-ttu-id="5cb55-102">Aufzählen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="5cb55-102">Enumerate folders</span></span>

<span data-ttu-id="5cb55-103">In diesem Beispiel wird gezeigt, wie Ordner durch das Durchlaufen einer Sammlung von Ordnern aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5cb55-103">This example shows how to enumerate folders by iterating through a collection of folders.</span></span>

## <a name="example"></a><span data-ttu-id="5cb55-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5cb55-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="5cb55-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="5cb55-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="5cb55-106">Im folgenden Codebeispiel wird durch die EnumerateFoldersInDefaultStore-Methode zuerst der Stammordner des Standardspeichers mithilfe der [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\))-Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5cb55-106">In the following code example, the EnumerateFoldersInDefaultStore method first obtains the root folder for the default store by using the [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) method.</span></span> <span data-ttu-id="5cb55-107">Dann folgt der Aufruf der EnumerateFolders-Methode über den Stammordner.</span><span class="sxs-lookup"><span data-stu-id="5cb55-107">It then calls the EnumerateFolders method on the root folder.</span></span> <span data-ttu-id="5cb55-108">EnumerateFolders übernimmt einen Stammordner und durchläuft die Ordner des Standardspeichers, den der Stammordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="5cb55-108">EnumerateFolders takes in a root folder and walks through the folders of the default store that the root folder represents.</span></span> <span data-ttu-id="5cb55-109">EnumerateFolders verwendet zuerst die [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\))-Eigenschaft zum Abrufen der Unterordner des [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekts des Stamms.</span><span class="sxs-lookup"><span data-stu-id="5cb55-109">EnumerateFolders first uses the [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) property to obtain the subfolders of the root [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span> <span data-ttu-id="5cb55-110">EnumerateFolders wird dann rekursiv aufgerufen, um alle Ordner der Hierarchie aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="5cb55-110">EnumerateFolders is then called recursively to enumerate all the folders in a hierarchy.</span></span> <span data-ttu-id="5cb55-111">Abschließend schreibt EnumerateFolders die [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\))-Eigenschaft aller **Folder** in die Ablaufverfolgungslistener der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="5cb55-111">Finally, EnumerateFolders writes the [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) property of each **Folder** to the trace listeners in the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="5cb55-112">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="5cb55-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="5cb55-113">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5cb55-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5cb55-114">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="5cb55-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateFoldersInDefaultStore()
{
    Outlook.Folder root =
        Application.Session.
        DefaultStore.GetRootFolder() as Outlook.Folder;
    EnumerateFolders(root);
}

// Uses recursion to enumerate Outlook subfolders.
private void EnumerateFolders(Outlook.Folder folder)
{
    Outlook.Folders childFolders =
        folder.Folders;
    if (childFolders.Count > 0)
    {
        foreach (Outlook.Folder childFolder in childFolders)
        {
            // Write the folder path.
            Debug.WriteLine(childFolder.FolderPath);
            // Call EnumerateFolders using childFolder.
            EnumerateFolders(childFolder);
        }
    }
}               
```

## <a name="see-also"></a><span data-ttu-id="5cb55-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cb55-115">See also</span></span>

- [<span data-ttu-id="5cb55-116">Folders</span><span class="sxs-lookup"><span data-stu-id="5cb55-116">Folders</span></span>](folders.md)

