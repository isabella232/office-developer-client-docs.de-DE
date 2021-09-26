---
title: Erstellen einer Besprechungsanfrage, Hinzufügen von Empfängern und Angeben eines Orts
TOCTitle: Create a meeting request, add recipients, and specify a location
ms:assetid: 3053c27e-34d9-440e-9b66-06de940c2813
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644964(v=office.15)
ms:contentKeyID: 55119873
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 410a90388ec9b3237eb150f74c08818b8b08739e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590793"
---
# <a name="create-a-meeting-request-add-recipients-and-specify-a-location"></a>Erstellen einer Besprechungsanfrage, Hinzufügen von Empfängern und Angeben eines Orts

In diesem Beispiel wird ein Terminelement als Besprechungsanfrage erstellt und der Zeitpunkt, die Empfänger und der Ort der Besprechung angegeben. Anschließend wir der Termin in einem Inspektorfenster angezeigt.

## <a name="example"></a>Beispiel

Eine Besprechungsanfrage in Outlook ist ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Um ein Terminelement als eine Besprechungsanfrage festzulegen, müssen Sie die [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\))-Eigenschaft auf **olMeeting** festlegen. Verwenden Sie die [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) -Eigenschaft des [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) -Objekts, um anzugeben, ob ein Besprechungsteilnehmer als optional gilt oder ein Empfänger anstatt als Teilnehmer als Besprechungsressource gewertet werden soll.

Wenn Sie dieses Codebeispiel mit Visual Studio testen, müssen Sie beim Importieren des **Microsoft.Office.Interop.Outlook**-Namespace zuerst einen Verweis auf die Microsoft Outlook 15.0-Objektbibliothekskomponente hinzufügen und die Outlook-Variable angeben. Die Anweisungen **Imports** oder **using** dürfen nicht direkt vor den Funktionen im Codebeispiel stehen, sondern müssen vor der öffentlichen Klassendeklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie der Import und die Zuweisung in Visual Basic und C\# ausgeführt werden.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SetRecipientTypeForAppt()
    Dim appt As Outlook.AppointmentItem = _
        CType(Application.CreateItem( _
        Outlook.OlItemType.olAppointmentItem), Outlook.AppointmentItem)
    appt.Subject = "Customer Review"
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting
    appt.Location = "36/2021"
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM")
    appt.End = DateTime.Parse("10/20/2006 11:00 AM")
    Dim recipRequired As Outlook.Recipient = _
        appt.Recipients.Add("Ryan Gregg")
    recipRequired.Type = _
        Outlook.OlMeetingRecipientType.olRequired
    Dim recipOptional As Outlook.Recipient = _
        appt.Recipients.Add("Peter Allenspach")
    recipOptional.Type = _
        Outlook.OlMeetingRecipientType.olOptional
    Dim recipConf As Outlook.Recipient = _
        appt.Recipients.Add("Conf Room 36/2021 (14) AV")
    recipConf.Type = _
        Outlook.OlMeetingRecipientType.olResource
    appt.Recipients.ResolveAll()
    appt.Display(False)
End Sub
```


```csharp
private void SetRecipientTypeForAppt()
{
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Customer Review";
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Location = "36/2021";
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM");
    appt.End = DateTime.Parse("10/20/2006 11:00 AM");
    Outlook.Recipient recipRequired =
        appt.Recipients.Add("Ryan Gregg");
    recipRequired.Type =
        (int)Outlook.OlMeetingRecipientType.olRequired;
    Outlook.Recipient recipOptional =
        appt.Recipients.Add("Peter Allenspach");
    recipOptional.Type =
        (int)Outlook.OlMeetingRecipientType.olOptional;
    Outlook.Recipient recipConf =
       appt.Recipients.Add("Conf Room 36/2021 (14) AV");
    recipConf.Type =
        (int)Outlook.OlMeetingRecipientType.olResource;
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a>Siehe auch

- [Besprechungsanfragen](meeting-requests.md)

