---
title: Verwenden der Sofortsuche zum Durchsuchen aller Ordner und aller Stores nach einem Ausdruck im Betreff
TOCTitle: Use instant search to search all folders and all stores for a phrase in the subject
ms:assetid: d3152bfa-6e7d-4b68-8c7e-e2e155a92b49
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424478(v=office.15)
ms:contentKeyID: 55119923
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 07b0ba7a1d488dc1c7e1fcf0e9ae487b04b88755
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709439"
---
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a>Verwenden der Sofortsuche zum Durchsuchen aller Ordner und aller Stores nach einem Ausdruck im Betreff

In diesem Beispiel werden mithilfe der Sofortsuche alle Ordner und alle Speicher nach einem Ausdruck im Betreff durchsucht und die gefundenen Elemente anschließend in einem Explorer-Fenster angezeigt.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Die Sofortsuche ist ein Feature von Microsoft Outlook, mit dem durch Ausgeben von Abfragen, die Ergebnisse basierend auf dem Inhalt zurückgeben, Suchvorgänge ausführen können. Nachdem die Abfrage verarbeitet wurde, können die Ergebnisse in einer Vielzahl von Objekten zurückgegeben werden, einschließlich des [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekts, der [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\))-Auflistung und des [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\))-Objekts. Sie können Code mithilfe der Advanced Query Syntax (AQS), die von der Microsoft Windows-Desktopsuche angeboten wird, Code schreiben, der die Sofortsuche verwendet. AQS ist eine der drei Abfragesprachen, die Outlook unterstützt. Sie ist leistungsstark, aber beschränkt auf die [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\))-Methode des [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\))-Objekts. Sie können AQS nicht verwenden, um eine Einschränkung für **Table**- oder **Item**-Objekte bereitzustellen. Außerdem können die von einer AQS-Abfrage zurückgegebenen Ergebnisse nur in der Outlook-Benutzeroberfläche zurückgegeben werden. In der folgenden Tabelle sind die drei Abfragesprachen aufgeführt, die Outlook unterstützt. In diesem Thema wird jedoch nur die Verwendung von AQS veranschaulicht.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Abfragesprache</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AQS</p></td>
<td><p>AQS wird von der Windows-Desktopsuche verwendet und ist die Abfragesprache für das Feature Sofortsuche in Outlook.</p></td>
</tr>
<tr class="even">
<td><p>DASL</p></td>
<td><p>Die Abfragesprache DAV Search and Locating (DASL) basiert auf der Microsoft Exchange-Implementierung von DASL in Outlook. Mit DASL können Ergebnisse im <b>Table</b>-Objekt zurückgegeben werden. </p></td>
</tr>
<tr class="odd">
<td><p>Jet</p></td>
<td><p>Die Abfragesprache Jet stellt eine einfache Abfragesprache für Outlook dar und baut auf dem Microsoft Jet-Ausdrucksdienst auf. Mit Jet werden Filterzeichenfolgen für die <b>Restrict</b>-Methoden der <b>Items</b>-Auflistung und des <b>Table</b>-Objekts erstellt.</p></td>
</tr>
</tbody>
</table>


Im folgenden Codebeispiel ruft DemoInstantSearch mithilfe der [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\))-Eigenschaft des [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\))-Objekts alle E-Mail-Ordner in allen Speichern ab, in denen die Indizierung aktiviert ist. Anschließend wird mit der **Search**-Methode des **Explorer**-Objekts nach allen Elementen gefiltert, die den genauen Ausdruck "Office 2007" im Betreff enthalten und die im letzten Monat empfangen wurden. Die Ergebnisse der Suche werden schließlich in einem separaten Explorerfenster angezeigt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoInstantSearch()
{
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        Outlook.Explorer explorer = Application.Explorers.Add(
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            as Outlook.Folder,
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        string filter = "subject:" +
            "\"" + "Office 2007" + "\"" +
            " received:(last month)";
        explorer.Search(filter,
            Outlook.OlSearchScope.olSearchScopeAllFolders);
        explorer.Display();
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Suchen und Filtern](search-and-filter.md)

