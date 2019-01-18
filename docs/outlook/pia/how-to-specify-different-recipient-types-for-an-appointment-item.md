---
title: Angeben verschiedener Empfängertypen für ein Terminelement
TOCTitle: Specify different recipient types for an appointment item
ms:assetid: 83aedc8f-adc0-453d-8e71-1bb9aacc7993
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184622(v=office.15)
ms:contentKeyID: 55119807
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: beb29c46d590938d1650dac0c862dd5f898333fc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709180"
---
# <a name="specify-different-recipient-types-for-an-appointment-item"></a>Angeben verschiedener Empfängertypen für ein Terminelement

In diesem Beispiel werden mithilfe der [OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\))-Auflistung verschiedene Empfängertypen für ein Terminelement angegeben.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Zum Hinzufügen von Empfängern zu einem [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) -Objekt, das eine Besprechungsanfrage darstellt, geben Sie mit der OlMeetingRecipientType-Aufzählung an, ob es sich beim Empfänger der Nachricht um einen erforderlichen oder optionalen Teilnehmer oder um eine Ressource (wie einen Raum oder eine bestimmte Ausstattung) handelt.

Im folgenden Codebeispiel erstellt SetRecipientTypeForAppt ein **AppointmentItem**-Objekt, legt Eigenschaften für dieses Objekt fest und fügt erforderliche und optionale Teilnehmer hinzu. Es wird auch ein Konferenzraum für die Besprechung hinzugefügt. Beachten Sie, dass die [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\))-Eigenschaft auf [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)) festgelegt wird, wodurch angegeben wird, dass der Termin eine Besprechungsanfrage ist.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
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

- [Termine](appointments.md)

