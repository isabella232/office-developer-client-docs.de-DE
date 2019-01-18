---
title: Auffordern eines Benutzers zum Antworten auf eine Besprechungsanfrage
TOCTitle: Prompt a user to respond to a meeting request
ms:assetid: a0d69f82-8659-457d-9418-1a897a10882f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184630(v=office.15)
ms:contentKeyID: 55119877
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26e59cca7431e9f11f3fea5fa058548b9a5903a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722613"
---
# <a name="prompt-a-user-to-respond-to-a-meeting-request"></a>Auffordern eines Benutzers zum Antworten auf eine Besprechungsanfrage

Dieses Beispiel zeigt, wie der Benutzer zu einer Antwort auf eine Besprechungsanfrage aufgefordert wird und wie ihm ermöglicht wird, die Antwort vor dem Senden zu bearbeiten.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Die [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\))-Methode des [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekts wird zum Benachrichtigen des Besprechungsorganisators darüber verwendet, ob die Besprechung zum Kalender des Empfängers als "Angenommen", "Abgelehnt" oder "Mit Vorbehalt" hinzugefügt wurde. Mithilfe der **Respond**-Methode können Sie angeben, ob Sie die Benachrichtigung automatisch senden möchten oder ob der Benutzer die Antwort vor dem Absenden bearbeiten kann. Die **Respond**-Methode akzeptiert drei Parameter. Der *Response*-Parameter gibt an, ob die Antwort "Angenommen", "Abgelehnt" oder "Mit Vorbehalt" lautet. Die Parameter *fNoUI* und *fAdditionalTextDialog* sind **bool**-Werte, die bestimmen, ob die Antwort gesendet wird und ob der Benutzer die Antwort bearbeitet hat. 

Im folgenden Codebeispiel listet PromptUserMeetingRequest die [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\))-Objekte auf, um die zugehörigen **AppointmentItem**-Objekte abzurufen. Anschließend wird die **Respond**-Methode aufgerufen, wobei der *fNoUI*-Parameter auf **false** und der *fAdditionalTextDialog*-Parameter auf **true** festgelegt ist. Auf diese Weise kann der Benutzer auswählen, ob eine Antwort gesendet werden soll und ob der Text der Antwort vor dem Absenden bearbeitet werden soll.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void PromptUserMeetingRequest()
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
                false, true);
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Besprechungsanfragen](meeting-requests.md)

