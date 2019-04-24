---
title: Erstellen einer Erinnerung für ein Terminelement
TOCTitle: Create a reminder for an appointment item
ms:assetid: 85e772f0-65ac-4abc-8286-9099882a2400
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184623(v=office.15)
ms:contentKeyID: 55119814
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1f5f31c480f31b01e53fec9651c8154765b581a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349497"
---
# <a name="create-a-reminder-for-an-appointment-item"></a><span data-ttu-id="90b51-102">Erstellen einer Erinnerung für ein Terminelement</span><span class="sxs-lookup"><span data-stu-id="90b51-102">Create a reminder for an appointment item</span></span>

<span data-ttu-id="90b51-103">Dieses Beispiel zeigt, wie Sie mithilfe der [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\))-Eigenschaft eine Erinnerung für einen Termin erstellen.</span><span class="sxs-lookup"><span data-stu-id="90b51-103">This example shows how to use the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property to create a reminder for an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="90b51-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="90b51-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="90b51-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="90b51-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="90b51-106">Outlook bietet eine Möglichkeit zum Festlegen einer Erinnerung für einen Termin mithilfe der [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\))-Eigenschaft des [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekts.</span><span class="sxs-lookup"><span data-stu-id="90b51-106">Outlook provides a way to set a reminder for an appointment by using the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="90b51-107">Diese Eigenschaft gibt an, ob eine Erinnerung für den Termin erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="90b51-107">This property indicates whether a reminder has been created for the appointment.</span></span> <span data-ttu-id="90b51-108">Durch Festlegen der ReminderSet-Eigenschaft auf „true“ wird eine Erinnerung erstellt; wenn diese Eigenschaft auf „false“ festgelegt wird, wird die Erinnerung entfernt.</span><span class="sxs-lookup"><span data-stu-id="90b51-108">Setting the ReminderSet property to true creates a reminder, and setting it to false removes the reminder.</span></span>

<span data-ttu-id="90b51-109">Im folgenden Codebeispiel erstellt ReminderExample eine Erinnerung in einem privaten Termin für eine Weinverkostung in Napa, Kalifornien, und es wird festgelegt, dass die Erinnerung zwei Stunden vor Beginn des Termins auftritt.</span><span class="sxs-lookup"><span data-stu-id="90b51-109">In the following code example, ReminderExample creates a reminder on a private appointment for wine tasting in Napa, California, and sets the reminder to occur two hours before the appointment starts.</span></span> <span data-ttu-id="90b51-110">Zuerst erstellt ReminderExample das Outlook-Objekt **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="90b51-110">First, ReminderExample creates an Outlook **AppointmentItem** object.</span></span> <span data-ttu-id="90b51-111">Dann wird die [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\))-Eigenschaft für das Element auf [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90b51-111">It then sets the [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) property for the item to [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)).</span></span> <span data-ttu-id="90b51-112">Dies weist darauf hin, dass der Termin ein privater Termin ist.</span><span class="sxs-lookup"><span data-stu-id="90b51-112">This indicates that the appointment is a private appointment.</span></span> <span data-ttu-id="90b51-113">Nach dem Festlegen anderer Eigenschaften des Termins, z. B. [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\))- und [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\))zeiten, legt ReminderExample die [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\))-Eigenschaft so fest, dass die Anzahl von Minuten angegeben wird, die die Erinnerung vor dem Beginn des Termins angezeigt wird. </span><span class="sxs-lookup"><span data-stu-id="90b51-113">After setting other properties of the appointment, such as [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) times, ReminderExample sets the [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) property to indicate the number of minutes that the reminder will appear before the start of the appointment.</span></span> <span data-ttu-id="90b51-114">In diesem Fall wird ReminderMinutesBeforeStart auf 120 Minuten (2 Stunden) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90b51-114">In this case, ReminderMinutesBeforeStart is set to 120 minutes (two hours).</span></span>

<span data-ttu-id="90b51-115">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="90b51-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="90b51-116">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="90b51-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="90b51-117">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="90b51-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void ReminderExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Wine Tasting";
    appt.Location = "Napa CA";
    appt.Sensitivity = Outlook.OlSensitivity.olPrivate;
    appt.Start = DateTime.Parse("10/21/2006 10:00 AM");
    appt.End = DateTime.Parse("10/21/2006 3:00 PM");
    appt.ReminderSet = true;
    appt.ReminderMinutesBeforeStart = 120;
    appt.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="90b51-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90b51-118">See also</span></span>

- [<span data-ttu-id="90b51-119">Termine</span><span class="sxs-lookup"><span data-stu-id="90b51-119">Appointments</span></span>](appointments.md)

