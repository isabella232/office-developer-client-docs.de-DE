---
title: Suchen nach einem bestimmten Termin in einer Terminserie
TOCTitle: Find a specific appointment in a recurring appointment series
ms:assetid: 01f55f04-7245-4325-a354-50a6eb270a31
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184586(v=office.15)
ms:contentKeyID: 55119812
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 19502895996d4777f2d1a6887aa80883a5398a09
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722977"
---
# <a name="find-a-specific-appointment-in-a-recurring-appointment-series"></a><span data-ttu-id="7d9a7-102">Suchen nach einem bestimmten Termin in einer Terminserie</span><span class="sxs-lookup"><span data-stu-id="7d9a7-102">Find a specific appointment in a recurring appointment series</span></span>

<span data-ttu-id="7d9a7-103">Dieses Beispiel zeigt, wie ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt zurückgegeben wird, das einen bestimmten Termin in einer Terminserie darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-103">This example shows how to return an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a specific appointment in a recurring appointment series.</span></span>

## <a name="example"></a><span data-ttu-id="7d9a7-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7d9a7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7d9a7-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="7d9a7-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="7d9a7-106">Verwenden Sie zum Auffinden einer Instanz einer Terminserie für ein angegebenes Datum mit angegebener Uhrzeit die [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) -Methode des [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) -Objekts, um ein **AppointmentItem**-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-106">To find an instance of a recurring appointment that occurs at a specified date and time, use the [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) method of the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object to return an **AppointmentItem** object.</span></span>

<span data-ttu-id="7d9a7-107">Wenn Sie mit Terminserien arbeiten, müssen Sie vorherige Verweise freigeben, neue Verweise auf das Terminserienelement abrufen, bevor Sie das Element öffnen oder bearbeiten, und diese Verweise freigeben, sobald Sie Ihre Änderungen abgeschlossen und gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-107">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="7d9a7-108">Diese Vorgehensweise gilt für das sich wiederholende **AppointmentItem**-Objekt und alle [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))- oder [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekte.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-108">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="7d9a7-109">Um einen Verweis in Visual Basic freizugeben, legen Sie dieses vorhandene Objekt auf „Nothing“ fest.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-109">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="7d9a7-110">Geben Sie in C\# den Arbeitsspeicher für dieses Objekt explizit frei.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-110">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="7d9a7-p102">Auch nachdem Sie Ihren Verweis freigegeben und versucht haben, einen neuen Verweis abzurufen, zeigt Ihr neuer Verweis, wenn es noch einen aktiven Verweis (der von einem anderen Add-In oder Outlook aktiviert wurde) auf eines der obigen Objekte gibt, weiter auf eine veraltete Kopie des Objekts. Deshalb müssen Sie stets Ihre Verweise freigeben, sobald Sie mit dem Bearbeiten der Terminserie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-p102">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="7d9a7-113">Im folgenden Codebeispiel verwendet CheckOccurrenceExample die Terminserie, die im Codebeispiel in [Erstellen einer Terminserie mit wöchentlichem Muster](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-113">In the following code example, CheckOccurrenceExample uses the recurring appointment that was created in the code example in [Create a Recurring Appointment That Has a Weekly Pattern](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md).</span></span> <span data-ttu-id="7d9a7-114">Dann wird die GetOccurrence-Methode aufgerufen, um zu ermitteln, ob die Terminserie an dem angegebenen Datum und zu der angegebenen Uhrzeit beginnt.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-114">It then calls the GetOccurrence method to determine whether the recurring appointment starts on the specified date and time.</span></span> <span data-ttu-id="7d9a7-115">Zum Sicherstellen, dass die Prozedur fortgesetzt wird, auch wenn die bereitgestellten Informationen nicht dem Startdatum und der Startuhrzeit einer Instanz der Terminserie entsprechen, verwendet das Beispiel einen try…catch-Block.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-115">To ensure that the procedure will continue even if the provided information does not match the start date and time of an instance of the recurring appointment, the example uses a try…catch block.</span></span> <span data-ttu-id="7d9a7-116">Nach Aufrufen der GetOccurrence-Methode für jeden Termin in der Terminserie testet CheckOccurrenceExample die singleAppt-Variable, um zu bestimmen, ob sie auf einen NULL-Verweis festgelegt ist, was bedeutet, dass die Methode keinen Erfolg hatte und kein **AppointmentItem**-Objekt zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-116">After calling the GetOccurrence method on every appointment in the recurring appointment series, CheckOccurrenceExample tests the singleAppt variable to determine whether it is set to a null reference, indicating that the method failed and did not return an **AppointmentItem** object.</span></span>

<span data-ttu-id="7d9a7-117">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7d9a7-118">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7d9a7-119">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="7d9a7-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CheckOccurrenceExample()
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
            Outlook.AppointmentItem singleAppt =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (singleAppt != null)
            {
                Debug.WriteLine("7/21/2006 2:00 PM occurrence found.");
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="7d9a7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d9a7-120">See also</span></span>

- [<span data-ttu-id="7d9a7-121">Termine</span><span class="sxs-lookup"><span data-stu-id="7d9a7-121">Appointments</span></span>](appointments.md)

