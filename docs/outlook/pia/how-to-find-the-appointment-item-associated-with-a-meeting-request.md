---
title: Suchen des einer Besprechungsanfrage zugeordneten Terminelements
TOCTitle: Find the appointment item associated with a meeting request
ms:assetid: ff356fcf-0980-4567-8570-4bbcb14381e7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184658(v=office.15)
ms:contentKeyID: 55119875
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43bc64dbbed14dae2e185ea89d15b6061858de42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320300"
---
# <a name="find-the-appointment-item-associated-with-a-meeting-request"></a><span data-ttu-id="e8467-102">Suchen des einer Besprechungsanfrage zugeordneten Terminelements</span><span class="sxs-lookup"><span data-stu-id="e8467-102">Find the appointment item associated with a meeting request</span></span>

<span data-ttu-id="e8467-103">In diesem Beispiel wird gezeigt, wie die [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\))-Methode verwendet wird, um den Termin zu finden, der einer Besprechungsanfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e8467-103">This example shows how to use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to find the appointment that is associated with a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="e8467-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e8467-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e8467-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="e8467-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="e8467-106">Ein [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\))-Objekt stellt keinen Termin dar, sondern eine Nachricht mit einer Anfrage, dem Kalender des Empfängers einen Termin hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e8467-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object does not represent an appointment, but a message that contains a request to add an appointment to the recipient’s calendar.</span></span> <span data-ttu-id="e8467-107">Im folgenden Codebeispiel verwendet MeetingRequestExample die [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\))-Methode des **MeetingItem**-Objekts für jedes **MeetingItem**-Objekt aus dem Posteingang des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="e8467-107">In the following code example, MeetingRequestExample uses the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method of the **MeetingItem** object on each **MeetingItem** retrieved from the user’s Inbox.</span></span> <span data-ttu-id="e8467-108">Das zurückgegebene [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt wird dann verwendet, um den Betreff des Termins in die Ablaufverfolgungslistener der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="e8467-108">The returned [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object is then used to write the subject of the appointment to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="e8467-109">Beachten Sie, dass das **GetAssociatedAppointment**-Argument auf **false** festgelegt wird, sodass der Termin dem Kalender des Benutzers nicht hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e8467-109">Note that **GetAssociatedAppointment** argument is set to **false** so that the appointment is not added to the user’s calendar.</span></span>

<span data-ttu-id="e8467-110">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="e8467-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e8467-111">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e8467-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e8467-112">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="e8467-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void MeetingRequestsExample()
{
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(false);
        if (appt != null)
        {
            Debug.WriteLine(appt.Subject);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="e8467-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8467-113">See also</span></span>

- [<span data-ttu-id="e8467-114">Besprechungsanfragen</span><span class="sxs-lookup"><span data-stu-id="e8467-114">Meeting requests</span></span>](meeting-requests.md)

