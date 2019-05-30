---
title: Erstellen einer Ansicht
TOCTitle: Create a view
ms:assetid: 2f8ad187-1030-420a-bc74-c327e3521550
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424468(v=office.15)
ms:contentKeyID: 55119902
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 75f414d95818b618cfcae236822bb2f5dacdf5f2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540805"
---
# <a name="create-a-view"></a>Erstellen einer Ansicht

In diesem Beispiel wird die Verwendung der [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\))-Methode der [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\))-Auflistung zum Erstellen einer Ansicht für ein [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekt veranschaulicht.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Sie können anpassbare Ansichten erstellen, in denen Sie Daten aller Typen im Ansichtsbereich in einem Outlook Explorer-Fenster besser sortieren, gruppieren und anzeigen können. Sie können auch vordefinierte Ansichten programmgesteuert anpassen. Die folgende Tabelle enthält Objekte, die Outlook-Ansichten darstellen. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objektname</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></p></td>
<td><p>Daten werden als Folge von Bildern elektronischer Visitenkarten angezeigt.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></p></td>
<td><p>Daten werden in einem Kalenderformat angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></p></td>
<td><p>Daten werden in einer Folge von Karten angezeigt.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></p></td>
<td><p>Daten werden als Symbole für Windows-Ordner oder Explorer-Symbole angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></p></td>
<td><p>Daten werden in einer einfachen feldbasierten Tabelle angezeigt.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></p></td>
<td><p>Daten werden in einer anpassbaren linearen Zeitachse angezeigt.</p></td>
</tr>
</tbody>
</table>


Sie können mithilfe des [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\))-Objekts auf Eigenschaften und Methoden zugreifen, die für alle Ansichten gelten. Um jedoch auf bestimmte Eigenschaften zugreifen zu können, die nicht für alle Ansichten gelten, müssen Sie das **View**-Objekt in ein abgeleitetes **View**-Objekt umwandeln, zu dem die Eigenschaft gehört, auf die Sie zugreifen möchten. Für den Zugriff auf die [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) -Eigenschaft des **Cardview**-Objekts müssen Sie das **View**-Objekt in das **CardView**-Objekt umwandeln. Wenn Sie ermitteln möchten, welche Art von Ansicht von einem bestimmten **View**-Objekt dargestellt wird, verwenden Sie die [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\))-Eigenschaft.

Verwenden Sie zum Erstellen einer neuen Ansicht die **Add**-Methode der **Views**-Auflistung für ein **Folder**-Objekt. Legen Sie dann die Sichtbarkeit für die Ansicht zum Zeitpunkt der Erstellung oder zu einem beliebigen Zeitpunkt nach der Erstellung der Ansicht fest. Zum Angeben der Sichtbarkeit der Ansicht zum Zeitpunkt der Erstellung geben Sie eine [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\))-Konstante im *SaveOption*-Parameter der **Add**-Methode an. Zum Angeben der Sichtbarkeit der Ansicht zu einem späteren Zeitpunkt nach der Erstellung geben Sie eine **OlViewSaveOption**-Konstante für die [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) -Eigenschaft des **View**-Objekts an. 

Durch Hinzufügen einer neuen Ansicht wird das [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) -Ereignis der **Views**-Auflistung ausgelöst. Passen Sie sie nach ihrer Erstellung programmgesteuert an, indem Sie das **View**-Objekt in eines der abgeleiteten Objekte umwandeln und dann die gewünschten Änderungen vornehmen. Verwenden Sie die **Save**-Methode des abgeleiteten **View**-Objekts oder das **View**-Objekt, um Änderungen an der Ansicht zu speichern. Verwenden Sie abschließend die **Apply**-Methode des abgeleiteten **View**-Objekts oder das **View**-Objekt, um die Ansicht auf das aktuelle [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\))-Objekt anzuwenden. Dadurch wird das [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\))-Ereignis des **Explorer**-Objekts ausgelöst.

Im folgenden Codebeispiel fügt CreateMeetingRequestsView die neue Ansicht "Meeting Requests" dem Posteingang des Benutzers hinzu, indem das **View**-Objekt in ein **TableView**-Objekt umgewandelt wird. CreateMeetingRequestsView ruft dann die **Add**-Methode des **Views**-Objekts ab, dessen *Name*-Parameter auf "Meeting Requests" und *ViewType*-Parameter auf **olTableView** festgelegt ist. Die [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\))-Eigenschaft des **TableView**-Objekts ist auf eine DASL-Zeichenfolge (DAV Searching and Locating) festgelegt, die bewirkt, dass die Ansicht nur angezeigt wird, wenn es Elemente gibt, die "IPM.Schedule" in der Nachrichtenklasse dieses Elements enthalten. Dann wird die neue Ansicht gespeichert und angewendet.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateMeetingRequestsView()
{
    const string PR_MESSAGE_CLASS =
        "http://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.Views views =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Views;
    Outlook.TableView tableView = (Outlook.TableView)
        views.Add("Meeting Requests",
        Outlook.OlViewType.olTableView,
        Outlook.OlViewSaveOption.olViewSaveOptionThisFolderEveryone);
    tableView.Filter = "\"" + PR_MESSAGE_CLASS + "\"" +
        " like 'IPM.Schedule%'";
    tableView.Save();
    tableView.Apply();
}
```

## <a name="see-also"></a>Siehe auch

- [Views](views.md)

