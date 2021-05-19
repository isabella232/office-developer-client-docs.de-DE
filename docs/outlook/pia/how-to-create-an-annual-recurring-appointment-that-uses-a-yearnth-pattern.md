---
title: Erstellen einer jährlichen Terminserie mit einem jährlichen Muster
TOCTitle: Create an annual recurring appointment that uses a YearNth pattern
ms:assetid: 5fb2ad0b-248c-417d-8868-52e0550d970f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184611(v=office.15)
ms:contentKeyID: 55119811
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc50166674ee7b9699ef8e29c5ff1e54db705ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349504"
---
# <a name="create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern"></a><span data-ttu-id="f7e8d-102">Erstellen einer jährlichen Terminserie mit einem jährlichen Muster</span><span class="sxs-lookup"><span data-stu-id="f7e8d-102">Create an annual recurring appointment that uses a YearNth pattern</span></span>

<span data-ttu-id="f7e8d-103">Dieses Beispiel zeigt, wie ein Termin erstellt wird, dessen jährliches Serienmuster ein bestimmter Tag ist, z. B. der erste Montag im Juni.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-103">This example shows how to create an appointment for which the annual recurrence pattern is a specific day such as the first Monday in June.</span></span>

## <a name="example"></a><span data-ttu-id="f7e8d-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7e8d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f7e8d-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="f7e8d-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="f7e8d-106">Wenn Sie einen jährlichen Termin erstellen möchten, der an einem bestimmten Tag der Woche in einen bestimmten Monat (z. B. am ersten Montag im Juni) stattfinden soll, müssen Sie YearNth-Serien verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-106">If you want to create an annual appointment that recurs on a specific day of the week during a specific month (for example, the first Monday in June), you must use YearNth recurrences.</span></span> <span data-ttu-id="f7e8d-107">Um eine YearNth-Serie festzulegen, müssen Sie zunächst die [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\))-Eigenschaft des [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekts auf „olRecursYearNth“ festlegen.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-107">To set a YearNth recurrence, you must first set the [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) property of the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object to olRecursYearNth.</span></span> <span data-ttu-id="f7e8d-108">Legen Sie dann die [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\))-Eigenschaft fest, um anzugeben, an welchem Tag der Woche der Termin wiederholt werden soll, und die [Instanz](https://msdn.microsoft.com/library/bb645269\(v=office.15\))-Eigenschaft, um das n-te Vorkommen an dem angegebenen Tag der Woche (z. B. am dritten Dienstag) in einem bestimmten Monat für das jährliche Muster anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-108">Then set the [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)) property to specify on which day of the week the appointment should recur, and the [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)) property to specify the Nth occurrence of the specified day of the week (for example, the third Tuesday) during a specified month for the yearly pattern.</span></span>

<span data-ttu-id="f7e8d-109">Wenn Sie mit Terminserien arbeiten, müssen Sie vorherige Verweise freigeben, neue Verweise auf das Terminserienelement abrufen, bevor Sie das Element öffnen oder bearbeiten, und diese Verweise freigeben, sobald Sie Ihre Änderungen abgeschlossen und gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-109">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="f7e8d-110">Diese Vorgehensweise gilt für das sich wiederholende **AppointmentItem**-Objekt und alle [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))- oder [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekte.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-110">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="f7e8d-111">Um einen Verweis in Visual Basic freizugeben, legen Sie dieses vorhandene Objekt auf „Nothing“ fest.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-111">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="f7e8d-112">Geben Sie in C\# den Arbeitsspeicher für dieses Objekt explizit frei.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-112">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="f7e8d-p103">Auch nachdem Sie Ihren Verweis freigegeben und versucht haben, einen neuen Verweis abzurufen, zeigt Ihr neuer Verweis, wenn es noch einen aktiven Verweis (der von einem anderen Add-In oder Outlook aktiviert wurde) auf eines der obigen Objekte gibt, weiter auf eine veraltete Kopie des Objekts. Deshalb müssen Sie stets Ihre Verweise freigeben, sobald Sie mit dem Bearbeiten der Terminserie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-p103">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="f7e8d-115">Im folgenden Codebeispiel erstellt RecurringYearNthAppointment einen Termin mit einem YearNth-Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-115">In the following code example, RecurringYearNthAppointment creates an appointment that has a YearNth recurrence pattern.</span></span> <span data-ttu-id="f7e8d-116">RecurringYearNthAppointment erstellt zunächst eine Terminserie, indem ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-116">RecurringYearNthAppointment first creates a recurring appointment by creating an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="f7e8d-117">Als Nächstes wird das Serienmuster des Termins mithilfe der [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\))-Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-117">Next, it gets the appointment’s recurrence pattern by using the [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) method.</span></span> <span data-ttu-id="f7e8d-118">Dann werden die folgenden RecurrencePattern-Eigenschaften festgelegt: RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)) und [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f7e8d-118">It then sets the following RecurrencePattern properties: RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)), and [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)).</span></span> <span data-ttu-id="f7e8d-119">Die MonthOfYear-Eigenschaft akzeptiert einen numerischen Wert von 1 bis 12, wobei jede Zahl den entsprechenden Monat darstellt.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-119">The MonthOfYear property can take a numerical value of 1 through 12, where each number represents the corresponding month.</span></span> <span data-ttu-id="f7e8d-120">Nachdem die Eigenschaften festgelegt wurden speichert RecurringYearNthAppointment den Termin und zeigt ihn dann mit dem Muster „Tritt am ersten Montag des Monats Juni ab dem 1.6.2007 bis 6.6.2016 von 14:00 – 17:00 Uhr auf“.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-120">Once the properties are set, RecurringYearNthAppointment saves the appointment, and then displays it with the pattern "Occurs the first Monday of June effective 6/1/2007 until 6/6/2016 from 2:00 PM to 5:00 PM."</span></span>

<span data-ttu-id="f7e8d-121">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="f7e8d-122">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="f7e8d-123">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="f7e8d-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringYearNthAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring YearNth Appointment";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearNth;
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday;
    pattern.MonthOfYear = 6;
    pattern.Instance = 1;
    pattern.Occurrences = 10;
    pattern.Duration = 180;
    pattern.PatternStartDate = DateTime.Parse("6/1/2007");
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("5:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="f7e8d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7e8d-124">See also</span></span>

- [<span data-ttu-id="f7e8d-125">Termine</span><span class="sxs-lookup"><span data-stu-id="f7e8d-125">Appointments</span></span>](appointments.md)

