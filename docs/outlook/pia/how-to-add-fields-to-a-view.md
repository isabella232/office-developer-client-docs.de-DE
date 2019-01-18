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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705267"
---
# <a name="add-fields-to-a-view"></a><span data-ttu-id="32574-102">Hinzufügen von Feldern zu einer Ansicht</span><span class="sxs-lookup"><span data-stu-id="32574-102">Add fields to a view</span></span>

<span data-ttu-id="32574-103">In diesem Beispiel wird gezeigt, wie eine Ansicht mit der [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\))-Methode für die [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\))-Auflistung anpasst wird, um einer Ansicht Felder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="32574-103">This example shows how to customize a view by using the [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) method of the [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) collection to add fields to a view.</span></span>

## <a name="example"></a><span data-ttu-id="32574-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="32574-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="32574-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="32574-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="32574-106">Sie können angeben, welche Outlook-Elementeigenschaften in einer Ansicht angezeigt werden, indem Sie der **ViewFields**-Auflistung nur für das [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\))- und das [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\))-Objekt eine oder mehrere Eigenschaften hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="32574-106">You can specify which Outlook item properties are displayed in a view by adding one or more properties to the **ViewFields** collection for only the [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) and [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) objects.</span></span> <span data-ttu-id="32574-107">Verwenden Sie für andere abgeleitete **View**-Objekte, z. B. [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\))-, [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\))-, [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\))- und [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\))-Objekte andere Methoden, um zu bestimmen, welche Outlook-Elementeigenschaften in der Ansicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="32574-107">For other derived **View** objects such as [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)), and [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)) objects, use other methods of determining which Outlook item properties are displayed within the view.</span></span> <span data-ttu-id="32574-108">Die für das **BusinessCardView**-Objekt angezeigten Felder werden beispielsweise vom Layout der elektronischen Visitenkarte bestimmt, die den einzelnen Outlook-Elementen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="32574-108">For example, the fields displayed for the **BusinessCardView** object are determined by the electronic business card (EBC) layout associated with each displayed Outlook item.</span></span>

<span data-ttu-id="32574-p102">Die **ViewFields**-Auflistung für eine Ansicht rufen Sie ab, indem Sie die **ViewFields**-Eigenschaft des zugehörigen **View**-Objekts (z. B. **CardView** oder **TableView**) verwenden. Mit der **Add**-Methode der **ViewFields**-Auflistung erstellen Sie ein [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) -Objekt, das eine in einer Ansicht anzuzeigende Outlook-Elementeigenschaft darstellt. Ein **ViewField**-Objekt identifiziert nicht nur eine Outlook-Elementeigenschaft, die in der Ansicht angezeigt werden soll, sondern beschreibt auch, wie die Werte für diese Eigenschaft angezeigt werden sollen. Sie können die Art und Weise ändern, wie einzelne Spalteneigenschaften in einer Ansicht angezeigt werden, indem Sie die [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) -Eigenschaft des **ViewField**-Objekts ändern.</span><span class="sxs-lookup"><span data-stu-id="32574-p102">To get the **ViewFields** collection for a view, use the **ViewFields** property of the associated **View** object (for example, the **CardView** or **TableView** objects). The **Add** method of the **ViewFields** collection is used to create a [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) object that represents the Outlook item property to be displayed in the view. A **ViewField** object not only identifies an Outlook item property to display within the view, but it also describes how the values for that property should be displayed. You can change how individual column properties are displayed in a view by modifying the [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) property of the **ViewField** object.</span></span>

<span data-ttu-id="32574-p103">Im folgenden Codebeispiel ruft ModifyMeetingRequestsView das TableView-Objekt ab, das alle Ansichten aus dem Posteingang des Benutzers darstellt, die Ansichten für Besprechungsanfragen sind. Anschließend werden mithilfe der Add-Methode dem ViewFields-Objekt, das dem TableView-Objekt entspricht, die Felder Beginn und Ende hinzugefügt. Außerdem wird die Bezeichnung des Felds Von auf Organisiert von geändert. Zuletzt speichert ModifyMeetingRequestsView das geänderte TableView-Objekt.</span><span class="sxs-lookup"><span data-stu-id="32574-p103">In the following code example, ModifyMeetingRequestsView gets the **TableView** object that represents all the views from the user’s Inbox that are “Meeting Requests” views. The example then uses the **Add** method to add the “Start” and “End” fields to the **ViewFields** object that corresponds to the **TableView** object. It also changes the label for the “From” field to “Organized By”. ModifyMeetingRequestsView then saves the modified **TableView** object.</span></span>

<span data-ttu-id="32574-117">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="32574-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="32574-118">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="32574-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="32574-119">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="32574-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="32574-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32574-120">See also</span></span>

- [<span data-ttu-id="32574-121">Ansichten</span><span class="sxs-lookup"><span data-stu-id="32574-121">Views</span></span>](views.md)

