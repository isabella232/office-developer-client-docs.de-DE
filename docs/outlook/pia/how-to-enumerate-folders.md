---
title: Aufzählen von Ordnern
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 91165754ccd86ebff07ec99e60f0ad1a167dea05
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406253"
---
# <a name="enumerate-folders"></a><span data-ttu-id="0b204-102">Aufzählen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="0b204-102">Enumerate folders</span></span>

<span data-ttu-id="0b204-103">In diesem Beispiel wird gezeigt, wie Ordner durch das Durchlaufen einer Sammlung von Ordnern aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0b204-103">This example shows how to enumerate folders by iterating through a collection of folders.</span></span>

## <a name="example"></a><span data-ttu-id="0b204-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0b204-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0b204-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0b204-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="0b204-106">Im folgenden Codebeispiel wird durch die EnumerateFoldersInDefaultStore-Methode zuerst der Stammordner des Standardspeichers mithilfe der [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\))-Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0b204-106">In the following code example, the   method first obtains the root folder for the default store by using the GetRootFolder() method.</span></span> <span data-ttu-id="0b204-107">Dann folgt der Aufruf der EnumerateFolders-Methode über den Stammordner.</span><span class="sxs-lookup"><span data-stu-id="0b204-107">It then calls the   method on the root folder.</span></span> <span data-ttu-id="0b204-108">EnumerateFolders übernimmt einen Stammordner und durchläuft die Ordner des Standardspeichers, den der Stammordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b204-108"> takes in a root folder and walks through the folders of the default store that the root folder represents.</span></span> <span data-ttu-id="0b204-109">EnumerateFolders verwendet zuerst die [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\))-Eigenschaft zum Abrufen der Unterordner des [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekts des Stamms.</span><span class="sxs-lookup"><span data-stu-id="0b204-109"> first uses the Folders property to obtain the subfolders of the root Folder object.</span></span> <span data-ttu-id="0b204-110">EnumerateFolders wird dann rekursiv aufgerufen, um alle Ordner der Hierarchie aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="0b204-110"> is then called recursively to enumerate all the folders in a hierarchy.</span></span> <span data-ttu-id="0b204-111">Abschließend schreibt EnumerateFolders die [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\))-Eigenschaft aller **Folder** in die Ablaufverfolgungslistener der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="0b204-111">Finally,   writes the FolderPath property of each Folder to the trace listeners in the Listeners collection.</span></span>

<span data-ttu-id="0b204-112">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="0b204-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="0b204-113">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0b204-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="0b204-114">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="0b204-114">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="0b204-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b204-115">See also</span></span>

- [<span data-ttu-id="0b204-116">Ordner</span><span class="sxs-lookup"><span data-stu-id="0b204-116">Folders</span></span>](folders.md)

