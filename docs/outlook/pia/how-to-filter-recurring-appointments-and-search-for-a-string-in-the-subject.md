---
title: Filtern von Terminserien und Suchen nach einer Zeichenfolge im Betreff
TOCTitle: Filter recurring appointments and search for a string in the subject
ms:assetid: 997186aa-5264-4b19-bed6-51c38831c03d
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611267(v=office.15)
ms:contentKeyID: 55119891
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1815cc4e1314a848229f6187925377809e7200cf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406302"
---
# <a name="filter-recurring-appointments-and-search-for-a-string-in-the-subject"></a><span data-ttu-id="93035-102">Filtern von Terminserien und Suchen nach einer Zeichenfolge im Betreff</span><span class="sxs-lookup"><span data-stu-id="93035-102">Filter recurring appointments and search for a string in the subject</span></span>

<span data-ttu-id="93035-103">In diesem Beispiel werden Terminserien in einem Kalenderordner gefiltert, die in einen bestimmten Datumsbereich fallen. Anschließend wird auf zwei Arten nach der Zeichenfolge "office" im Betreff gesucht.</span><span class="sxs-lookup"><span data-stu-id="93035-103">This example filters recurring appointments that fall within a date range in a Calendar folder, and then searches in two ways for the string "office" in the subject.</span></span>

## <a name="example"></a><span data-ttu-id="93035-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="93035-104">Example</span></span>

<span data-ttu-id="93035-105">Zum Filtern von Terminserien verwendet dieser Beispielcode die [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\))-Auflistung anstelle des [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekts, da das **Table**-Objekt nur die Masterserientermine zurückgibt und keine Terminserien in dem Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="93035-105">To filter recurring appointments, this code sample uses the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection instead of the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, because the **Table** object returns only the master series appointments and does not include recurring items in the folder.</span></span> <span data-ttu-id="93035-106">Um Terminserien beim Aufrufen der [Find(String)](https://msdn.microsoft.com/library/bb646289\(v=office.15\))- oder der [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\))-Methode einzuschließen, legt das Codebeispiel die [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\))-Eigenschaft der **Items**-Auflistung fest und sortiert dann Termine im Ordner anhand der [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="93035-106">To include recurring appointments when calling the [Find(String)](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) or [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method, the code sample sets the [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) property of the **Items** collection, and then sorts appointments in the folder by their [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) property.</span></span> <span data-ttu-id="93035-107">Dann wird eine Jet-Abfrage verwendet, um Start- und Enddaten für die Termine anzugeben.</span><span class="sxs-lookup"><span data-stu-id="93035-107">It then uses a Jet query to specify start and end dates for the recurrences.</span></span>

<span data-ttu-id="93035-108">Nach dem Abrufen einer **Items**-Auflistung von Terminserienelementen, die in den angegebenen Datumsbereich fallen, führt das Codebeispiel zwei oder mehr Suchvorgänge mithilfe von DASL-Abfragen (DAV Searching and Locating) aus.</span><span class="sxs-lookup"><span data-stu-id="93035-108">After obtaining an **Items** collection of recurring appointment items that fall within the specified range of dates, the code sample carries out two more searches using DAV Searching and Locating (DASL) queries.</span></span> <span data-ttu-id="93035-109">Bei der ersten Suche wird **Items.Find**, [FindNext](https://msdn.microsoft.com/library/bb623799\(v=office.15\)) und das **like**-Schlüsselwort verwendet, um nach Elementen zu suchen, die „office“ als Teilzeichenfolge im Betreff enthalten.</span><span class="sxs-lookup"><span data-stu-id="93035-109">The first search uses **Items.Find**, [FindNext](https://msdn.microsoft.com/library/bb623799\(v=office.15\)), and the **like** keyword to search for items that have "office" as a substring in the subject.</span></span> <span data-ttu-id="93035-110">Bei der zweiten Suche wird die **Items.Restrict**-Methode und das **ci\_startswith**-Schlüsselwort verwendet, um nach Elementen zu suchen, deren Betreff mit „office“ beginnt.</span><span class="sxs-lookup"><span data-stu-id="93035-110">The second search uses the **Items.Restrict** method and the **ci\_startswith** keyword to search for items that have subjects beginning with "office."</span></span>

<span data-ttu-id="93035-111">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="93035-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="93035-112">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="93035-112">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="93035-113">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="93035-113">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SearchRecurringAppointments()
    Dim appt As Outlook.AppointmentItem = Nothing
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar), _
        Outlook.Folder)
    ' Set start value
    Dim startTime As DateTime = New DateTime(2006, 8, 9, 0, 0, 0)
    ' Set end value
    Dim endTime As DateTime = New DateTime(2006, 12, 14, 0, 0, 0)
    ' Initial restriction is Jet query for date range
    Dim filter1 As String = "[Start] >= '" & startTime.ToString("g") _
        & "' AND [End] <= '" & endTime.ToString("g") & "'"
    Dim calendarItems As Outlook.Items = folder.Items.Restrict(filter1)
    calendarItems.IncludeRecurrences = True
    calendarItems.Sort("[Start]")
    ' Must use 'like' comparison for Find/FindNext
    Dim filter2 As String
    filter2 = "@SQL=" & _
        Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & _
        " like '%Office%'"
    ' Create DASL query for additional Restrict method
    Dim filter3 As String
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter3 = "@SQL=" & _
            Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & " _
            ci_startswith 'Office'"
    Else
        filter3 = "@SQL=" & _
            Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & " _
            like '%Office%'"
    End If
    ' Use Find and FindNext methods
    appt = CType(calendarItems.Find(filter2), Outlook.AppointmentItem)
    While Not (appt Is Nothing)
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(appt.Subject)
        sb.AppendLine("Start: " & appt.Start)
        sb.AppendLine("End: " & appt.End)
        Debug.WriteLine(sb.ToString())
        ' Find the next appointment
        appt = CType(calendarItems.FindNext(), Outlook.AppointmentItem)
    End While
    ' Restrict calendarItems with DASL query
    Dim restrictedItems As Outlook.Items = _
        calendarItems.Restrict(filter3)
    For Each apptItem As Outlook.AppointmentItem In restrictedItems
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(apptItem.Subject)
        sb.AppendLine("Start: " & apptItem.Start)
        sb.AppendLine("End: " & apptItem.End)
        sb.AppendLine()
        Debug.WriteLine(sb.ToString())
    Next
End Sub
```


```csharp
private void SearchRecurringAppointments()
{
    Outlook.AppointmentItem appt = null;
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    // Set start value
    DateTime start =
        new DateTime(2006, 8, 9, 0, 0, 0);
    // Set end value
    DateTime end =
        new DateTime(2006, 12, 14, 0, 0, 0);
    // Initial restriction is Jet query for date range
    string filter1 = "[Start] >= '" +
        start.ToString("g")
        + "' AND [End] <= '" +
        end.ToString("g") + "'";
    Outlook.Items calendarItems = folder.Items.Restrict(filter1);
    calendarItems.IncludeRecurrences = true;
    calendarItems.Sort("[Start]", Type.Missing);
    // Must use 'like' comparison for Find/FindNext
    string filter2;
    filter2 = "@SQL="
        + "\"" + "urn:schemas:httpmail:subject" + "\""
        + " like '%Office%'";
    // Create DASL query for additional Restrict method
    string filter3;
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter3 = "@SQL="
            + "\"" + "urn:schemas:httpmail:subject" + "\""
            + " ci_startswith 'Office'";
    }
    else
    {
        filter3 = "@SQL="
            + "\"" + "urn:schemas:httpmail:subject" + "\""
            + " like '%Office%'";
    }
    // Use Find and FindNext methods
    appt = calendarItems.Find(filter2)
        as Outlook.AppointmentItem;
    while (appt != null)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(appt.Subject);
        sb.AppendLine("Start: " + appt.Start);
        sb.AppendLine("End: " + appt.End);
        Debug.WriteLine(sb.ToString());
        // Find the next appointment
        appt = calendarItems.FindNext()
            as Outlook.AppointmentItem;
    }
    // Restrict calendarItems with DASL query
    Outlook.Items restrictedItems =
        calendarItems.Restrict(filter3);
    foreach (Outlook.AppointmentItem apptItem in restrictedItems)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(apptItem.Subject);
        sb.AppendLine("Start: " + apptItem.Start);
        sb.AppendLine("End: " + apptItem.End);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="93035-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93035-114">See also</span></span>

- [<span data-ttu-id="93035-115">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="93035-115">Search and Filter</span></span>](search-and-filter.md)

