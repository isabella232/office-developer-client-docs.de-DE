---
title: Filtern und Anzeigen von berechneten Eigenschaften beim Aufzählen von Elementen in einem Ordner
TOCTitle: Filter and display computed properties when enumerating items in a folder
ms:assetid: b068e625-ff12-444d-a30d-51a3acba3043
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184632(v=office.15)
ms:contentKeyID: 55119922
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1c1702ce816714b21da860aea3e49db8a3511701
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542639"
---
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a>Filtern und Anzeigen von berechneten Eigenschaften beim Aufzählen von Elementen in einem Ordner

In diesem Beispiel wird gezeigt, wie Sie beim Aufzählen von Elementen in einem Ordner berechnete Eigenschaften filtern und anzeigen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Das [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) -Objekt stellt eine Gruppe von Elementdaten aus einem [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) - oder einem [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) -Objekt dar. Das [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) -Objekt stellt Zeilen von Daten in einem **Table**-Objekt dar. Das [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) -Objekt stellt Eigenschaften des **Table**-Objekts dar. Sie können dem **Table**-Objekt bestimmte Eigenschaften hinzufügen, indem Sie die [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) -Methode des **Columns**-Objekts verwenden. Mithilfe der [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) -Methode des **Table**-Objekts können Sie bestimmte Eigenschaften filtern. Bestimmte Eigenschaften lassen sich jedoch weder mithilfe von **Columns.Add** dem **Table**-Objekt hinzufügen noch mithilfe der **Restrict**-Methode filtern. In der folgenden Tabelle wird erklärt, ob Eigenschaften für das **Table**-Objekt unterstützt werden, wenn Sie die **Columns.Add**- oder die **Restrict**-Methode verwenden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Eigenschaft</p></th>
<th><p>For Columns.Add</p></th>
<th><p>For Restrict</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Binäre Eigenschaften, z. B. <b>EntryID</b>.</p></td>
<td><p>Über die integrierte oder Namespace-Eigenschaft unterstützt.</p></td>
<td><p>Nicht unterstützt. In Outlook wird ein Fehler ausgelöst.</p></td>
</tr>
<tr class="even">
<td><p>Body-Eigenschaften, einschließlich <b>Body</b> und <b>HTMLBody</b>, sowie die Namespacedarstellung dieser Eigenschaften, einschließlich <b>PR_RTF_COMPRESSED</b>.</p></td>
<td><p>Die <b>Body</b> Eigenschaft wird mit einer Bedingung unterstützt, dass nur die ersten 255 Byte des Werts in einem <b>Table</b>-Objekt gespeichert werden. Andere Eigenschaften, die den Textinhalt in HTML oder RTF darstellen, werden nicht unterstützt. Da nur die ersten 255 Byte von <b>Body</b> zurückgegeben werden, verwenden Sie die <b>EntryID</b> des Elements in der <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a>-Methode zum Abrufen des Elementobjekts, wenn Sie den gesamten Textinhalt eines Elements in Text oder HTML abrufen möchten. Rufen Sie dann den vollständigen Wert von <b>Body</b> über das Elementobjekt ab.</p></td>
<td><p>In einem Filter wird nur die in Text dargestellte <b>Body</b>-Eigenschaft unterstützt. Das bedeutet, dass in einem DASL-Filter (DAV Searching and Locating) mit <em>urn:schemas:http-mail:textdescription</em> auf die Eigenschaft verwiesen werden muss und dass Sie keine HTML-Tags im Textkörper filtern können. Sie können die Leistung verbessern, indem Sie im Filter Schlüsselwörter für den Inhaltsindex verwenden, um Zeichenfolgen im Textkörper zu vergleichen.</p></td>
</tr>
<tr class="odd">
<td><p>Computer-Eigenschaften, z. B. <b>AutoResolvedWinner</b> und <b>BodyFormat</b>.</p></td>
<td><p>Nicht unterstützt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td><p>Mehrwertige Eigenschaften, z. B. <b>Categories</b>, <b>Children</b>, <b>Companies</b> und <b>VotingOptions</b>.</p></td>
<td><p>Unterstützt</p></td>
<td><p>Unterstützt, vorausgesetzt, dass Sie eine DASL-Abfrage unter Verwendung der Namespace-Darstellung erstellen können.</p></td>
</tr>
<tr class="odd">
<td><p>Eigenschaften, die ein Objekt zurückgeben, z. B. <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b> und <b>UserProperties</b></p></td>
<td><p>Nicht unterstützt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
</tbody>
</table>


In der folgenden Tabelle werden bekannte ungültige Eigenschaften aufgelistet, die Sie nicht mithilfe der **Columns.Add**-Methode dem **Table**-Objekt hinzufügen können. Wenn Sie versuchen, eine Eigenschaft aus dieser Liste hinzuzufügen, wird in Outlook ein Fehler ausgelöst.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>AutoResolvedWinner</p></td>
<td><p>BodyFormat</p></td>
<td><p>Klasse</p></td>
</tr>
<tr class="even">
<td><p>Unternehmen</p></td>
<td><p>ContactNames</p></td>
<td><p>DLName</p></td>
</tr>
<tr class="odd">
<td><p>DownloadState</p></td>
<td><p>FlagIcon</p></td>
<td><p>HtmlBody</p></td>
</tr>
<tr class="even">
<td><p>InternetCodePage</p></td>
<td><p>IsConflict</p></td>
<td><p>IsMarkedAsTask</p></td>
</tr>
<tr class="odd">
<td><p>MeetingWorkspaceURL</p></td>
<td><p>MemberCount</p></td>
<td><p>Berechtigung</p></td>
</tr>
<tr class="even">
<td><p>PermissionService</p></td>
<td><p>RecurrenceState</p></td>
<td><p>ResponseState</p></td>
</tr>
<tr class="odd">
<td><p>Saved</p></td>
<td><p>Gesendet</p></td>
<td><p>Übermittelt</p></td>
</tr>
<tr class="even">
<td><p>TaskSubject</p></td>
<td><p>Ungelesen</p></td>
<td><p>VotingOptions</p></td>
</tr>
</tbody>
</table>


Einige berechnete Eigenschaften können nicht zum Spaltensatz für eine Tabelle hinzugefügt werden; im folgenden Codebeispiel wird diese Einschränkung umgangen. GetToDoItems verwendet eine DASL-Abfrage, um die Elemente zu beschränken, die in der **Table** angezeigt werde.. Wenn die berechnete Eigenschaft eine Namespacedarstellung hat, wird diese verwendet, um eine DASL-Abfrage erstellen, die das **Table**-Objekt so einschränkt, dass Zeilen für einen bestimmten Wert der berechneten Eigenschaft zurückgegeben werden. GetToDoItems ruft Elemente im Posteingang ab, wobei der Wert der [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\))- Eigenschaft gleich **true** ist; dann werden Werte bestimmten Aufgabeneigenschaften zugewiesen, z. B. [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)) und [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)). Schließlich werden diese Eigenschaften in die Listener der Ablaufverfolgung der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung geschrieben.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetToDoItems()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // DASL filter for IsMarkedAsTask
    string filter = "@SQL=" + "\"" +
        "http://schemas.microsoft.com/mapi/proptag/0x0E2B0003"
        + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    table.Columns.Add("TaskStartDate");
    table.Columns.Add("TaskDueDate");
    table.Columns.Add("TaskCompletedDate");
    // Use GUID/ID to represent TaskSubject
    table.Columns.Add(
        "http://schemas.microsoft.com/mapi/id/" +
        "{00062008-0000-0000-C000-000000000046}/85A4001E");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Task Subject: " + nextRow[9]);
        sb.AppendLine("Start Date: "
            + nextRow["TaskStartDate"]);
        sb.AppendLine("Due Date: "
            + nextRow["TaskDueDate"]);
        sb.AppendLine("Completed Date: "
            + nextRow["TaskCompletedDate"]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Suchen und Filtern](search-and-filter.md)

