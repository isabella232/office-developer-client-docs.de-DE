---
title: Abonnieren eines RSS-Feeds
TOCTitle: Subscribe to an RSS feed
ms:assetid: 7ecefbcd-1a34-48e8-afac-7d54e79fd159
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424473(v=office.15)
ms:contentKeyID: 55119852
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b92c733c5030ce12eb691bba57afb5ce6b9d1dad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335399"
---
# <a name="subscribe-to-an-rss-feed"></a><span data-ttu-id="8b4b2-102">Abonnieren eines RSS-Feeds</span><span class="sxs-lookup"><span data-stu-id="8b4b2-102">Subscribe to an RSS feed</span></span>

<span data-ttu-id="8b4b2-103">In diesem Beispiel wird veranschaulicht, wie Sie einen RSS-Feed mit der [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\))-Methode abonnieren.</span><span class="sxs-lookup"><span data-stu-id="8b4b2-103">This example shows how to subscribe to an RSS feed by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="8b4b2-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8b4b2-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="8b4b2-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="8b4b2-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="8b4b2-p101">Das Outlook-Objektmodell unterstützt das Bereitstellen von Zugriff auf freigegebene Daten, z. B. Internetkalender, RSS-Feeds und Daten aus Microsoft SharePoint-Listen und -Dokumentbibliotheken. Es ermöglicht das Herstellen von Verbindungen zu diesen gemeinsam genutzten Datenquellen und das Einrichten der Synchronisierungskontexte, sodass diese die freigegebenen Ressourcen kontinuierlich abfragen. Das Outlook-Objektmodell bietet die [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) -Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts zum Herunterladen und Synchronisieren mit einem bestimmten Typ von freigegebenem Ordner.</span><span class="sxs-lookup"><span data-stu-id="8b4b2-p101">The Outlook object model supports providing access to shared data, such as Internet calendars, RSS feeds, and data from Microsoft SharePoint lists and document libraries. It enables connecting to these shared sources of data and setting up the synchronization contexts to continue to poll those shared resources. The Outlook object model provides the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to download and synchronize with a particular type of shared folder.</span></span>

<span data-ttu-id="8b4b2-p102">Im folgenden Beispiel abonniert AddRssFeed einen neuen RSS-Feed namens “Example RSS Feed” durch Aufrufen der **OpenSharedFolder**-Methode mit einer URL, die auf den neuen RSS-Feed verweist. Die letzten beiden Parameter der **OpenSharedFolder**-Methode sind auf **true** festgelegt, um anzugeben, dass Anlagen heruntergeladen werden sollen und von Outlook die im RSS-Feed bereitgestellte Aktualisierungsrate verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b4b2-p102">In the following example, AddRssFeed subscribes to a new RSS feed named “Example RSS Feed” by calling the **OpenSharedFolder** method with a URL that refers to the new RSS feed. The last two parameters of **OpenSharedFolder** method are set to **true** to indicate that attachments should be downloaded, and Outlook should use the refresh ratio provided in the RSS feed.</span></span>


> [!NOTE]
> <span data-ttu-id="8b4b2-111">Sie müssen den korrekten Protokollhandler für die Ordner-URL in der **OpenSharedFolder**-Methode angeben, um einen RSS-Feed zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="8b4b2-111">You must specify the correct protocol handler for the folder URL in the **OpenSharedFolder** method to subscribe to an RSS feed.</span></span> <span data-ttu-id="8b4b2-112">Sie müssen z. B. eine URL verwenden, die mit `feed://` anstelle von `https://` beginnt.</span><span class="sxs-lookup"><span data-stu-id="8b4b2-112">For example, you must use a URL that begins with `feed://` instead of `https://`.</span></span> <span data-ttu-id="8b4b2-113">Outlook kann keine RSS-Feeds öffnen, die eine Authentifizierung erfordern, es sei denn, die Windows NTLM-Authentifizierung (Windows NT LAN Manager) ist verfügbar. Außerdem können keine RSS-Feeds von SSL-Speicherorten (Secure Sockets Layer) geladen werden.</span><span class="sxs-lookup"><span data-stu-id="8b4b2-113">Outlook cannot open RSS feeds that require authentication unless Windows NT LAN Manager (NTLM) authentication is available, and it cannot load RSS feeds from Secure Sockets Layer (SSL) locations.</span></span>

<span data-ttu-id="8b4b2-114">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="8b4b2-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="8b4b2-115">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8b4b2-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="8b4b2-116">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="8b4b2-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddRssFeed()
{
    string feedUrl = "feed://example.org/rssfeed.xml";
    Outlook.Folder subscriptionFolder =
        Application.Session.OpenSharedFolder(feedUrl, "Example RSS Feed", true, true) as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(subscriptionFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a><span data-ttu-id="8b4b2-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b4b2-117">See also</span></span>

- [<span data-ttu-id="8b4b2-118">Gruppenfreigabe</span><span class="sxs-lookup"><span data-stu-id="8b4b2-118">Group sharing</span></span>](group-sharing.md)

