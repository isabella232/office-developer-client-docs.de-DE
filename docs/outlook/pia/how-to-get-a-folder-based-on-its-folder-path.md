---
title: Abrufen eines Ordners basierend auf seinem Ordnerpfad
TOCTitle: Get a folder based on its folder path
ms:assetid: 613f2209-667c-48f0-82cf-86e3c9a24cb4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184612(v=office.15)
ms:contentKeyID: 55119858
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fed1e7eb39f31ddd4340fc82a16e31ec67523a9d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320286"
---
# <a name="get-a-folder-based-on-its-folder-path"></a><span data-ttu-id="7a630-102">Abrufen eines Ordners basierend auf seinem Ordnerpfad</span><span class="sxs-lookup"><span data-stu-id="7a630-102">Get a folder based on its folder path</span></span>

<span data-ttu-id="7a630-103">In diesem Beispiel wird ein Ordnerpfad verwendet und der zugehörige Ordner abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7a630-103">This example takes a folder path and obtains the associated folder.</span></span>

## <a name="example"></a><span data-ttu-id="7a630-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7a630-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7a630-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="7a630-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="7a630-106">Im folgenden Codebeispiel verwendet die GetKeyContacts-Methode die [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\))-Eigenschaft zum Abrufen des Ordnerpfads des Ordners "Kontakte\\Wichtige Kontakte".</span><span class="sxs-lookup"><span data-stu-id="7a630-106">In the following code example, the GetKeyContacts method uses the [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) property to obtain the folder path of the Contacts\\Key Contacts folder.</span></span> <span data-ttu-id="7a630-107">Die GetFolder-Methode wird dann mithilfe der [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\))-Eigenschaft als Argument aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7a630-107">The GetFolder method is then called by using the [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) property as the argument.</span></span> <span data-ttu-id="7a630-108">Wenn GetFolder einen Ordner zurückgibt, wird eine Meldung angezeigt, die besagt, dass die wichtigen Kontakte gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="7a630-108">If GetFolder returns a folder, a message will appear saying the Key Contacts are found.</span></span> <span data-ttu-id="7a630-109">Die GetFolder-Methode übernimmt den Pfad zum Ordner und gibt das richtige [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="7a630-109">The GetFolder method takes in a path to a folder and returns the correct [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span> <span data-ttu-id="7a630-110">Hierzu wird die **FolderPath**-Eigenschaft in einen string-Array geteilt und dieser dazu verwendet, das richtige **Folder**-Objekt zu finden, indem die **FolderPath**-Eigenschaft von oben an durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="7a630-110">This is done by first splitting the **FolderPath** property into a string array and then using the array to find the correct **Folder** object starting from the top of the **FolderPath** property.</span></span> <span data-ttu-id="7a630-111">Wenn der angegebene Ordner nicht gefunden wird, gibt GetFolder einen Null-Verweis zurück.</span><span class="sxs-lookup"><span data-stu-id="7a630-111">If the specified folder is not found, GetFolder returns a null reference.</span></span>

<span data-ttu-id="7a630-112">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="7a630-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7a630-113">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7a630-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7a630-114">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="7a630-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetKeyContacts()
{
    string folderPath =
        Application.Session.
        DefaultStore.GetRootFolder().FolderPath
        + @"\Contacts\Key Contacts";
    Outlook.Folder folder = GetFolder(folderPath);
    if (folder != null)
    {
        //Work with folder here
        Debug.WriteLine("Found Key Contacts");
    }
}

// Returns Folder object based on folder path
private Outlook.Folder GetFolder(string folderPath)
{
    Outlook.Folder folder;
    string backslash = @"\";
    try
    {
        if (folderPath.StartsWith(@"\\"))
        {
            folderPath = folderPath.Remove(0, 2);
        }
        String[] folders =
            folderPath.Split(backslash.ToCharArray());
        folder =
            Application.Session.Folders[folders[0]]
            as Outlook.Folder;
        if (folder != null)
        {
            for (int i = 1; i <= folders.GetUpperBound(0); i++)
            {
                Outlook.Folders subFolders = folder.Folders;
                folder = subFolders[folders[i]]
                    as Outlook.Folder;
                if (folder == null)
                {
                    return null;
                }
            }
        }
        return folder;
    }
    catch { return null; }
}        
```

## <a name="see-also"></a><span data-ttu-id="7a630-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a630-115">See also</span></span>

- [<span data-ttu-id="7a630-116">Folders</span><span class="sxs-lookup"><span data-stu-id="7a630-116">Folders</span></span>](folders.md)

