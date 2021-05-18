---
title: Suchen und Abrufen von Terminen in einem Zeitbereich
TOCTitle: Search and obtain appointments in a time range
ms:assetid: ce5205ad-6967-4f21-8a9d-503b731dbd40
ms:mtpsurl: https://msdn.microsoft.com/library/Gg619398(v=office.15)
ms:contentKeyID: 55119927
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9088da5f2deb4b3d4ccb1c2bc5409e0ff280ed24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316090"
---
# <a name="search-and-obtain-appointments-in-a-time-range"></a><span data-ttu-id="e7928-102">Suchen und Abrufen von Terminen in einem Zeitbereich</span><span class="sxs-lookup"><span data-stu-id="e7928-102">Search and obtain appointments in a time range</span></span>

<span data-ttu-id="e7928-103">Dieses Beispiel gibt im standardmäßigen Microsoft Outlook-Kalender Termine in einem bestimmten Zeitraum zurück.</span><span class="sxs-lookup"><span data-stu-id="e7928-103">This example returns appointments in a specific time range in the default Microsoft Outlook calendar.</span></span>

## <a name="example"></a><span data-ttu-id="e7928-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e7928-104">Example</span></span>

<span data-ttu-id="e7928-105">Dieses Codebeispiel enthält zwei Methoden: DemoAppointmentsInRange und GetAppointmentsInRange.</span><span class="sxs-lookup"><span data-stu-id="e7928-105">This code example contains two methods: DemoAppointmentsInRange and GetAppointmentsInRange.</span></span> <span data-ttu-id="e7928-106">DemoAppointmentsInRange ruft den Standardkalender für das derzeit angemeldete Outlook-Profil ab, legt einen Datumsbereich von fünf Tagen ab 12:00 Uhr am heutigen Tag fest,</span><span class="sxs-lookup"><span data-stu-id="e7928-106">DemoAppointmentsInRange obtains the default calendar for the current signed-in Outlook profile, sets a date range of 5 days from 12:00 A.M.</span></span> <span data-ttu-id="e7928-107">ruft GetAppointmentsInRange auf, um Termine abzurufen, die in diesen Bereich fallen, und zeigt den Betreff und die Startzeit der einzelnen zurückgegebenen Termine an.</span><span class="sxs-lookup"><span data-stu-id="e7928-107">today, calls GetAppointmentsInRange to obtain appointments that fall in that time range, and displays the subject and start time of each of the returned appointments.</span></span>

<span data-ttu-id="e7928-108">GetAppointmentsInRange akzeptiert einen Outlook-Ordner und die **DateTime**-Werte für die Start- und Endzeit als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="e7928-108">GetAppointmentsInRange accepts an Outlook folder, and the start and end **DateTime** values of the time range as input parameters.</span></span> <span data-ttu-id="e7928-109">Diese Methode verwendet die [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\))-Methode und einen Zeichenfolgenfilter im Jet-Format, der Termine zurückgibt, die innerhalb des angegebenen Zeitraums beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="e7928-109">This method uses the [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method and a string filter in Jet format that returns appointments that start and end within the specified time range.</span></span> <span data-ttu-id="e7928-110">Unter der Annahme, dass \[Start\] und \[End\] die Start- und Endzeiten eines Termins und startTime und endTime die Start- und Endzeiten des angegebenen Zeitraums sind, richtet GetAppointmentsInRange einen Filter ein, der nach Terminen mit `[Start]>=startTime` und `[End]<=endTime` sucht.</span><span class="sxs-lookup"><span data-stu-id="e7928-110">Assuming \[Start\] and \[End\] are the start time and end time of an appointment, and startTime and endTime are the beginning and end time of the specified time range, GetAppointmentsInRange sets up a filter  that looks for appointments with `[Start]>=startTime`, and `[End]<=endTime`.</span></span> <span data-ttu-id="e7928-111">Im folgenden Code ist der Jet-Filter in C\# dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e7928-111">The following code shows the Jet filter in C\#.</span></span>

```csharp
string filter = "[Start] >= '"
    + startTime.ToString("g")
    + "' AND [End] <= '"
    + endTime.ToString("g") + "'";
```

<span data-ttu-id="e7928-112">Vor dem Aufrufen der **Items.Restrict**-Methode zur Suche von Terminen werden von GetAppointmentsInRange zwei weitere Vorgänge ausgeführt, um Terminserien einzuschließen, die in dem angegebenen Zeitraum auftreten:</span><span class="sxs-lookup"><span data-stu-id="e7928-112">Before calling the **Items.Restrict** method to search for appointments, GetAppointmentsInRange does two other things to include recurring appointments that occur in the specified time range:</span></span>

- <span data-ttu-id="e7928-113">Legt die [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\))-Eigenschaft der [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\))-Auflistung fest.</span><span class="sxs-lookup"><span data-stu-id="e7928-113">Sets the [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) property of the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection.</span></span>

- <span data-ttu-id="e7928-114">Sortiert die Terminelemente in dem angegebenen Kalenderordner anhand der [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e7928-114">Sorts the appointment items in the given calendar folder by the [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) property.</span></span>

<span data-ttu-id="e7928-115">Wenn Sie auch an Terminen interessiert sind, die teilweise oder komplett mit dem angegebenen Zeitraum überlappen, können Sie alternativ einen anderen Filter angeben, um weitere Typen von Terminen zurückzugeben (wie in Abbildung 1 dargestellt):</span><span class="sxs-lookup"><span data-stu-id="e7928-115">Alternatively, if you are also interested in appointments that overlap partially or entirely with the specified time range, you would specify a different filter to return additional types of appointments (as shown in Figure 1):</span></span>

- <span data-ttu-id="e7928-116">Termine, die innerhalb des angegebenen Zeitraums beginnen und enden (z. B. Termin A):</span><span class="sxs-lookup"><span data-stu-id="e7928-116">Appointments that start and end within the specified time range (for example, appointment A):</span></span><br/><br/>`[Start]>=startTime and [End]<=endTime`

- <span data-ttu-id="e7928-117">Termine, die vor dem angegebenen Zeitraum beginnen, aber innerhalb des Zeitraums enden (z. B. Termin B):</span><span class="sxs-lookup"><span data-stu-id="e7928-117">Appointments that start before the specified time range but end within the time range (for example, appointment B):</span></span><br/><br/>`[Start]<startTime and [End]<=endTime`

- <span data-ttu-id="e7928-118">Termine, die innerhalb des angegebenen Zeitraums beginnen, aber nach dem Zeitraum enden (z. B. Termin C):</span><span class="sxs-lookup"><span data-stu-id="e7928-118">Appointments that start within the specified time range but end after the time range (for example, appointment C):</span></span><br/><br/>`[Start]>=startTime and [End]>endTime`

- <span data-ttu-id="e7928-119">Termine, die vor dem angegebenen Zeitraum beginnen und nach dem Zeitraum enden (z. B. Termin D):</span><span class="sxs-lookup"><span data-stu-id="e7928-119">Appointments that start before the specified time range and end after the time range (for example, appointment D):</span></span><br/><br/>`[Start]<startTime and [End]>endTime`

<span data-ttu-id="e7928-120">**Abbildung 1. Arten von Terminen, die innerhalb eines Zeitraums auftreten oder sich mit diesem Zeitraum überschneiden**</span><span class="sxs-lookup"><span data-stu-id="e7928-120">**Figure 1. Types of appointments that occur within a time range, or overlap with that time range**</span></span>

![Arten von Terminen, die innerhalb eines Zeitraums auftreten oder sich mit diesem Zeitraum überschneiden.](media/pia-appointment-starttime-endtime.gif)
 

<span data-ttu-id="e7928-122&quot;>In einem beliebigen Zeitraum `startTime<=endTime` würde ein Filter mit `[Start]<=endTime` und `[End]>=startTime` die vorherigen Typen von Terminen in diesem Zeitraum erfassen.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e7928-122&quot;>Because in any time range `startTime<=endTime`, a filter with `[Start]<=endTime` and `[End]>=startTime` would capture the preceding types of appointments in that time range.</span></span>

<span data-ttu-id=&quot;e7928-123&quot;>In C\# können Sie den Jet-Filter wie folgt ausdrücken.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e7928-123&quot;>In C\#, you can express the Jet filter as follows.</span></span>

```csharp
string filter = &quot;[Start] <= '&quot;
    + endTime.ToString(&quot;g")
    + "' AND [End] >= '"
    + startTime.ToString("g") + "'";
```

<span data-ttu-id="e7928-124">Im folgenden Code ist das vollständige Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e7928-124">The following code shows the complete example.</span></span> <span data-ttu-id="e7928-125">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="e7928-125">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e7928-126">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e7928-126">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e7928-127">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="e7928-127">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoAppointmentsInRange()
{
    Outlook.Folder calFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    DateTime start = DateTime.Now;
    DateTime end = start.AddDays(5);
    Outlook.Items rangeAppts = GetAppointmentsInRange(calFolder, start, end);
    if (rangeAppts != null)
    {
        foreach (Outlook.AppointmentItem appt in rangeAppts)
        {
            Debug.WriteLine("Subject: " + appt.Subject 
                + " Start: " + appt.Start.ToString("g"));
        }
    }
}

/// <summary>
/// Get recurring appointments in date range.
/// </summary>
/// <param name="folder"></param>
/// <param name="startTime"></param>
/// <param name="endTime"></param>
/// <returns>Outlook.Items</returns>
private Outlook.Items GetAppointmentsInRange(
    Outlook.Folder folder, DateTime startTime, DateTime endTime)
{
    string filter = "[Start] >= '"
        + startTime.ToString("g")
        + "' AND [End] <= '"
        + endTime.ToString("g") + "'";
    Debug.WriteLine(filter);
    try
    {
        Outlook.Items calItems = folder.Items;
        calItems.IncludeRecurrences = true;
        calItems.Sort("[Start]", Type.Missing);
        Outlook.Items restrictItems = calItems.Restrict(filter);
        if (restrictItems.Count > 0)
        {
            return restrictItems;
        }
        else
        {
            return null;
        }
    }
    catch { return null; }
}
```

## <a name="see-also"></a><span data-ttu-id="e7928-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7928-128">See also</span></span>

- [<span data-ttu-id="e7928-129">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="e7928-129">Search and filter</span></span>](search-and-filter.md)

