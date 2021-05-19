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
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="52a3b-102">Filtern und Anzeigen von berechneten Eigenschaften beim Aufzählen von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="52a3b-102">Filter and display computed properties when enumerating items in a folder</span></span>

<span data-ttu-id="52a3b-103">In diesem Beispiel wird gezeigt, wie Sie beim Aufzählen von Elementen in einem Ordner berechnete Eigenschaften filtern und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="52a3b-103">This example shows how to filter and display computed properties when enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="52a3b-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="52a3b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="52a3b-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="52a3b-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="52a3b-p101">Das [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) -Objekt stellt eine Gruppe von Elementdaten aus einem [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) - oder einem [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) -Objekt dar. Das [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) -Objekt stellt Zeilen von Daten in einem **Table**-Objekt dar. Das [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) -Objekt stellt Eigenschaften des **Table**-Objekts dar. Sie können dem **Table**-Objekt bestimmte Eigenschaften hinzufügen, indem Sie die [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) -Methode des **Columns**-Objekts verwenden. Mithilfe der [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) -Methode des **Table**-Objekts können Sie bestimmte Eigenschaften filtern. Bestimmte Eigenschaften lassen sich jedoch weder mithilfe von **Columns.Add** dem **Table**-Objekt hinzufügen noch mithilfe der **Restrict**-Methode filtern. In der folgenden Tabelle wird erklärt, ob Eigenschaften für das **Table**-Objekt unterstützt werden, wenn Sie die **Columns.Add**- oder die **Restrict**-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="52a3b-p101">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object. The [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object represents rows of data in a **Table**. The [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) object represents properties of the **Table**. You can add certain properties to the **Table** object by using the [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) method of the **Columns** object. You can filter certain properties by using the [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) method of the **Table** object. However, some properties cannot be added to the **Table** object by using **Columns.Add**, nor can they be filtered by using the **Restrict** method. The following table describes whether properties are supported for the **Table** object when you use the **Columns.Add** or **Restrict** method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52a3b-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="52a3b-113">Property</span></span></p></th>
<th><p><span data-ttu-id="52a3b-114">For Columns.Add</span><span class="sxs-lookup"><span data-stu-id="52a3b-114">For Columns.Add</span></span></p></th>
<th><p><span data-ttu-id="52a3b-115">For Restrict</span><span class="sxs-lookup"><span data-stu-id="52a3b-115">For Restrict</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52a3b-116">Binäre Eigenschaften, z. B. <b>EntryID</b>.</span><span class="sxs-lookup"><span data-stu-id="52a3b-116">Binary properties such as <b>EntryID</b>.</span></span></p></td>
<td><p><span data-ttu-id="52a3b-117">Über die integrierte oder Namespace-Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52a3b-117">Supported via built-in or namespace property.</span></span></p></td>
<td><p><span data-ttu-id="52a3b-p102">Nicht unterstützt. In Outlook wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="52a3b-p102">Not supported. Outlook will raise an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52a3b-120">Body-Eigenschaften, einschließlich <b>Body</b> und <b>HTMLBody</b>, sowie die Namespacedarstellung dieser Eigenschaften, einschließlich <b>PR_RTF_COMPRESSED</b>.</span><span class="sxs-lookup"><span data-stu-id="52a3b-120">Body properties, including <b>Body</b> and <b>HTMLBody</b>, and namespace representation of those properties, including <b>PR_RTF_COMPRESSED</b>.</span></span></p></td>
<td><p><span data-ttu-id="52a3b-121">Die <b>Body</b> Eigenschaft wird mit einer Bedingung unterstützt, dass nur die ersten 255 Byte des Werts in einem <b>Table</b>-Objekt gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="52a3b-121">The <b>Body</b> property is supported with a condition that only the first 255 bytes of the value are stored in a <b>Table</b> object.</span></span> <span data-ttu-id="52a3b-122">Andere Eigenschaften, die den Textinhalt in HTML oder RTF darstellen, werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52a3b-122">Other properties that represent the body content in HTML or RTF are not supported.</span></span> <span data-ttu-id="52a3b-123">Da nur die ersten 255 Byte von <b>Body</b> zurückgegeben werden, verwenden Sie die <b>EntryID</b> des Elements in der <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a>-Methode zum Abrufen des Elementobjekts, wenn Sie den gesamten Textinhalt eines Elements in Text oder HTML abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="52a3b-123">Because only the first 255 bytes of <b>Body</b> are returned, if you want to obtain the full body content of an item in text or HTML, use the item’s <b>EntryID</b> in the <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> method to obtain the item object.</span></span> <span data-ttu-id="52a3b-124">Rufen Sie dann den vollständigen Wert von <b>Body</b> über das Elementobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="52a3b-124">Then retrieve the full value of <b>Body</b> through the item object.</span></span></p></td>
<td><p><span data-ttu-id="52a3b-p104">In einem Filter wird nur die in Text dargestellte <b>Body</b>-Eigenschaft unterstützt. Das bedeutet, dass in einem DASL-Filter (DAV Searching and Locating) mit <em>urn:schemas:http-mail:textdescription</em> auf die Eigenschaft verwiesen werden muss und dass Sie keine HTML-Tags im Textkörper filtern können. Sie können die Leistung verbessern, indem Sie im Filter Schlüsselwörter für den Inhaltsindex verwenden, um Zeichenfolgen im Textkörper zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="52a3b-p104">Only the <b>Body</b> property represented in text is supported in a filter. This means that the property must be referenced in a DAV Searching and Locating (DASL) filter as <em>urn:schemas:http-mail:textdescription</em>, and you cannot filter on any HTML tags in the body. To improve performance, use context indexer keywords in the filter to match strings in the body.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52a3b-128">Computer-Eigenschaften, z. B. <b>AutoResolvedWinner</b> und <b>BodyFormat</b>.</span><span class="sxs-lookup"><span data-stu-id="52a3b-128">Computer properties, such as <b>AutoResolvedWinner</b> and <b>BodyFormat</b>.</span></span></p></td>
<td><p><span data-ttu-id="52a3b-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52a3b-129">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="52a3b-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52a3b-130">Not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52a3b-131">Mehrwertige Eigenschaften, z. B. <b>Categories</b>, <b>Children</b>, <b>Companies</b> und <b>VotingOptions</b>.</span><span class="sxs-lookup"><span data-stu-id="52a3b-131">Multivalued properties, such as <b>Categories</b>, <b>Children</b>, <b>Companies</b>, and <b>VotingOptions</b>.</span></span></p></td>
<td><p><span data-ttu-id="52a3b-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="52a3b-132">Supported.</span></span></p></td>
<td><p><span data-ttu-id="52a3b-133">Unterstützt, vorausgesetzt, dass Sie eine DASL-Abfrage unter Verwendung der Namespace-Darstellung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="52a3b-133">Supported, provided that you can create a DASL query by using the namespace representation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52a3b-134">Eigenschaften, die ein Objekt zurückgeben, z. B. <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b> und <b>UserProperties</b></span><span class="sxs-lookup"><span data-stu-id="52a3b-134">Properties that return an object, such as <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b>, and <b>UserProperties</b>.</span></span></p></td>
<td><p><span data-ttu-id="52a3b-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52a3b-135">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="52a3b-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52a3b-136">Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52a3b-p105">In der folgenden Tabelle werden bekannte ungültige Eigenschaften aufgelistet, die Sie nicht mithilfe der **Columns.Add**-Methode dem **Table**-Objekt hinzufügen können. Wenn Sie versuchen, eine Eigenschaft aus dieser Liste hinzuzufügen, wird in Outlook ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="52a3b-p105">The following table lists known invalid properties that cannot be added to the **Table** object by using **Columns.Add**. If you attempt to add a property from this list, Outlook will raise an error.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52a3b-139">AutoResolvedWinner</span><span class="sxs-lookup"><span data-stu-id="52a3b-139">AutoResolvedWinner</span></span></p></td>
<td><p><span data-ttu-id="52a3b-140">BodyFormat</span><span class="sxs-lookup"><span data-stu-id="52a3b-140">BodyFormat</span></span></p></td>
<td><p><span data-ttu-id="52a3b-141">Klasse</span><span class="sxs-lookup"><span data-stu-id="52a3b-141">Class</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52a3b-142">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="52a3b-142">Companies</span></span></p></td>
<td><p><span data-ttu-id="52a3b-143">ContactNames</span><span class="sxs-lookup"><span data-stu-id="52a3b-143">ContactNames</span></span></p></td>
<td><p><span data-ttu-id="52a3b-144">DLName</span><span class="sxs-lookup"><span data-stu-id="52a3b-144">DLName</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52a3b-145">DownloadState</span><span class="sxs-lookup"><span data-stu-id="52a3b-145">DownloadState</span></span></p></td>
<td><p><span data-ttu-id="52a3b-146">FlagIcon</span><span class="sxs-lookup"><span data-stu-id="52a3b-146">FlagIcon</span></span></p></td>
<td><p><span data-ttu-id="52a3b-147">HtmlBody</span><span class="sxs-lookup"><span data-stu-id="52a3b-147">HtmlBody</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52a3b-148">InternetCodePage</span><span class="sxs-lookup"><span data-stu-id="52a3b-148">InternetCodePage</span></span></p></td>
<td><p><span data-ttu-id="52a3b-149">IsConflict</span><span class="sxs-lookup"><span data-stu-id="52a3b-149">IsConflict</span></span></p></td>
<td><p><span data-ttu-id="52a3b-150">IsMarkedAsTask</span><span class="sxs-lookup"><span data-stu-id="52a3b-150">IsMarkedAsTask</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52a3b-151">MeetingWorkspaceURL</span><span class="sxs-lookup"><span data-stu-id="52a3b-151">MeetingWorkspaceURL</span></span></p></td>
<td><p><span data-ttu-id="52a3b-152">MemberCount</span><span class="sxs-lookup"><span data-stu-id="52a3b-152">MemberCount</span></span></p></td>
<td><p><span data-ttu-id="52a3b-153">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="52a3b-153">Permission</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52a3b-154">PermissionService</span><span class="sxs-lookup"><span data-stu-id="52a3b-154">PermissionService</span></span></p></td>
<td><p><span data-ttu-id="52a3b-155">RecurrenceState</span><span class="sxs-lookup"><span data-stu-id="52a3b-155">RecurrenceState</span></span></p></td>
<td><p><span data-ttu-id="52a3b-156">ResponseState</span><span class="sxs-lookup"><span data-stu-id="52a3b-156">ResponseState</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52a3b-157">Saved</span><span class="sxs-lookup"><span data-stu-id="52a3b-157">Saved</span></span></p></td>
<td><p><span data-ttu-id="52a3b-158">Gesendet</span><span class="sxs-lookup"><span data-stu-id="52a3b-158">Sent</span></span></p></td>
<td><p><span data-ttu-id="52a3b-159">Übermittelt</span><span class="sxs-lookup"><span data-stu-id="52a3b-159">Submitted</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52a3b-160">TaskSubject</span><span class="sxs-lookup"><span data-stu-id="52a3b-160">TaskSubject</span></span></p></td>
<td><p><span data-ttu-id="52a3b-161">Ungelesen</span><span class="sxs-lookup"><span data-stu-id="52a3b-161">Unread</span></span></p></td>
<td><p><span data-ttu-id="52a3b-162">VotingOptions</span><span class="sxs-lookup"><span data-stu-id="52a3b-162">VotingOptions</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52a3b-163">Einige berechnete Eigenschaften können nicht zum Spaltensatz für eine Tabelle hinzugefügt werden; im folgenden Codebeispiel wird diese Einschränkung umgangen.</span><span class="sxs-lookup"><span data-stu-id="52a3b-163">Although some computed properties cannot be added to the column set for a table, the following code example works around this limitation.</span></span> <span data-ttu-id="52a3b-164">GetToDoItems verwendet eine DASL-Abfrage, um die Elemente zu beschränken, die in der **Table** angezeigt werde..</span><span class="sxs-lookup"><span data-stu-id="52a3b-164">GetToDoItems uses a DASL query to restrict the items that appear in the **Table**.</span></span> <span data-ttu-id="52a3b-165">Wenn die berechnete Eigenschaft eine Namespacedarstellung hat, wird diese verwendet, um eine DASL-Abfrage erstellen, die das **Table**-Objekt so einschränkt, dass Zeilen für einen bestimmten Wert der berechneten Eigenschaft zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="52a3b-165">If the computed property has a namespace representation, the namespace representation is used to create a DASL query that restricts the **Table** object to return rows for a specified value of the computed property.</span></span> <span data-ttu-id="52a3b-166">GetToDoItems ruft Elemente im Posteingang ab, wobei der Wert der [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\))- Eigenschaft gleich **true** ist; dann werden Werte bestimmten Aufgabeneigenschaften zugewiesen, z. B. [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)) und [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="52a3b-166">GetToDoItems gets items in the Inbox where the value of the [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) property is equal to **true**, and then assigns values to certain task properties such as [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)), and [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)).</span></span> <span data-ttu-id="52a3b-167">Schließlich werden diese Eigenschaften in die Listener der Ablaufverfolgung der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung geschrieben.</span><span class="sxs-lookup"><span data-stu-id="52a3b-167">Finally, those properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="52a3b-168">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="52a3b-168">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="52a3b-169">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="52a3b-169">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="52a3b-170">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="52a3b-170">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="52a3b-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52a3b-171">See also</span></span>

- [<span data-ttu-id="52a3b-172">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="52a3b-172">Search and filter</span></span>](search-and-filter.md)

