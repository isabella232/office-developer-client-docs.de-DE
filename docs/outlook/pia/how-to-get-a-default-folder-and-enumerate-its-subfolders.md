---
title: Abrufen eines Standardordners und Auflisten seiner Unterordner
TOCTitle: Get a default folder and enumerate its subfolders
ms:assetid: 587e8392-cb03-442c-9058-1282f36dabdb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184610(v=office.15)
ms:contentKeyID: 55119857
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 934b5f823127fde9fbbd3a49f41cedb791277e7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407401"
---
# <a name="get-a-default-folder-and-enumerate-its-subfolders"></a><span data-ttu-id="1981f-102">Abrufen eines Standardordners und Auflisten seiner Unterordner</span><span class="sxs-lookup"><span data-stu-id="1981f-102">Get a default folder and enumerate its subfolders</span></span>

<span data-ttu-id="1981f-103">In diesem Beispiel wird gezeigt, wie ein Standardordner im Standardspeicher des Benutzers abgerufen und dessen Unterordner aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="1981f-103">This example shows how to obtain a default folder in the user’s default store and enumerate its subfolders.</span></span>

## <a name="example"></a><span data-ttu-id="1981f-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1981f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1981f-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="1981f-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="1981f-106">Im folgenden Codebeispiel verwendet GetRSSFeeds die [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\))-Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts zum Abrufen des Stammordners für RSS Feeds des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1981f-106">In the following code example,   uses the GetDefaultFolder(OlDefaultFolders) method of the NameSpace object to obtain the user's RSS Feeds root folder.</span></span> <span data-ttu-id="1981f-107">Von GetRSSFeeds wird dann ein Meldungsfeld mit den Ordnernamen für alle RSS Feeds im Stammordner für RSS Feeds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1981f-107"> then displays a message box that contains the folder names for all RSS feeds in the RSS Feeds folder.</span></span>

<span data-ttu-id="1981f-108">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="1981f-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="1981f-109">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1981f-109">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="1981f-110">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="1981f-110">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetRSSFeeds()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderRssFeeds)
        as Outlook.Folder;
    if (folder != null)
    {
        if (folder.Folders.Count > 0)
        {
            StringBuilder sb = new StringBuilder();
            foreach (Outlook.Folder subfolder
                in folder.Folders)
            {
                sb.AppendLine(subfolder.Name);
            }
            MessageBox.Show(sb.ToString(),
                "RSS Feeds",
                MessageBoxButtons.OK,
                MessageBoxIcon.Information);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="1981f-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1981f-111">See also</span></span>

- [<span data-ttu-id="1981f-112">Ordner</span><span class="sxs-lookup"><span data-stu-id="1981f-112">Folders</span></span>](folders.md)

