---
title: Auswählen eines Ordners und Anzeigen von Ordnerinformationen
TOCTitle: Select a folder and display folder information
ms:assetid: 737b19bc-1efd-4ddb-86d0-72b3ab8eaf8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184616(v=office.15)
ms:contentKeyID: 55119859
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41dc96f26e7e0040467096731cb16ae7c0c08f74
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721937"
---
# <a name="select-a-folder-and-display-folder-information"></a><span data-ttu-id="32178-102">Auswählen eines Ordners und Anzeigen von Ordnerinformationen</span><span class="sxs-lookup"><span data-stu-id="32178-102">Select a folder and display folder information</span></span>

<span data-ttu-id="32178-103">Dieses Beispiel zeigt, wie Informationen zu einem Ordner, den ein Benutzer aus einer Liste angegebener Ordner auswählt, programmgesteuert angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="32178-103">This example shows how to programmatically display information about a folder that a user selects from a specified folder list.</span></span>

## <a name="example"></a><span data-ttu-id="32178-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="32178-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="32178-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="32178-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="32178-106">Im folgenden Codebeispiel verwendet ShowFolderInfo die [PickFolder()](https://msdn.microsoft.com/library/bb623484\(v=office.15\))-Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts zum Anzeigen des Dialogfeldes **Ordner auswählen**, damit der Benutzer einen Ordner auswählt.</span><span class="sxs-lookup"><span data-stu-id="32178-106">In the following code example, ShowFolderInfo uses the [PickFolder()](https://msdn.microsoft.com/library/bb623484\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to display a **Select Folder** dialog box to the user, and waits for the user to select a folder.</span></span> <span data-ttu-id="32178-107">Nach Auswahl des Ordners werden die folgenden Eigenschaften angezeigt: [EntryID](https://msdn.microsoft.com/library/bb646192\(v=office.15\)), [StoreID](https://msdn.microsoft.com/library/bb612609\(v=office.15\)), [UnReadItemCount](https://msdn.microsoft.com/library/bb610138\(v=office.15\)), [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)), [CurrentView](https://msdn.microsoft.com/library/bb612411\(v=office.15\)), [Name](https://msdn.microsoft.com/library/bb623727\(v=office.15\)) und [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="32178-107">Once the user selects a folder, its [EntryID](https://msdn.microsoft.com/library/bb646192\(v=office.15\)), [StoreID](https://msdn.microsoft.com/library/bb612609\(v=office.15\)), [UnReadItemCount](https://msdn.microsoft.com/library/bb610138\(v=office.15\)), [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)), [CurrentView](https://msdn.microsoft.com/library/bb612411\(v=office.15\)), [Name](https://msdn.microsoft.com/library/bb623727\(v=office.15\)), and [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) properties are displayed.</span></span> <span data-ttu-id="32178-108">Anschließend ruft das Beispiel die [GetFolderFromID](https://msdn.microsoft.com/library/bb647784\(v=office.15\))-Methode zum Erstellen eines neuen [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekts und zum Anzeigen des Ordners auf.</span><span class="sxs-lookup"><span data-stu-id="32178-108">The example then calls the [GetFolderFromID](https://msdn.microsoft.com/library/bb647784\(v=office.15\)) method to create a new [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object and display the folder.</span></span>

<span data-ttu-id="32178-109">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="32178-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="32178-110">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="32178-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="32178-111">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="32178-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ShowFolderInfo()
{
    Outlook.Folder folder =
        Application.Session.PickFolder()
        as Outlook.Folder;
    if (folder != null)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Folder EntryID:");
        sb.AppendLine(folder.EntryID);
        sb.AppendLine();
        sb.AppendLine("Folder StoreID:");
        sb.AppendLine(folder.StoreID);
        sb.AppendLine();
        sb.AppendLine("Unread Item Count: "
            + folder.UnReadItemCount);
        sb.AppendLine("Default MessageClass: "
            + folder.DefaultMessageClass);
        sb.AppendLine("Current View: "
            + folder.CurrentView.Name);
        sb.AppendLine("Folder Path: "
            + folder.FolderPath);
        MessageBox.Show(sb.ToString(),
            "Folder Information",
            MessageBoxButtons.OK,
            MessageBoxIcon.Information);
        Outlook.Folder folderFromID =
            Application.Session.GetFolderFromID(
            folder.EntryID, folder.StoreID)
            as Outlook.Folder;
        folderFromID.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="32178-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32178-112">See also</span></span>

- [<span data-ttu-id="32178-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="32178-113">Folders</span></span>](folders.md)

