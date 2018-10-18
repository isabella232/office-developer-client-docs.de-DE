---
title: Erstellen einer Terminserie mit einem wöchentlichen Muster
TOCTitle: Create a recurring appointment that has a weekly pattern
ms:assetid: 20b46b26-e278-451b-9e35-36683205d164
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184595(v=office.15)
ms:contentKeyID: 55119810
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: bc764fd1be5fb419a0bd4586e7ccba39c6a34dc9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405560"
---
# <a name="create-a-recurring-appointment-that-has-a-weekly-pattern"></a><span data-ttu-id="b46e2-102">Erstellen einer Terminserie mit einem wöchentlichen Muster</span><span class="sxs-lookup"><span data-stu-id="b46e2-102">Create a recurring appointment that has a weekly pattern</span></span>

<span data-ttu-id="b46e2-103">Dieses Beispiel veranschaulicht das Erstellen einer Terminserie mit wöchentlichem Muster (z. B. eines Termins, der montags, mittwochs und freitags ansteht).</span><span class="sxs-lookup"><span data-stu-id="b46e2-103">This example shows how to create a recurring appointment that has a weekly pattern (for example, an appointment that occurs every Monday, Wednesday, and Friday).</span></span>

## <a name="example"></a><span data-ttu-id="b46e2-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b46e2-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b46e2-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="b46e2-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="b46e2-106">Wenn Sie eine neue Terminserie erstellen, basiert das Serienmuster auf der Zeit, die Sie beim Erstellen des Termins angeben.</span><span class="sxs-lookup"><span data-stu-id="b46e2-106">When you create a new recurring appointment, the recurrence pattern is based on the time you specify when you create the appointment.</span></span> <span data-ttu-id="b46e2-107">Wenn Sie beispielsweise einen Termin erstellen, der täglich um 13:00 Uhr stattfinden soll, so wird der Termin jeden Tag nur um 13:00 Uhr wiederholt.</span><span class="sxs-lookup"><span data-stu-id="b46e2-107">For example, if you create an appointment that recurs daily at 1:00 PM, the appointment will recur only at 1:00 PM on a daily basis.</span></span> <span data-ttu-id="b46e2-108">Um das Serienmuster eines Termin zu ändern, legen Sie die Eigenschaften des [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekts des Termins fest.</span><span class="sxs-lookup"><span data-stu-id="b46e2-108">To change the recurrence pattern of an appointment, set the properties of the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="b46e2-109">Legen Sie die [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\))-Eigenschaft des RecurrencePattern-Objekts fest, bevor Sie andere RecurrencePattern-Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="b46e2-109">Set the [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) property of the RecurrencePattern object before setting other RecurrencePattern properties.</span></span> <span data-ttu-id="b46e2-110">Die folgende Tabelle zeigt gültige RecurrencePattern-Eigenschaften für einen angegebenen RecurrenceType (angegeben durch die [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\))-Enumeration).</span><span class="sxs-lookup"><span data-stu-id="b46e2-110">The following table shows valid RecurrencePattern properties for a given RecurrenceType (specified by the [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\)) enumeration).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b46e2-111">OlRecurrenceType-Wert</span><span class="sxs-lookup"><span data-stu-id="b46e2-111">OlRecurrenceType value</span></span></p></th>
<th><p><span data-ttu-id="b46e2-112">Gültige RecurrencePattern-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b46e2-112">Valid RecurrencePattern Properties</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b46e2-113">olRecursDaily</span><span class="sxs-lookup"><span data-stu-id="b46e2-113">olRecursDaily</span></span></p></td>
<td><p><span data-ttu-id="b46e2-114"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></span><span class="sxs-lookup"><span data-stu-id="b46e2-114"><a href="https://msdn.microsoft.com/library/bb644544(v=office.15)"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a></a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)"><a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">Interval</a></a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)"><a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">NoEndDate</a></a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">Occurrences, PatternStartDate, PatternEndDate, StartTime</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b46e2-115">olRecursWeekly</span><span class="sxs-lookup"><span data-stu-id="b46e2-115">olRecursWeekly</span></span></p></td>
<td><p><span data-ttu-id="b46e2-116"><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="b46e2-116">DayOfWeekMask, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b46e2-117">olRecursMonthly</span><span class="sxs-lookup"><span data-stu-id="b46e2-117">olRecursMonthly</span></span></p></td>
<td><p><span data-ttu-id="b46e2-118"><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="b46e2-118"> DayOfMonth , Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b46e2-119">olRecursMonthNth</span><span class="sxs-lookup"><span data-stu-id="b46e2-119">olRecursMonthNth</span></span></p></td>
<td><p><span data-ttu-id="b46e2-120">DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="b46e2-120">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b46e2-121">olRecursYearly</span><span class="sxs-lookup"><span data-stu-id="b46e2-121">olRecursYearly</span></span></p></td>
<td><p><span data-ttu-id="b46e2-122">DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="b46e2-122">DayOfMonth, Duration, EndTime, Interval,  MonthOfYear , NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b46e2-123">olRecursYearNth</span><span class="sxs-lookup"><span data-stu-id="b46e2-123">olRecursYearNth</span></span></p></td>
<td><p><span data-ttu-id="b46e2-124">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="b46e2-124">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b46e2-125">Wenn Sie mit Terminserien arbeiten, müssen Sie vorherige Verweise freigeben, neue Verweise auf das Terminserienelement abrufen, bevor Sie das Element öffnen oder bearbeiten, und diese Verweise freigeben, sobald Sie Ihre Änderungen abgeschlossen und gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="b46e2-125">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="b46e2-126">Diese Vorgehensweise gilt für das sich wiederholende **AppointmentItem**-Objekt und alle [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))- oder [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekte.</span><span class="sxs-lookup"><span data-stu-id="b46e2-126">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="b46e2-127">Um einen Verweis in Visual Basic freizugeben, legen Sie dieses vorhandene Objekt auf „Nothing“ fest.</span><span class="sxs-lookup"><span data-stu-id="b46e2-127">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="b46e2-128">Geben Sie in C\# den Arbeitsspeicher für dieses Objekt explizit frei.</span><span class="sxs-lookup"><span data-stu-id="b46e2-128">In C#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="b46e2-p103">Auch nachdem Sie Ihren Verweis freigegeben und versucht haben, einen neuen Verweis abzurufen, zeigt Ihr neuer Verweis, wenn es noch einen aktiven Verweis (der von einem anderen Add-In oder Outlook aktiviert wurde) auf eines der obigen Objekte gibt, weiter auf eine veraltete Kopie des Objekts. Deshalb müssen Sie stets Ihre Verweise freigeben, sobald Sie mit dem Bearbeiten der Terminserie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="b46e2-p103">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="b46e2-131">Im folgenden Codebeispiel erstellt RecurringAppointmentEveryMondayWednesdayFriday ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt und ruft anschließend [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) auf, um das RecurrencePattern-Objekt des neuen Termins abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b46e2-131">In the following code example,   creates an AppointmentItem object, and then calls GetRecurrencePattern() to get the newly created appointment's RecurrencePattern object.</span></span> <span data-ttu-id="b46e2-132">RecurringAppointmentEveryMondayWednesdayFriday legt dann die Eigenschaften RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime und Subject fest, speichert den Termin, und zeigt anschließend den Termin mit dem folgenden Muster an "Montags, mittwochs und freitags ab dem 10.07.2006 bis zum 25.08.2006 von 14:00 Uhr bis 15:00 Uhr".</span><span class="sxs-lookup"><span data-stu-id="b46e2-132"> then sets the RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime, and Subject properties, saves the appointment, and finally displays the appointment with the pattern "Occurs every Monday, Wednesday, and Friday effective 7/10/2006 until 8/25/2006 from 2:00 PM to 3:00 PM."</span></span>

<span data-ttu-id="b46e2-133">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="b46e2-133">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="b46e2-134">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b46e2-134">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="b46e2-135">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="b46e2-135">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringAppointmentEveryMondayWednesdayFriday()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring Appointment DaysOfWeekMask Example";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursWeekly;
    // Logical OR for DayOfWeekMask creates pattern
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday |
        Outlook.OlDaysOfWeek.olWednesday |
        Outlook.OlDaysOfWeek.olFriday;
    pattern.PatternStartDate = DateTime.Parse("7/10/2006");
    pattern.PatternEndDate = DateTime.Parse("8/25/2006");
    pattern.Duration = 60;
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("3:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="b46e2-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b46e2-136">See also</span></span>

- [<span data-ttu-id="b46e2-137">Termine</span><span class="sxs-lookup"><span data-stu-id="b46e2-137">Appointments</span></span>](appointments.md)

