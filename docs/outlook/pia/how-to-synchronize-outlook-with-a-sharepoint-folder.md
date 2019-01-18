---
title: Synchronisieren von Outlook mit einem SharePoint-Ordner
TOCTitle: Synchronize Outlook with a SharePoint folder
ms:assetid: fecb04ab-39c6-43e1-9a21-12ecb29d94fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424483(v=office.15)
ms:contentKeyID: 55119853
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b6c88d40236ffb6cc3201b659a39e4d869de188
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718714"
---
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a><span data-ttu-id="f5579-102">Synchronisieren von Outlook mit einem SharePoint-Ordner</span><span class="sxs-lookup"><span data-stu-id="f5579-102">Synchronize Outlook with a SharePoint folder</span></span>

<span data-ttu-id="f5579-103">In diesem Beispiel wird veranschaulicht, wie programmgesteuert eine Verbindung zwischen Outlook und einem SharePoint-Ordner hergestellt und die Ordnerinhalte synchronisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="f5579-103">This example shows how to programmatically connect Outlook with a SharePoint folder and to synchronize the folder contents.</span></span>

## <a name="example"></a><span data-ttu-id="f5579-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f5579-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f5579-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="f5579-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="f5579-106">In Outlook können Sie Kalender, Kontaktlisten, Aufgabenlisten, Diskussionsrunden und Dokumentbibliotheken mit SharePoint-Ordnern synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f5579-106">In Outlook, you can synchronize calendars, contact lists, task lists, discussion boards, and document libraries to SharePoint folders.</span></span> <span data-ttu-id="f5579-107">Basierend auf der URL, die bei der Synchronisierung angegeben wurde, erstellt Outlook einen neuen Ordner vom gleichen Basistyp wie der SharePoint-Ordner.</span><span class="sxs-lookup"><span data-stu-id="f5579-107">Based on the URL provided upon synchronization, Outlook will create a new folder of the same base type as the SharePoint folder.</span></span> <span data-ttu-id="f5579-108">Beim Synchronisieren mit einem SharePoint-Kalenderordner zum Beispiel wird eine neuer Kalenderordner in Outlook erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5579-108">For example, synchronizing to a SharePoint calendar folder will create a new calendar folder in Outlook.</span></span> <span data-ttu-id="f5579-109">SharePoint-Synchronisierungsordner werden in eigenen persönlichen Outlook-Ordnern (PST-Datei) außerhalb des Benutzerpostfachs gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f5579-109">SharePoint synchronization folders are stored in their own Outlook Personal Folders (.pst) file outside of the user’s mailbox.</span></span> <span data-ttu-id="f5579-110">Sie können eine Verbindung mit einem SharePoint-Ordner mit der [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\))-Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts herstellen.</span><span class="sxs-lookup"><span data-stu-id="f5579-110">You can connect to a SharePoint folder by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="f5579-111">Beachten Sie, dass Sie eine stssync://-URL verwenden müssen, die Details zum SharePoint-Server, Ordnerpfad und andere Informationen bereitstellt, die Outlook zum Öffnen eines SharePoint-Ordners benötigt.</span><span class="sxs-lookup"><span data-stu-id="f5579-111">Note that you must use a stssync:// URL that provides details about the SharePoint server, folder path, and other information that Outlook needs to open a SharePoint folder.</span></span>

<span data-ttu-id="f5579-112">Wenn Sie programmgesteuert eine Verbindung zu einem SharePoint-Ordner herstellen, müssen Sie die richtige URL ermitteln, die zum Erstellen der Freigabebeziehung zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="f5579-112">When connecting to a SharePoint folder programmatically, you must determine the proper URL to use to create the sharing relationship.</span></span> <span data-ttu-id="f5579-113">Da die stssync://-URL für den Ordner nicht auf der SharePoint-Benutzeroberfläche bereitgestellt wird, müssen Sie den Zielordner in Outlook manuell verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="f5579-113">Because the stssync:// URL is not provided in the SharePoint user interface for the folder, manually link the destination folder into Outlook.</span></span> <span data-ttu-id="f5579-114">Verwenden Sie dann das erste Verfahren, DisplaySharePointUrl, im folgenden Codebeispiel, um die richtige URL abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f5579-114">Then use the first procedure, DisplaySharePointUrl, in the following code example, to get the correct URL.</span></span> <span data-ttu-id="f5579-115">DisplaySharePointUrl verwendet das [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt, um nach Freigabebindungsinformationen im aktuellen Ordner für das aktive Explorer-Fenster zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f5579-115">DisplaySharePointUrl uses the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object to look for the sharing binding information in the current folder for the active explorer window.</span></span> <span data-ttu-id="f5579-116">Wenn eine oder mehrere Bindungskontexte gefunden werden, werden die URLs für alle verfügbaren Freigabekontexte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5579-116">If one or more binding contexts are found, the URLs for all available sharing contexts will be displayed.</span></span>

<span data-ttu-id="f5579-117">Jetzt haben Sie die richtige URL zum Erstellen der Freigabebeziehung.</span><span class="sxs-lookup"><span data-stu-id="f5579-117">Now you have the proper URL to create the sharing relationship.</span></span> <span data-ttu-id="f5579-118">Um den neuen SharePoint-Ordner in Outlook zu synchronisieren, kopieren Sie die URL und fügen Sie sie in die Zuweisung der Zeichenfolgenvariable „CalendarUrl“ in dem zweiten Verfahren „AddSpsFolder“.</span><span class="sxs-lookup"><span data-stu-id="f5579-118">To synchronize the new SharePoint folder in Outlook, copy and paste the URL to the assignment of the string variable calendarUrl in the second procedure, AddSpsFolder.</span></span> <span data-ttu-id="f5579-119">AddSpsFolder automatisiert die Synchronisierung des neuen SharePoint-Ordners in Outlook, indem die **NameSpace.OpenSharedFolder**-Methode mit einer `stssync://`-URL (in diesem Fall die URL, die im DisplaySharePointUrl-Verfahren generiert wurde) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f5579-119">AddSpsFolder automates the synchronization of the new SharePoint folder in Outlook by using the **NameSpace.OpenSharedFolder** method with a `stssync://` URL (in this case, the URL produced by the DisplaySharePointUrl procedure).</span></span> <span data-ttu-id="f5579-120">AddSpsFolder bietet auch einen benutzerdefinierten Ordnernamen „Example SPS Calendar“ und weist Outlook an, die standardmäßige Gültigkeitsdauer (Time to Live, TTL) für den Ordner zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5579-120">AddSpsFolderalso provides a custom folder name, “Example SPS Calendar”, and specifies Outlook to use the default Time to Live (TTL) for the folder.</span></span> <span data-ttu-id="f5579-121">SharePoint-Ordner laden immer Elementanlagen herunter, daher müssen Sie dies hier nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="f5579-121">SharePoint folders always download item attachments, so you do not have to specify that here.</span></span>

<span data-ttu-id="f5579-122">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="f5579-122">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="f5579-123">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f5579-123">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="f5579-124">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="f5579-124">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySharePointUrl()
{
    const string PROP_SYNC_URL = 
        "https://schemas.microsoft.com/mapi/id/{00062040-0000-0000-C000-000000000046}/8A24001E";

    Outlook.Folder folder = Application.ActiveExplorer().CurrentFolder as Outlook.Folder;
    Outlook.Table table = folder.GetTable(Type.Missing, Outlook.OlTableContents.olHiddenItems);
    table.Columns.RemoveAll();
    table.Columns.Add("MessageClass");
    table.Columns.Add(PROP_SYNC_URL);

    StringBuilder sb = new StringBuilder();
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        string msgClass, spsUrl;
        msgClass = row["MessageClass"] as string;
        spsUrl = row[PROP_SYNC_URL] as string;

        if (msgClass == "IPM.Sharing.Binding.In")
        {
            sb.Append(spsUrl);
            sb.Append("\r\n");
        }
    }
    if (sb.Length > 0)
    {
        System.Windows.Forms.MessageBox.Show(
            "The following SharePoint Folder URLs were found:\r\n" + sb.ToString());
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("No SharePoint URLs were found in this folder.");
    }
}

private void AddSpsFolder()
{
    string calendarUrl = "stssync://sts/?ver=1.1&type=calendar&cmd=add-folder&base-url=
        https://example.org/calendar&list-url=/Lists/Calendar/calendar.aspx&guid=&site-name=
        Example%20Site&list-name=Calendar";
    string folderName = "Example SPS Calendar";
    bool useDefaultTTL = true;
    Outlook.Folder calendarFolder =
        Application.Session.OpenSharedFolder(calendarUrl, folderName, Type.Missing, useDefaultTTL) 
        as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(calendarFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a><span data-ttu-id="f5579-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5579-125">See also</span></span>

- [<span data-ttu-id="f5579-126">Gruppenfreigabe</span><span class="sxs-lookup"><span data-stu-id="f5579-126">Group sharing</span></span>](group-sharing.md)

