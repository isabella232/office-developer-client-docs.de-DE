---
title: Erstellen einer Erinnerung für ein Terminelement
TOCTitle: Create a reminder for an appointment item
ms:assetid: 85e772f0-65ac-4abc-8286-9099882a2400
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184623(v=office.15)
ms:contentKeyID: 55119814
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 164e744e03ab0984265736673c71d2d0bf57bf45
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405973"
---
# <a name="create-a-reminder-for-an-appointment-item"></a>Erstellen einer Erinnerung für ein Terminelement

Dieses Beispiel zeigt, wie Sie mithilfe der [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\))-Eigenschaft eine Erinnerung für einen Termin erstellen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Outlook bietet eine Möglichkeit zum Festlegen einer Erinnerung für einen Termin mithilfe der [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\))-Eigenschaft des [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekts. Diese Eigenschaft gibt an, ob eine Erinnerung für den Termin erstellt wurde. Durch Festlegen der ReminderSet-Eigenschaft auf „true“ wird eine Erinnerung erstellt; wenn diese Eigenschaft auf „false“ festgelegt wird, wird die Erinnerung entfernt.

Im folgenden Codebeispiel erstellt ReminderExample eine Erinnerung in einem privaten Termin für eine Weinverkostung in Napa, Kalifornien, und es wird festgelegt, dass die Erinnerung zwei Stunden vor Beginn des Termins auftritt. Zuerst erstellt ReminderExample das Outlook-Objekt **AppointmentItem**. Dann wird die [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\))-Eigenschaft für das Element auf [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)) festgelegt. Dies weist darauf hin, dass der Termin ein privater Termin ist. Nach dem Festlegen anderer Eigenschaften des Termins, z. B. [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\))- und [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\))zeiten, legt ReminderExample die [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\))-Eigenschaft so fest, dass die Anzahl von Minuten angegeben wird, die die Erinnerung vor dem Beginn des Termins angezeigt wird.  In diesem Fall wird ReminderMinutesBeforeStart auf 120 Minuten (2 Stunden) festgelegt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void ReminderExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Wine Tasting";
    appt.Location = "Napa CA";
    appt.Sensitivity = Outlook.OlSensitivity.olPrivate;
    appt.Start = DateTime.Parse("10/21/2006 10:00 AM");
    appt.End = DateTime.Parse("10/21/2006 3:00 PM");
    appt.ReminderSet = true;
    appt.ReminderMinutesBeforeStart = 120;
    appt.Save();
}
```

## <a name="see-also"></a>Siehe auch

- [Termine](appointments.md)

