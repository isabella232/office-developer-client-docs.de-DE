---
title: Suchen nach einem bestimmten Termin in einer Terminserie
TOCTitle: Find a specific appointment in a recurring appointment series
ms:assetid: 01f55f04-7245-4325-a354-50a6eb270a31
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184586(v=office.15)
ms:contentKeyID: 55119812
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 19502895996d4777f2d1a6887aa80883a5398a09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320251"
---
# <a name="find-a-specific-appointment-in-a-recurring-appointment-series"></a>Suchen nach einem bestimmten Termin in einer Terminserie

Dieses Beispiel zeigt, wie ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt zurückgegeben wird, das einen bestimmten Termin in einer Terminserie darstellt.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Verwenden Sie zum Auffinden einer Instanz einer Terminserie für ein angegebenes Datum mit angegebener Uhrzeit die [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) -Methode des [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) -Objekts, um ein **AppointmentItem**-Objekt zurückzugeben.

Wenn Sie mit Terminserien arbeiten, müssen Sie vorherige Verweise freigeben, neue Verweise auf das Terminserienelement abrufen, bevor Sie das Element öffnen oder bearbeiten, und diese Verweise freigeben, sobald Sie Ihre Änderungen abgeschlossen und gespeichert haben. Diese Vorgehensweise gilt für das sich wiederholende **AppointmentItem**-Objekt und alle [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))- oder [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekte. Um einen Verweis in Visual Basic freizugeben, legen Sie dieses vorhandene Objekt auf „Nothing“ fest. Geben Sie in C\# den Arbeitsspeicher für dieses Objekt explizit frei.

Auch nachdem Sie Ihren Verweis freigegeben und versucht haben, einen neuen Verweis abzurufen, zeigt Ihr neuer Verweis, wenn es noch einen aktiven Verweis (der von einem anderen Add-In oder Outlook aktiviert wurde) auf eines der obigen Objekte gibt, weiter auf eine veraltete Kopie des Objekts. Deshalb müssen Sie stets Ihre Verweise freigeben, sobald Sie mit dem Bearbeiten der Terminserie fertig sind.

Im folgenden Codebeispiel verwendet CheckOccurrenceExample die Terminserie, die im Codebeispiel in [Erstellen einer Terminserie mit wöchentlichem Muster](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md) erstellt wurde. Dann wird die GetOccurrence-Methode aufgerufen, um zu ermitteln, ob die Terminserie an dem angegebenen Datum und zu der angegebenen Uhrzeit beginnt. Zum Sicherstellen, dass die Prozedur fortgesetzt wird, auch wenn die bereitgestellten Informationen nicht dem Startdatum und der Startuhrzeit einer Instanz der Terminserie entsprechen, verwendet das Beispiel einen try…catch-Block. Nach Aufrufen der GetOccurrence-Methode für jeden Termin in der Terminserie testet CheckOccurrenceExample die singleAppt-Variable, um zu bestimmen, ob sie auf einen NULL-Verweis festgelegt ist, was bedeutet, dass die Methode keinen Erfolg hatte und kein **AppointmentItem**-Objekt zurückgegeben hat.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CheckOccurrenceExample()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find(
        "[Subject]='Recurring Appointment DaysOfWeekMask Example'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        try
        {
            Outlook.RecurrencePattern pattern =
                appt.GetRecurrencePattern();
            Outlook.AppointmentItem singleAppt =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (singleAppt != null)
            {
                Debug.WriteLine("7/21/2006 2:00 PM occurrence found.");
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Termine](appointments.md)

