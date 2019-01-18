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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700332"
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

