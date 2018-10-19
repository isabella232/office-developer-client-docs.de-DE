---
title: Erstellen einer Terminserie mithilfe des Standardserienmusters
TOCTitle: Create a recurring appointment by using the default recurrence pattern
ms:assetid: 157bf1ae-2efe-4783-99ea-606722dde204
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184589(v=office.15)
ms:contentKeyID: 55119809
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: be6c024012c02d31af7ce37af6010ba6b40419ce
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406708"
---
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a>Erstellen einer Terminserie mithilfe des Standardserienmusters

Dieses Beispiel zeigt, wie eine Terminserie mithilfe des Standardserienmusters erstellt wird.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Wenn Sie einen Termin in Outlook erstellen, erstellen Sie ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt. Bei Ihrem Termin handelt es sich um eine Terminserie, wenn die [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\))-Eigenschaft des AppointmentItem auf „true“ festgelegt wird. IsRecurring kann nicht direkt festgelegt werden. 

Sie können jedoch eine Terminserie mithilfe des [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekts erstellen. Um eine Terminserie programmgesteuert zu erstellen, erstellen Sie ein **AppointmentItem**-Objekt, rufen Sie die [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\))-Methode des **AppointmentItem**-Objekts auf, und speichern Sie dann das **AppointmentItem**-Objekt. Dadurch wird ein Termin erstellt, der das Standardserienmuster verwendet, und der täglich an dem Tag der Woche auftritt, für den der Termin erstellt wurde. Eine Terminserie weist kein Enddatum auf. Mit dem RecurrencePattern-Objekt können Sie Terminserien an angegebenen Intervallen erstellen – täglich, wöchentlich, monatlich oder jährlich. Wenn Sie keine Intervalle für das RecurrencePattern-Objekt nicht angeben, verwendet Outlook das Standardserienmuster.

Wenn Sie mit Terminserien arbeiten, müssen Sie vorherige Verweise freigeben, neue Verweise auf das Terminserienelement abrufen, bevor Sie das Element öffnen oder bearbeiten, und diese Verweise freigeben, sobald Sie Ihre Änderungen abgeschlossen und gespeichert haben. Diese Vorgehensweise gilt für das sich wiederholende **AppointmentItem**-Objekt und alle [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))- oder [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekte. Um einen Verweis in Visual Basic freizugeben, legen Sie dieses vorhandene Objekt auf „Nothing“ fest. Geben Sie in C\# den Arbeitsspeicher für dieses Objekt explizit frei.

Auch nachdem Sie Ihren Verweis freigegeben und versucht haben, einen neuen Verweis abzurufen, zeigt Ihr neuer Verweis, wenn es noch einen aktiven Verweis (der von einem anderen Add-In oder Outlook aktiviert wurde) auf eines der obigen Objekte gibt, weiter auf eine veraltete Kopie des Objekts. Deshalb müssen Sie stets Ihre Verweise freigeben, sobald Sie mit dem Bearbeiten der Terminserie fertig sind.

Im folgenden Beispiel erstellt CreateRecurringAppointment ein **AppointmentItem**-Objekt. Dann wird GetRecurrencePattern aufgerufen. GetRecurrencePattern gibt ein RecurrencePattern-Objekt zurück, und das AppointmentItem wird gespeichert. Dadurch wird eine Terminserie erstellt, die das Standardserienmuster verwendet.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateRecurringAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Weekly Extensibility Team Meeting";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    appt.Save();
}
```

## <a name="see-also"></a>Siehe auch

- [Termine](appointments.md)

