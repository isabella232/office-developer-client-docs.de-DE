---
title: Erstellen eines Termins, der ein ganztägiges Ereignis darstellt
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5065395afe39247f8113bc5223b0e3e403a02fa
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710825"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a><span data-ttu-id="89b11-102">Erstellen eines Termins, der ein ganztägiges Ereignis darstellt</span><span class="sxs-lookup"><span data-stu-id="89b11-102">Create an appointment that is an all-day event</span></span>

<span data-ttu-id="89b11-103">In diesem Beispiel wird veranschaulicht, wie die [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\))-Eigenschaft verwendet wird, um einen Termin als ganztägiges Ereignis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="89b11-103">This example shows how use the [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) property to create an appointment that is an all-day event.</span></span>

## <a name="example"></a><span data-ttu-id="89b11-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="89b11-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="89b11-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="89b11-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="89b11-p101">Ein Ereignis unterscheidet sich insofern von einem normalen Termin, als es sich um eine Aktivität von mindestens 24-stündiger Dauer handelt. Beispiele für Ereignisse sind Messen, Seminare oder Urlaube. Ereignisse und jährliche Ereignisse werden nicht als belegte Zeiträume im Kalender des Benutzers angezeigt. Sie werden vielmehr als Banner dargestellt. Sie können die Banner am oberen Rand einer Tages- oder Wochenansicht des Kalenders sehen. Für einen ganztägigen Termin wird die Zeit des Benutzers anderen Personen gegenüber standardmäßig als gebucht angezeigt, für ein Ereignis oder jährliches Ereignis wird sie dagegen als frei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89b11-p101">An event is different from a regular appointment because it is an activity that lasts 24 hours or longer. Examples of events include trade shows, seminars, or vacations. Events and annual events do not appear as occupied blocks of time in the user’s calendar. Instead, they appear as banners. You can see the banners at the top of a calendar day or week view. For an all-day appointment, by default, the user’s time is displayed as busy when viewed by other people, but the user’s time is displayed as free for an event or annual event.</span></span>

<span data-ttu-id="89b11-112">Um ein ganztägiges Ereignis programmgesteuert zu erstellen, legen Sie die [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\))-Eigenschaft des [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekts auf „true“ fest.</span><span class="sxs-lookup"><span data-stu-id="89b11-112">To create an all-day event programmatically, set the [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) property of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object to true.</span></span> <span data-ttu-id="89b11-113">Legen Sie dann die Eigenschaften [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) und [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) des AppointmentItem fest.</span><span class="sxs-lookup"><span data-stu-id="89b11-113">Then set the [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) properties of the AppointmentItem.</span></span> <span data-ttu-id="89b11-114">Wenn Sie die AllDayEvent-Eigenschaft auf „true“ festlegen und die Start- und End-Eigenschaft nicht festlegen, findet das Ereignis heute statt, und es handelt sich um einen Termin, sodass der Status „Gebucht“ in Ihrem Kalender angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="89b11-114">If you set the AllDayEvent property to true and do not set the Start and End properties, the event will occur today, and it will be an appointment, showing a busy status on your calendar.</span></span> <span data-ttu-id="89b11-115">Sie müssen die Start- und End-Eigenschaft festlegen, wenn das Ereignis an einem Datum in der Zukunft stattfinden soll.</span><span class="sxs-lookup"><span data-stu-id="89b11-115">You must set the Start and End properties if you want the event to occur on a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="89b11-116">Um den Termin als ganztägiges Ereignis festzulegen, müssen Sie die Start-Eigenschaft auf 24:00 Uhr (Mitternacht)</span><span class="sxs-lookup"><span data-stu-id="89b11-116">To make the appointment an all-day event, you must set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="89b11-117">an dem Tag festlegen, an dem das Ereignis beginnen soll, und Sie müssen die End-Eigenschaft auf 24 Uhr</span><span class="sxs-lookup"><span data-stu-id="89b11-117">(midnight) on the day you want the event to begin, and set End property to 12:00 A.M.</span></span> <span data-ttu-id="89b11-118">an dem Tag festlegen, an dem das Ereignis enden soll.</span><span class="sxs-lookup"><span data-stu-id="89b11-118">on the day after you want the event to end.</span></span> <span data-ttu-id="89b11-119">Wenn Sie die Start- oder Endzeit auf einen anderen Datums- oder Zeitwert als 24 Uhr festlegen, wird der Termin ein mehrtägiger Termin und kein ganztägiges Ereignis.</span><span class="sxs-lookup"><span data-stu-id="89b11-119">If you set the Start or End time to a date and time value other than 12:00 A.M., the appointment will become a multiday appointment instead of an all-day event.</span></span> 
>
> <span data-ttu-id="89b11-120">Wenn die Dauer beispielsweise nur ein Tag ist, legen Sie die Start-Eigenschaft auf 24 Uhr</span><span class="sxs-lookup"><span data-stu-id="89b11-120">For example, if your event duration is only one day, set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="89b11-121">an dem Tag fest, an dem das Ereignis beginnen soll, und legen die End-Eigenschaft auf 24 Uhr</span><span class="sxs-lookup"><span data-stu-id="89b11-121">on the day you want the event to begin, and set the End property to 12:00 A.M.</span></span> <span data-ttu-id="89b11-122">am folgenden Tag fest.</span><span class="sxs-lookup"><span data-stu-id="89b11-122">on the following day.</span></span> <span data-ttu-id="89b11-123">Sie sollten die End-Eigenschaft immer auf 12:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="89b11-123">You should always set the End property to 12:00 A.M.</span></span> <span data-ttu-id="89b11-124">an einem Datum festlegen, das einen Tag nach dem Startdatum liegt.</span><span class="sxs-lookup"><span data-stu-id="89b11-124">on a date that is more than one day after the start date.</span></span>

<span data-ttu-id="89b11-p105">Im folgenden Codebeispiel wird von AllDayEventExample ein ganztägiges Ereignis erstellt, das am 11. Juni 2007 beginnt und am 15. Juni 2007 endet. Beachten Sie, dass die End-Eigenschaft für den Termin auf 00:00 Uhr am 16. Juni 2007 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="89b11-p105">In the following code example, AllDayEventExample creates an all-day event that begins on June 11, 2007, and ends on June 15, 2007. Note that the End property for the appointment is set to 12:00 A.M. on June 16, 2007.</span></span>

<span data-ttu-id="89b11-128">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="89b11-128">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="89b11-129">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="89b11-129">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="89b11-130">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="89b11-130">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AllDayEventExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Developer's Conference";
    appt.AllDayEvent = true;
    appt.Start = DateTime.Parse("6/11/2007 12:00 AM");
    appt.End = DateTime.Parse("6/16/2007 12:00 AM");
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="89b11-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89b11-131">See also</span></span>

- [<span data-ttu-id="89b11-132">Termine</span><span class="sxs-lookup"><span data-stu-id="89b11-132">Appointments</span></span>](appointments.md)

