---
title: Automatisches Annehmen einer Besprechungsanfrage
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f546b4e2de2a77034fdfeca4d685d7b7f909f40a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359703"
---
# <a name="automatically-accept-a-meeting-request"></a><span data-ttu-id="75fc7-102">Automatisches Annehmen einer Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="75fc7-102">Automatically accept a meeting request</span></span>

<span data-ttu-id="75fc7-103">Dieses Beispiel verwendet die [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\))-Methode, um eine Besprechungsanfrage automatisch anzunehmen.</span><span class="sxs-lookup"><span data-stu-id="75fc7-103">This example shows how to use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method to automatically accept a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="75fc7-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="75fc7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="75fc7-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="75fc7-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="75fc7-106">Ein [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\))-Objekt stellt eine Anfrage zum Hinzufügen eines Termins, dargestellt durch ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt, zum Kalender eines Empfängers dar.</span><span class="sxs-lookup"><span data-stu-id="75fc7-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object represents a request to add an appointment, represented by an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, to a recipient’s calendar.</span></span> <span data-ttu-id="75fc7-107">In diesem Beispiel wird gezeigt, wie die [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\))-Methode verwendet wird, um den **AppointmentItem** abzurufen, der einer Besprechungsanfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="75fc7-107">To respond to a meeting request, use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to obtain the **AppointmentItem** associated with the meeting request.</span></span> <span data-ttu-id="75fc7-108">Verwenden Sie dann die [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\))-Methode des **AppointmentItem**-Elements zum Benachrichtigen des Besprechungsorganisators darüber, ob die Besprechung zum Kalender des Empfängers als "Angenommen", "Abgelehnt" oder "Mit Vorbehalt" hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="75fc7-108">Then use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the **AppointmentItem** to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient’s calendar.</span></span> <span data-ttu-id="75fc7-109">Die **Respond**-Methode akzeptiert drei Parameter.</span><span class="sxs-lookup"><span data-stu-id="75fc7-109">The **Respond** method accepts three parameters.</span></span> 

<span data-ttu-id="75fc7-110">Der *Response*-Parameter gibt an, ob die Antwort "Angenommen", "Abgelehnt" oder "Mit Vorbehalt" lautet.</span><span class="sxs-lookup"><span data-stu-id="75fc7-110">The *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="75fc7-111">Die Parameter fNoUI und fAdditionalTextDialog sind **bool**-Werte, die bestimmen, ob die Antwort gesendet wird und ob der Benutzer die Antwort bearbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="75fc7-111">The fNoUI and fAdditionalTextDialog parameters are **bool** values that determine whether a response will be sent, and whether the user may or may not edit the response, respectively.</span></span> <span data-ttu-id="75fc7-112">Im folgenden Codebeispiel wird von AutoAcceptMeetingRequests jedes **MeetingItem**-Objekt aufgeführt, um die verknüpften **AppointmentItem**-Elemente abzurufen.</span><span class="sxs-lookup"><span data-stu-id="75fc7-112">In the following code example, AutoAcceptMeetingRequests enumerates through every **MeetingItem** object to get the associated **AppointmentItem**.</span></span> <span data-ttu-id="75fc7-113">AutoAcceptMeetingRequests verwendet dann die **Respond**-Methode mit dem auf **true** festgelegten *fNoUI*-Parameter, um anzuzeigen, dass die Antwort automatisch gesendet wird, um die Besprechungsanfrage anzunehmen.</span><span class="sxs-lookup"><span data-stu-id="75fc7-113">AutoAcceptMeetingRequests then uses the **Respond** method with the *fNoUI* parameter set to **true** to indicate that a response will be sent automatically to accept the meeting request.</span></span>

<span data-ttu-id="75fc7-114">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="75fc7-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="75fc7-115">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="75fc7-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="75fc7-116">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="75fc7-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AutoAcceptMeetingRequests()
{
    Outlook.MeetingItem mtgResponse;
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(true);
        if (appt != null)
        {
            mtgResponse = appt.Respond(
                Outlook.OlMeetingResponse.olMeetingAccepted,
                true, Type.Missing);
            mtgResponse.Send();
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="75fc7-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75fc7-117">See also</span></span>

- [<span data-ttu-id="75fc7-118">Besprechungsanfragen</span><span class="sxs-lookup"><span data-stu-id="75fc7-118">Meeting requests</span></span>](meeting-requests.md)

