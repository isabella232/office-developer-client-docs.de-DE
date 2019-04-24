---
title: Hinzufügen von Feldern zu einer Ansicht
TOCTitle: Add fields to a view
ms:assetid: ea371f27-ea65-47ef-ae44-ef843a78ab6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424481(v=office.15)
ms:contentKeyID: 55119934
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4b850bf87be4024152ee808624ad93836b904897
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359696"
---
# <a name="add-fields-to-a-view"></a>Hinzufügen von Feldern zu einer Ansicht

In diesem Beispiel wird gezeigt, wie eine Ansicht mit der [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\))-Methode für die [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\))-Auflistung anpasst wird, um einer Ansicht Felder hinzuzufügen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Sie können angeben, welche Outlook-Elementeigenschaften in einer Ansicht angezeigt werden, indem Sie der **ViewFields**-Auflistung nur für das [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\))- und das [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\))-Objekt eine oder mehrere Eigenschaften hinzufügen. Verwenden Sie für andere abgeleitete **View**-Objekte, z. B. [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\))-, [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\))-, [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\))- und [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\))-Objekte andere Methoden, um zu bestimmen, welche Outlook-Elementeigenschaften in der Ansicht angezeigt werden. Die für das **BusinessCardView**-Objekt angezeigten Felder werden beispielsweise vom Layout der elektronischen Visitenkarte bestimmt, die den einzelnen Outlook-Elementen zugeordnet ist.

Die **ViewFields**-Auflistung für eine Ansicht rufen Sie ab, indem Sie die **ViewFields**-Eigenschaft des zugehörigen **View**-Objekts (z. B. **CardView** oder **TableView**) verwenden. Mit der **Add**-Methode der **ViewFields**-Auflistung erstellen Sie ein [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) -Objekt, das eine in einer Ansicht anzuzeigende Outlook-Elementeigenschaft darstellt. Ein **ViewField**-Objekt identifiziert nicht nur eine Outlook-Elementeigenschaft, die in der Ansicht angezeigt werden soll, sondern beschreibt auch, wie die Werte für diese Eigenschaft angezeigt werden sollen. Sie können die Art und Weise ändern, wie einzelne Spalteneigenschaften in einer Ansicht angezeigt werden, indem Sie die [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) -Eigenschaft des **ViewField**-Objekts ändern.

Im folgenden Codebeispiel ruft ModifyMeetingRequestsView das TableView-Objekt ab, das alle Ansichten aus dem Posteingang des Benutzers darstellt, die Ansichten für Besprechungsanfragen sind. Anschließend werden mithilfe der Add-Methode dem ViewFields-Objekt, das dem TableView-Objekt entspricht, die Felder Beginn und Ende hinzugefügt. Außerdem wird die Bezeichnung des Felds Von auf Organisiert von geändert. Zuletzt speichert ModifyMeetingRequestsView das geänderte TableView-Objekt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ModifyMeetingRequestsView()
{
    Outlook.TableView tableView = null;
    Outlook.ViewField startField = null;
    Outlook.ViewField endField = null;
    Outlook.ViewField fromField = null;
    try
    {
        tableView =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            .Views["Meeting Requests"] as Outlook.TableView;
    }
    catch { }
    if (tableView != null)
    {
        try
        {
            startField = tableView.ViewFields["Start"];
        }
        catch{}
        if (startField == null)
        {
            startField = tableView.ViewFields.Add("Start");
        }
        try
        {
            endField = tableView.ViewFields["End"];
        }
        catch{}
        if (endField == null)
        {
            endField = tableView.ViewFields.Add("End");
        }
        try
        {
            fromField = tableView.ViewFields["From"];
        }
        catch{}
        if (fromField != null)
        {
            fromField.ColumnFormat.Label = "Organized By";
        }
        try
        {
            tableView.Save();
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Views](views.md)

