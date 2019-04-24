---
title: Filtern und Anzeigen der im letzten Monat geänderten Posteingangselemente
TOCTitle: Filter and display Inbox items modified in the last month
ms:assetid: ef6004dc-0b5a-4d1f-8937-1384d1dfc1ca
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424482(v=office.15)
ms:contentKeyID: 55119886
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77fe6e7df4cf67ed1ca2d62b8cf48f1b2873ccbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320293"
---
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a>Filtern und Anzeigen der im letzten Monat geänderten Posteingangselemente

In diesem Beispiel wird veranschaulicht, wie Posteingangselemente gefiltert und angezeigt werden, die im letzten Monat geändert wurden.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Die Abfragesprache DAV Search and Locating (DASL) basiert auf der Microsoft Exchange-Implementierung von DASL in Outlook. Sie kann verwendet werden, um eigenschaftsbasierte Ergebnisse für Suchvorgänge auf Elementebene in Ordnerdaten zurückzugeben, z. B. die von einem [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt dargestellten Daten. DASL-Filter unterstützen Zeichenfolgenvergleiche unter Verwendung des Gleichheitszeichens (=), einschließlich Äquivalenz, Präfix-, Ausdrucks- und Teilzeichenfolgenübereinstimmung. DASL-Abfragen können für einen Datums-/Uhrzeitvergleich und zum Filtern verwendet werden.

Da DASL-Abfragen **DateTime**-Vergleiche stets in koordinierter Weltzeit (Coordinated Universal Time, UTC) ausführen, müssen Sie den lokalen Zeitwert in UTC konvertieren, damit die Abfrage fehlerfrei funktioniert. Außerdem müssen Sie den **DateTime**-Wert in eine Zeichenfolgendarstellung umwandeln, weil DASL-Filter Zeichenfolgenvergleiche unterstützen. Sie haben zwei Möglichkeiten, die **DateTime**-Konvertierung durchzuführen: mithilfe der [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) -Methode des [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) -Objekts oder mithilfe von Outlook- **DateTime**-Makros.

In der folgenden Codezeile wird die Verwendung der **LocalTimeToUTC**-Methode zum Konvertieren des Werts der **LastModificationTime**-Eigenschaft in UTC gezeigt (diese ist in allen **Item**-Objekten eine Standardspalte).

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

In der folgenden Tabelle werden die **DateTime**-Makros aufgelistet, mit denen Sie gefilterte Zeichenfolgen zurückgeben können, die den Wert einer gegebenen **DateTime**-Eigenschaft mit einem angegebenen relativen Datum oder Datumsbereich in UTC vergleichen. Die SchemaName-Eigenschaft stellt eine beliebige gültige **DateTime**-Eigenschaft dar, auf die anhand des Namespace verwiesen wird.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Makro</p></th>
<th><p>Syntax</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>heute</p></td>
<td><p>%today(“SchemaName”)%</p></td>
<td><p>Legt eine Beschränkung auf Elemente fest, deren Wert der SchemaName-Eigenschaft „heute“ lautet.</p></td>
</tr>
<tr class="even">
<td><p>morgen</p></td>
<td><p>%tomorrow(“SchemaName”)%</p></td>
<td><p>Legt eine Beschränkung auf Elemente fest, deren Wert der SchemaName-Eigenschaft „morgen“ lautet.</p></td>
</tr>
<tr class="odd">
<td><p>gestern</p></td>
<td><p>%yesterday(“SchemaName”)%</p></td>
<td><p>Legt eine Beschränkung auf Elemente fest, deren Wert der SchemaName-Eigenschaft „gestern“ lautet.</p></td>
</tr>
<tr class="even">
<td><p>next7days</p></td>
<td><p>%next7days(“SchemaName”)%</p></td>
<td><p>Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der den nächsten sieben Tagen entspricht.</p></td>
</tr>
<tr class="odd">
<td><p>last7days</p></td>
<td><p>%last7days(“SchemaName”)%</p></td>
<td><p>Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der den letzten sieben Tagen entspricht.</p></td>
</tr>
<tr class="even">
<td><p>nextweek</p></td>
<td><p>%nextweek(“SchemaName”)%</p></td>
<td><p>Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der der nächsten Woche entspricht.</p></td>
</tr>
<tr class="odd">
<td><p>thisweek</p></td>
<td><p>%thisweek(“SchemaName”)%</p></td>
<td><p>Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der dieser Woche entspricht.</p></td>
</tr>
<tr class="even">
<td><p>lastweek</p></td>
<td><p>%lastweek(“SchemaName”)%</p></td>
<td><p>Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der der letzten Woche entspricht.</p></td>
</tr>
<tr class="odd">
<td><p>nextmonth</p></td>
<td><p>%nextmonth(“SchemaName”)%</p></td>
<td><p>Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte in einem Bereich hat, der dem nächsten Monat entspricht.</p></td>
</tr>
<tr class="even">
<td><p>thismonth</p></td>
<td><p>%thismonth(“SchemaName”)%</p></td>
<td><p>Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte im Bereich dieses Monats hat.</p></td>
</tr>
<tr class="odd">
<td><p>lastmonth</p></td>
<td><p>%lastmonth(“SchemaName”)%</p></td>
<td><p>Legt eine Beschränkung auf Elemente fest, deren SchemaName-Eigenschaft Werte im Bereich des letzten Monats hat.</p></td>
</tr>
</tbody>
</table>


Im folgenden Beispiel erstellt DemoDASLDateMacro eine DASL-Abfrage, in der mit dem **lastmonthDateTime**-Makro Elemente aus dem Posteingang des Benutzers herausgefiltert werden, die im vergangenen Monat geändert wurden. Dann wird ein **Table**-Objekt mit diesen Filter erstellt die Zeilen in dem eingeschränkten **Table**-Objekt aufgezählt und angezeigt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoDASLDateMacro()
{
    string filter = "@SQL=" + "%lastmonth(" + "\"" +
        "DAV:getlastmodified" + "\"" + ")%";
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Suchen und Filtern](search-and-filter.md)

