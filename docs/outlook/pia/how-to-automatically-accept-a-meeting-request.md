---
title: Automatisches Annehmen einer Besprechungsanfrage
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d19963814e86587e3ad5b53071d43e647b596a88
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590842"
---
# <a name="automatically-accept-a-meeting-request"></a>Automatisches Annehmen einer Besprechungsanfrage

Dieses Beispiel verwendet die [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\))-Methode, um eine Besprechungsanfrage automatisch anzunehmen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Ein [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\))-Objekt stellt eine Anfrage zum Hinzufügen eines Termins, dargestellt durch ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt, zum Kalender eines Empfängers dar. In diesem Beispiel wird gezeigt, wie die [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\))-Methode verwendet wird, um den **AppointmentItem** abzurufen, der einer Besprechungsanfrage zugeordnet ist. Verwenden Sie dann die [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\))-Methode des **AppointmentItem**-Elements zum Benachrichtigen des Besprechungsorganisators darüber, ob die Besprechung zum Kalender des Empfängers als "Angenommen", "Abgelehnt" oder "Mit Vorbehalt" hinzugefügt wurde. Die **Respond**-Methode akzeptiert drei Parameter. 

Der *Response*-Parameter gibt an, ob die Antwort "Angenommen", "Abgelehnt" oder "Mit Vorbehalt" lautet. Die Parameter fNoUI und fAdditionalTextDialog sind **bool**-Werte, die bestimmen, ob die Antwort gesendet wird und ob der Benutzer die Antwort bearbeitet hat. Im folgenden Codebeispiel wird von AutoAcceptMeetingRequests jedes **MeetingItem**-Objekt aufgeführt, um die verknüpften **AppointmentItem**-Elemente abzurufen. AutoAcceptMeetingRequests verwendet dann die **Respond**-Methode mit dem auf **true** festgelegten *fNoUI*-Parameter, um anzuzeigen, dass die Antwort automatisch gesendet wird, um die Besprechungsanfrage anzunehmen.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Besprechungsanfragen](meeting-requests.md)

