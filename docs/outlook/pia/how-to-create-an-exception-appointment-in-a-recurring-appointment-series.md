---
title: Erstellen eines Ausnahmetermins in einer Terminserie
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70e491069fd3f178371e9e8e3e6bcd8dc08e729e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356434"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a><span data-ttu-id="55c9c-102">Erstellen eines Ausnahmetermins in einer Terminserie</span><span class="sxs-lookup"><span data-stu-id="55c9c-102">Create an exception appointment in a recurring appointment series</span></span>

<span data-ttu-id="55c9c-103">In diesem Beispiel wird mithilfe eines [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))-Objekts eine Ausnahme zu einem Standardserienmuster für einen Termin erstellt.</span><span class="sxs-lookup"><span data-stu-id="55c9c-103">This example uses an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object to create an exception to a standard recurrence pattern for an appointment.</span></span>

## <a name="example"></a><span data-ttu-id="55c9c-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="55c9c-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="55c9c-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="55c9c-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="55c9c-106">Nachdem Sie eine Termininstanz einer Terminserie gelöscht oder geändert haben, erstellt Outlook ein [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))-Objekt.</span><span class="sxs-lookup"><span data-stu-id="55c9c-106">Once you delete or change one appointment instance of a recurring appointment, Outlook creates an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object.</span></span> <span data-ttu-id="55c9c-107">Mithilfe dem Exception-Objekt können Sie eine Ausnahme zu einem Standardserienmuster erstellen.</span><span class="sxs-lookup"><span data-stu-id="55c9c-107">The Exception object allows you to create an exception to a standard recurrence pattern.</span></span> <span data-ttu-id="55c9c-108">Die Eigenschaften des Objekts enthalten die Änderungen, die an der Termininstanz vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="55c9c-108">The object’s properties contain the changes that were made to the appointment instance.</span></span> <span data-ttu-id="55c9c-109">Die [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\))-Auflistung enthält alle Exception-Objekte für eine Terminserie und ist mit dem [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekt des Termins verknüpft.</span><span class="sxs-lookup"><span data-stu-id="55c9c-109">The [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) collection contains all of the Exception objects for a recurring appointment, and is associated with the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span>

<span data-ttu-id="55c9c-110">Um das [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt abzurufen, das die Ausnahme zu dem ursprünglichen Serienmuster der Terminserie darstellt, verwenden Sie die [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\))-Eigenschaft von Exception.</span><span class="sxs-lookup"><span data-stu-id="55c9c-110">To get the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents the exception to the original recurrence pattern of the recurring appointment, use the [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) property of the Exception.</span></span> <span data-ttu-id="55c9c-111">Mit den Methoden und Eigenschaften des zurückgegebenen AppointmentItem können Sie die Eigenschaften der Terminausnahme festlegen.</span><span class="sxs-lookup"><span data-stu-id="55c9c-111">By using the methods and properties of the returned AppointmentItem, you can set the properties of the appointment exception.</span></span>

<span data-ttu-id="55c9c-112">Wenn Sie mit Terminserien arbeiten, müssen Sie vorherige Verweise freigeben, neue Verweise auf das Terminserienelement abrufen, bevor Sie das Element öffnen oder bearbeiten, und diese Verweise freigeben, sobald Sie Ihre Änderungen abgeschlossen und gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="55c9c-112">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="55c9c-113">Diese Vorgehensweise gilt für das sich wiederholende **AppointmentItem**-Objekt und alle [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))- oder [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekte.</span><span class="sxs-lookup"><span data-stu-id="55c9c-113">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="55c9c-114">Um einen Verweis in Visual Basic freizugeben, legen Sie dieses vorhandene Objekt auf „Nothing“ fest.</span><span class="sxs-lookup"><span data-stu-id="55c9c-114">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="55c9c-115">Geben Sie in C\# den Arbeitsspeicher für dieses Objekt explizit frei.</span><span class="sxs-lookup"><span data-stu-id="55c9c-115">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="55c9c-p104">Beachten Sie Folgendes: Selbst wenn Sie den Verweis freigegeben haben und versuchen, einen neuen Verweise abzurufen, zeigt der neue Verweis weiterhin auf eine veraltete Kopie des Objekts, wenn immer noch ein aktiver Verweis auf eines der obigen Objekte vorhanden ist, der von einem anderen Add-In oder von Outlook verwendet wird. Deshalb ist es wichtig, dass Sie die Verweise freigeben, sobald Sie die Bearbeitung der Terminserie abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="55c9c-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference, held by another add-in or Outlook, to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="55c9c-118">Im folgenden Codebeispiel ändert CreateExceptionExample den Betreff der im Thema [Suchen nach einem bestimmten Termin in einer Terminserie](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md) erstellten Terminserie. Anschließend wird mit der AppointmentItem-Eigenschaft des resultierenden Exception-Objekts das AppointmentItem-Objekt abgerufen, das der Terminausnahme entspricht.</span><span class="sxs-lookup"><span data-stu-id="55c9c-118">In the following code example, CreateExceptionExample changes the subject of the recurring appointment that was created in the topic [Find a Specific Appointment in a Recurring Appointment Series](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md), and then uses the AppointmentItem property of the resulting Exception object to retrieve the AppointmentItem that corresponds to the appointment exception.</span></span> <span data-ttu-id="55c9c-119">CreateExceptionExample ändert dann die Start- und Endzeit der Terminausnahme.</span><span class="sxs-lookup"><span data-stu-id="55c9c-119">CreateExceptionExample then changes the start and end times of the appointment exception.</span></span>

<span data-ttu-id="55c9c-120">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="55c9c-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="55c9c-121">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="55c9c-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="55c9c-122">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="55c9c-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateExceptionExample()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find(
        "[Subject]='Recurring Appointment DaysOfWeekMask Example'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        try
        {
            Outlook.RecurrencePattern pattern =
                appt.GetRecurrencePattern();
            Outlook.AppointmentItem myInstance =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (myInstance != null)
            {
                myInstance.Subject = "My Exception";
                myInstance.Save();
                Outlook.RecurrencePattern newPattern =
                    appt.GetRecurrencePattern();
                Outlook.Exception myException =
                    newPattern.Exceptions[1];
                if (myException != null)
                {
                    Outlook.AppointmentItem myNewInstance =
                        myException.AppointmentItem;
                    myNewInstance.Start =
                        DateTime.Parse("7/21/2006 1:00 PM");
                    myNewInstance.End =
                        DateTime.Parse("7/21/2006 2:00 PM");
                    myNewInstance.Save();
                }
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="55c9c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55c9c-123">See also</span></span>

- [<span data-ttu-id="55c9c-124">Termine</span><span class="sxs-lookup"><span data-stu-id="55c9c-124">Appointments</span></span>](appointments.md)

