---
title: Abonnieren eines RSS-Feeds
TOCTitle: Subscribe to an RSS feed
ms:assetid: 7ecefbcd-1a34-48e8-afac-7d54e79fd159
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424473(v=office.15)
ms:contentKeyID: 55119852
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4f6f2067605208966d095a83137947dd9232b6a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583107"
---
# <a name="subscribe-to-an-rss-feed"></a>Abonnieren eines RSS-Feeds

In diesem Beispiel wird veranschaulicht, wie Sie einen RSS-Feed mit der [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\))-Methode abonnieren.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Das Outlook-Objektmodell unterstützt das Bereitstellen von Zugriff auf freigegebene Daten, z. B. Internetkalender, RSS-Feeds und Daten aus Microsoft SharePoint-Listen und -Dokumentbibliotheken. Es ermöglicht das Herstellen von Verbindungen zu diesen gemeinsam genutzten Datenquellen und das Einrichten der Synchronisierungskontexte, sodass diese die freigegebenen Ressourcen kontinuierlich abfragen. Das Outlook-Objektmodell bietet die [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) -Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts zum Herunterladen und Synchronisieren mit einem bestimmten Typ von freigegebenem Ordner.

Im folgenden Beispiel abonniert AddRssFeed einen neuen RSS-Feed namens “Example RSS Feed” durch Aufrufen der **OpenSharedFolder**-Methode mit einer URL, die auf den neuen RSS-Feed verweist. Die letzten beiden Parameter der **OpenSharedFolder**-Methode sind auf **true** festgelegt, um anzugeben, dass Anlagen heruntergeladen werden sollen und von Outlook die im RSS-Feed bereitgestellte Aktualisierungsrate verwendet werden soll.


> [!NOTE]
> Sie müssen den korrekten Protokollhandler für die Ordner-URL in der **OpenSharedFolder**-Methode angeben, um einen RSS-Feed zu abonnieren. Sie müssen z. B. eine URL verwenden, die mit `feed://` anstelle von `https://` beginnt. Outlook kann keine RSS-Feeds öffnen, die eine Authentifizierung erfordern, es sei denn, die Windows NTLM-Authentifizierung (Windows NT LAN Manager) ist verfügbar. Außerdem können keine RSS-Feeds von SSL-Speicherorten (Secure Sockets Layer) geladen werden.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Gruppenfreigabe](group-sharing.md)

