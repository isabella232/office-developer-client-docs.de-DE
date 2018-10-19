---
title: Erstellen einer Terminserie mithilfe des Standardserienmusters
TOCTitle: Create a recurring appointment by using the default recurrence pattern
ms:assetid: 157bf1ae-2efe-4783-99ea-606722dde204
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184589(v=office.15)
ms:contentKeyID: 55119809
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: be6c024012c02d31af7ce37af6010ba6b40419ce
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406708"
---
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a><span data-ttu-id="afb01-102">Erstellen einer Terminserie mithilfe des Standardserienmusters</span><span class="sxs-lookup"><span data-stu-id="afb01-102">Creates a recurring appointment by using the default recurrence pattern.</span></span>

<span data-ttu-id="afb01-103">Dieses Beispiel zeigt, wie eine Terminserie mithilfe des Standardserienmusters erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="afb01-103">This example shows how to create a recurring appointment by using the default recurrence pattern.</span></span>

## <a name="example"></a><span data-ttu-id="afb01-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="afb01-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="afb01-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="afb01-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="afb01-106">Wenn Sie einen Termin in Outlook erstellen, erstellen Sie ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt.</span><span class="sxs-lookup"><span data-stu-id="afb01-106">When you create an appointment in Outlook, you are creating an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="afb01-107">Bei Ihrem Termin handelt es sich um eine Terminserie, wenn die [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\))-Eigenschaft des AppointmentItem auf „true“ festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="afb01-107">Your appointment is a recurring appointment if the [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) property of the AppointmentItem is set to true.</span></span> <span data-ttu-id="afb01-108">IsRecurring kann nicht direkt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="afb01-108">IsRecurring cannot be set directly.</span></span> 

<span data-ttu-id="afb01-109">Sie können jedoch eine Terminserie mithilfe des [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekts erstellen.</span><span class="sxs-lookup"><span data-stu-id="afb01-109">However, you can create a recurring appointment by using the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="afb01-110">Um eine Terminserie programmgesteuert zu erstellen, erstellen Sie ein **AppointmentItem**-Objekt, rufen Sie die [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\))-Methode des **AppointmentItem**-Objekts auf, und speichern Sie dann das **AppointmentItem**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="afb01-110">To create a recurring appointment programmatically, create an **AppointmentItem** object, call the [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) method of the **AppointmentItem** object, and then save the **AppointmentItem** object.</span></span> <span data-ttu-id="afb01-111">Dadurch wird ein Termin erstellt, der das Standardserienmuster verwendet, und der täglich an dem Tag der Woche auftritt, für den der Termin erstellt wurde. Eine Terminserie weist kein Enddatum auf.</span><span class="sxs-lookup"><span data-stu-id="afb01-111">This creates an appointment that uses the default recurrence pattern, which occurs weekly on the day of the week for which the appointment was created, and has no end date.</span></span> <span data-ttu-id="afb01-112">Mit dem RecurrencePattern-Objekt können Sie Terminserien an angegebenen Intervallen erstellen – täglich, wöchentlich, monatlich oder jährlich.</span><span class="sxs-lookup"><span data-stu-id="afb01-112">The RecurrencePattern object allows you to create recurring appointments at specified intervals—daily, weekly, monthly, or yearly.</span></span> <span data-ttu-id="afb01-113">Wenn Sie keine Intervalle für das RecurrencePattern-Objekt nicht angeben, verwendet Outlook das Standardserienmuster.</span><span class="sxs-lookup"><span data-stu-id="afb01-113">If you do not specify intervals for the RecurrencePattern object, Outlook will use the default recurrence pattern.</span></span>

<span data-ttu-id="afb01-114">Wenn Sie mit Terminserien arbeiten, müssen Sie vorherige Verweise freigeben, neue Verweise auf das Terminserienelement abrufen, bevor Sie das Element öffnen oder bearbeiten, und diese Verweise freigeben, sobald Sie Ihre Änderungen abgeschlossen und gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="afb01-114">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="afb01-115">Diese Vorgehensweise gilt für das sich wiederholende **AppointmentItem**-Objekt und alle [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))- oder [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekte.</span><span class="sxs-lookup"><span data-stu-id="afb01-115">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="afb01-116">Um einen Verweis in Visual Basic freizugeben, legen Sie dieses vorhandene Objekt auf „Nothing“ fest.</span><span class="sxs-lookup"><span data-stu-id="afb01-116">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="afb01-117">Geben Sie in C\# den Arbeitsspeicher für dieses Objekt explizit frei.</span><span class="sxs-lookup"><span data-stu-id="afb01-117">In C#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="afb01-p104">Auch nachdem Sie Ihren Verweis freigegeben und versucht haben, einen neuen Verweis abzurufen, zeigt Ihr neuer Verweis, wenn es noch einen aktiven Verweis (der von einem anderen Add-In oder Outlook aktiviert wurde) auf eines der obigen Objekte gibt, weiter auf eine veraltete Kopie des Objekts. Deshalb müssen Sie stets Ihre Verweise freigeben, sobald Sie mit dem Bearbeiten der Terminserie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="afb01-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="afb01-120">Im folgenden Beispiel erstellt CreateRecurringAppointment ein **AppointmentItem**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="afb01-120">In the following code example,   creates an AppointmentItem object and sets some of its properties.</span></span> <span data-ttu-id="afb01-121">Dann wird GetRecurrencePattern aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="afb01-121">It then calls GetRecurrencePattern.</span></span> <span data-ttu-id="afb01-122">GetRecurrencePattern gibt ein RecurrencePattern-Objekt zurück, und das AppointmentItem wird gespeichert.</span><span class="sxs-lookup"><span data-stu-id="afb01-122">GetRecurrencePattern returns a RecurrencePattern object, and the AppointmentItem is saved.</span></span> <span data-ttu-id="afb01-123">Dadurch wird eine Terminserie erstellt, die das Standardserienmuster verwendet.</span><span class="sxs-lookup"><span data-stu-id="afb01-123">This creates a recurring appointment that uses the default recurrence pattern.</span></span>

<span data-ttu-id="afb01-124">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="afb01-124">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="afb01-125">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="afb01-125">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="afb01-126">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="afb01-126">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateRecurringAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Weekly Extensibility Team Meeting";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    appt.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="afb01-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afb01-127">See also</span></span>

- [<span data-ttu-id="afb01-128">Termine</span><span class="sxs-lookup"><span data-stu-id="afb01-128">Appointments</span></span>](appointments.md)

