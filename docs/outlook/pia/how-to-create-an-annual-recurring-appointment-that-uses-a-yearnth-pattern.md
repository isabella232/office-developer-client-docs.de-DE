---
title: Erstellen einer jährlichen Terminserie mit einem jährlichen Muster
TOCTitle: Create an annual recurring appointment that uses a YearNth pattern
ms:assetid: 5fb2ad0b-248c-417d-8868-52e0550d970f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184611(v=office.15)
ms:contentKeyID: 55119811
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc50166674ee7b9699ef8e29c5ff1e54db705ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349504"
---
# <a name="create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern"></a>Erstellen einer jährlichen Terminserie mit einem jährlichen Muster

Dieses Beispiel zeigt, wie ein Termin erstellt wird, dessen jährliches Serienmuster ein bestimmter Tag ist, z. B. der erste Montag im Juni.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Wenn Sie einen jährlichen Termin erstellen möchten, der an einem bestimmten Tag der Woche in einen bestimmten Monat (z. B. am ersten Montag im Juni) stattfinden soll, müssen Sie YearNth-Serien verwenden. Um eine YearNth-Serie festzulegen, müssen Sie zunächst die [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\))-Eigenschaft des [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekts auf „olRecursYearNth“ festlegen. Legen Sie dann die [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\))-Eigenschaft fest, um anzugeben, an welchem Tag der Woche der Termin wiederholt werden soll, und die [Instanz](https://msdn.microsoft.com/library/bb645269\(v=office.15\))-Eigenschaft, um das n-te Vorkommen an dem angegebenen Tag der Woche (z. B. am dritten Dienstag) in einem bestimmten Monat für das jährliche Muster anzugeben.

Wenn Sie mit Terminserien arbeiten, müssen Sie vorherige Verweise freigeben, neue Verweise auf das Terminserienelement abrufen, bevor Sie das Element öffnen oder bearbeiten, und diese Verweise freigeben, sobald Sie Ihre Änderungen abgeschlossen und gespeichert haben. Diese Vorgehensweise gilt für das sich wiederholende **AppointmentItem**-Objekt und alle [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))- oder [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekte. Um einen Verweis in Visual Basic freizugeben, legen Sie dieses vorhandene Objekt auf „Nothing“ fest. Geben Sie in C\# den Arbeitsspeicher für dieses Objekt explizit frei.

Auch nachdem Sie Ihren Verweis freigegeben und versucht haben, einen neuen Verweis abzurufen, zeigt Ihr neuer Verweis, wenn es noch einen aktiven Verweis (der von einem anderen Add-In oder Outlook aktiviert wurde) auf eines der obigen Objekte gibt, weiter auf eine veraltete Kopie des Objekts. Deshalb müssen Sie stets Ihre Verweise freigeben, sobald Sie mit dem Bearbeiten der Terminserie fertig sind.

Im folgenden Codebeispiel erstellt RecurringYearNthAppointment einen Termin mit einem YearNth-Serienmuster. RecurringYearNthAppointment erstellt zunächst eine Terminserie, indem ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt erstellt wird. Als Nächstes wird das Serienmuster des Termins mithilfe der [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\))-Methode abgerufen. Dann werden die folgenden RecurrencePattern-Eigenschaften festgelegt: RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)) und [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)). Die MonthOfYear-Eigenschaft akzeptiert einen numerischen Wert von 1 bis 12, wobei jede Zahl den entsprechenden Monat darstellt. Nachdem die Eigenschaften festgelegt wurden speichert RecurringYearNthAppointment den Termin und zeigt ihn dann mit dem Muster „Tritt am ersten Montag des Monats Juni ab dem 1.6.2007 bis 6.6.2016 von 14:00 – 17:00 Uhr auf“.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringYearNthAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring YearNth Appointment";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearNth;
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday;
    pattern.MonthOfYear = 6;
    pattern.Instance = 1;
    pattern.Occurrences = 10;
    pattern.Duration = 180;
    pattern.PatternStartDate = DateTime.Parse("6/1/2007");
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("5:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a>Siehe auch

- [Termine](appointments.md)

