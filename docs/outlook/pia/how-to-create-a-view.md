---
title: Erstellen einer Ansicht
TOCTitle: Create a view
ms:assetid: 2f8ad187-1030-420a-bc74-c327e3521550
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424468(v=office.15)
ms:contentKeyID: 55119902
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c91f43001d6c56ad3b4c316aede9845a5e0a0064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349490"
---
# <a name="create-a-view"></a><span data-ttu-id="e7fc5-102">Erstellen einer Ansicht</span><span class="sxs-lookup"><span data-stu-id="e7fc5-102">Create a view</span></span>

<span data-ttu-id="e7fc5-103">In diesem Beispiel wird die Verwendung der [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\))-Methode der [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\))-Auflistung zum Erstellen einer Ansicht für ein [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekt veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-103">This example shows how to use the [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) method of the [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) collection to create a view for a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="e7fc5-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e7fc5-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e7fc5-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="e7fc5-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="e7fc5-p101">Sie können anpassbare Ansichten erstellen, in denen Sie Daten aller Typen im Ansichtsbereich in einem Outlook Explorer-Fenster besser sortieren, gruppieren und anzeigen können. Sie können auch vordefinierte Ansichten programmgesteuert anpassen. Die folgende Tabelle enthält Objekte, die Outlook-Ansichten darstellen. </span><span class="sxs-lookup"><span data-stu-id="e7fc5-p101">You can create customizable views that allow you to sort, group, and view data of all different types within the View Pane of the Outlook explorer window. You can also customize built-in views programmatically. The following table lists objects that represent Outlook views.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e7fc5-109">Objektname</span><span class="sxs-lookup"><span data-stu-id="e7fc5-109">Object Name</span></span></p></th>
<th><p><span data-ttu-id="e7fc5-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7fc5-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7fc5-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></span><span class="sxs-lookup"><span data-stu-id="e7fc5-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></span></span></p></td>
<td><p><span data-ttu-id="e7fc5-112">Daten werden als Folge von Bildern elektronischer Visitenkarten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-112">Data is viewed as a series of electronic business card images.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7fc5-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span><span class="sxs-lookup"><span data-stu-id="e7fc5-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span></span></p></td>
<td><p><span data-ttu-id="e7fc5-114">Daten werden in einem Kalenderformat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-114">Data is viewed in a calendar format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7fc5-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></span><span class="sxs-lookup"><span data-stu-id="e7fc5-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></span></span></p></td>
<td><p><span data-ttu-id="e7fc5-116">Daten werden in einer Folge von Karten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-116">Data is viewed in a series of cards.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7fc5-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></span><span class="sxs-lookup"><span data-stu-id="e7fc5-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></span></span></p></td>
<td><p><span data-ttu-id="e7fc5-118">Daten werden als Symbole für Windows-Ordner oder Explorer-Symbole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-118">Data is viewed as Windows folder icons or explorer icons.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7fc5-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></span><span class="sxs-lookup"><span data-stu-id="e7fc5-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></span></span></p></td>
<td><p><span data-ttu-id="e7fc5-120">Daten werden in einer einfachen feldbasierten Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-120">Data is viewed in a simple field-based table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7fc5-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></span><span class="sxs-lookup"><span data-stu-id="e7fc5-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></span></span></p></td>
<td><p><span data-ttu-id="e7fc5-122">Daten werden in einer anpassbaren linearen Zeitachse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-122">Data is viewed in a customizable linear time line.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e7fc5-123">Sie können mithilfe des [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\))-Objekts auf Eigenschaften und Methoden zugreifen, die für alle Ansichten gelten.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-123">You can access properties and methods that are common to all views by using the [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)) object.</span></span> <span data-ttu-id="e7fc5-124">Um jedoch auf bestimmte Eigenschaften zugreifen zu können, die nicht für alle Ansichten gelten, müssen Sie das **View**-Objekt in ein abgeleitetes **View**-Objekt umwandeln, zu dem die Eigenschaft gehört, auf die Sie zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-124">However, to access certain properties that are not common to all views, you must cast the **View** object to a derived **View** object that the property you want to access belongs to.</span></span> <span data-ttu-id="e7fc5-125">Für den Zugriff auf die [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) -Eigenschaft des **Cardview**-Objekts müssen Sie das **View**-Objekt in das **CardView**-Objekt umwandeln.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-125">For example, to access the [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) property of the **Cardview** object, cast the **View** object to the **Cardview** object.</span></span> <span data-ttu-id="e7fc5-126">Wenn Sie ermitteln möchten, welche Art von Ansicht von einem bestimmten **View**-Objekt dargestellt wird, verwenden Sie die [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-126">If you want to determine which type of view is represented by a particular **View** object, use the [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)) property.</span></span>

<span data-ttu-id="e7fc5-127">Verwenden Sie zum Erstellen einer neuen Ansicht die **Add**-Methode der **Views**-Auflistung für ein **Folder**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-127">To create a new view, use the **Add** method of the **Views** collection for a **Folder** object.</span></span> <span data-ttu-id="e7fc5-128">Legen Sie dann die Sichtbarkeit für die Ansicht zum Zeitpunkt der Erstellung oder zu einem beliebigen Zeitpunkt nach der Erstellung der Ansicht fest.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-128">Then set the visibility for the view either at the time of creation, or at any time after the view is created.</span></span> <span data-ttu-id="e7fc5-129">Zum Angeben der Sichtbarkeit der Ansicht zum Zeitpunkt der Erstellung geben Sie eine [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\))-Konstante im *SaveOption*-Parameter der **Add**-Methode an.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-129">To set the visibility for the view at the time of creation, specify an [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) constant in the *SaveOption* parameter of the **Add** method.</span></span> <span data-ttu-id="e7fc5-130">Zum Angeben der Sichtbarkeit der Ansicht zu einem späteren Zeitpunkt nach der Erstellung geben Sie eine **OlViewSaveOption**-Konstante für die [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) -Eigenschaft des **View**-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-130">To set the visibility at any time after the view is created, specify an **OlViewSaveOption** constant for the [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) property of the **View** object.</span></span> 

<span data-ttu-id="e7fc5-131">Durch Hinzufügen einer neuen Ansicht wird das [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) -Ereignis der **Views**-Auflistung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-131">Adding a new view raises the [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) event of the **Views** collection.</span></span> <span data-ttu-id="e7fc5-132">Passen Sie sie nach ihrer Erstellung programmgesteuert an, indem Sie das **View**-Objekt in eines der abgeleiteten Objekte umwandeln und dann die gewünschten Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-132">Once the view is created, customize the view programmatically by casting the **View** object to one of the derived objects and then making necessary changes.</span></span> <span data-ttu-id="e7fc5-133">Verwenden Sie die **Save**-Methode des abgeleiteten **View**-Objekts oder das **View**-Objekt, um Änderungen an der Ansicht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-133">Use the **Save** method of the derived **View** object or the **View** object to save any changes to the view.</span></span> <span data-ttu-id="e7fc5-134">Verwenden Sie abschließend die **Apply**-Methode des abgeleiteten **View**-Objekts oder das **View**-Objekt, um die Ansicht auf das aktuelle [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\))-Objekt anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-134">Finally, use the **Apply** method of the derived **View** object or the **View** object to apply the view to the current [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object.</span></span> <span data-ttu-id="e7fc5-135">Dadurch wird das [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\))-Ereignis des **Explorer**-Objekts ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-135">This raises the [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) event of the **Explorer** object.</span></span>

<span data-ttu-id="e7fc5-136">Im folgenden Codebeispiel fügt CreateMeetingRequestsView die neue Ansicht "Meeting Requests" dem Posteingang des Benutzers hinzu, indem das **View**-Objekt in ein **TableView**-Objekt umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-136">In the following code example, CreateMeetingRequestsView adds a new view named “Meeting Requests” to the user’s Inbox by casting the **View** object to a **TableView** object.</span></span> <span data-ttu-id="e7fc5-137">CreateMeetingRequestsView ruft dann die **Add**-Methode des **Views**-Objekts ab, dessen *Name*-Parameter auf "Meeting Requests" und *ViewType*-Parameter auf **olTableView** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-137">CreateMeetingRequestsView then calls the **Add** method of the **Views** object with the *Name* parameter set to “Meeting Requests” and the *ViewType* parameter set to **olTableView**.</span></span> <span data-ttu-id="e7fc5-138">Die [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\))-Eigenschaft des **TableView**-Objekts ist auf eine DASL-Zeichenfolge (DAV Searching and Locating) festgelegt, die bewirkt, dass die Ansicht nur angezeigt wird, wenn es Elemente gibt, die "IPM.Schedule" in der Nachrichtenklasse dieses Elements enthalten.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-138">The [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) property of the **TableView** object is set to a DAV Searching and Locating (DASL) string that causes the view to display only when there are items that contain “IPM.Schedule” in the message class for the item.</span></span> <span data-ttu-id="e7fc5-139">Dann wird die neue Ansicht gespeichert und angewendet.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-139">The new view is then saved and applied.</span></span>

<span data-ttu-id="e7fc5-140">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-140">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e7fc5-141">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-141">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e7fc5-142">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="e7fc5-142">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateMeetingRequestsView()
{
    const string PR_MESSAGE_CLASS =
        "https://schemas.microsoft.com/mapi/proptag/0x001A001E";
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

## <a name="see-also"></a><span data-ttu-id="e7fc5-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7fc5-143">See also</span></span>

- [<span data-ttu-id="e7fc5-144">Views</span><span class="sxs-lookup"><span data-stu-id="e7fc5-144">Views</span></span>](views.md)

