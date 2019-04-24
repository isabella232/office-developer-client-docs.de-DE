---
title: Hinzufügen eines Ordners zur Ordnerliste
TOCTitle: Add a folder to the folder list
ms:assetid: f636a190-d966-4421-9977-0ead2bff5eee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184655(v=office.15)
ms:contentKeyID: 55119850
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 27a9efb76fdbb1c6ac6b0b57e874ca59d002b928
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321329"
---
# <a name="add-a-folder-to-the-folder-list"></a><span data-ttu-id="a8676-102">Hinzufügen eines Ordners zur Ordnerliste</span><span class="sxs-lookup"><span data-stu-id="a8676-102">Add a folder to the folder list</span></span>

<span data-ttu-id="a8676-103">In diesem Beispiel wird die Verwendung der [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\))-Methode erläutert, um einen Ordner zur Ordnerliste von Outlook hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a8676-103">This example shows how to use the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add a folder to the Outlook folder list.</span></span>

## <a name="example"></a><span data-ttu-id="a8676-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a8676-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a8676-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="a8676-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="a8676-106">Im folgenden Codebeispiel ruft **AddMyNewFolder** die **Add**-Methode der [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\))-Auflistung auf, um dem [Posteingang](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) in der Outlook-Ordnerliste ein **Folder**-Objekt hinzuzufügen, das einen Ordner namens „My New Folder“ darstellt.</span><span class="sxs-lookup"><span data-stu-id="a8676-106">In the following code example, **AddMyNewFolder** calls the **Add** method of the [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) collection to add a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that represents a folder called “My New Folder” to the **Inbox** in the Outlook folder list.</span></span> <span data-ttu-id="a8676-107">„My New Folder“ wird anschließend angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8676-107">“My New Folder” is then displayed.</span></span>

<span data-ttu-id="a8676-108">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="a8676-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a8676-109">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a8676-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a8676-110">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a8676-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddMyNewFolder()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Folders folders = folder.Folders;
    try
    {
        Outlook.Folder newFolder = folders.Add(
            "My New Folder", Type.Missing)
            as Outlook.Folder;
        newFolder.Display();
    }
    catch
    {
        MessageBox.Show(
            "Could not add 'My New Folder'",
            "Add Folder",
            MessageBoxButtons.OK,
            MessageBoxIcon.Error);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="a8676-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8676-111">See also</span></span>

- [<span data-ttu-id="a8676-112">Folders</span><span class="sxs-lookup"><span data-stu-id="a8676-112">Folders</span></span>](folders.md)

