---
title: Erstellen eines Ausnahmetermins in einer Terminserie
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1344188ad8947245ec0a6d54efff603b9e7755e7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405980"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a>Erstellen eines Ausnahmetermins in einer Terminserie

In diesem Beispiel wird mithilfe eines [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))-Objekts eine Ausnahme zu einem Standardserienmuster für einen Termin erstellt.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Nachdem Sie eine Termininstanz einer Terminserie gelöscht oder geändert haben, erstellt Outlook ein [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))-Objekt. Mithilfe dem Exception-Objekt können Sie eine Ausnahme zu einem Standardserienmuster erstellen. Die Eigenschaften des Objekts enthalten die Änderungen, die an der Termininstanz vorgenommen wurden. Die [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\))-Auflistung enthält alle Exception-Objekte für eine Terminserie und ist mit dem [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekt des Termins verknüpft.

Um das [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt abzurufen, das die Ausnahme zu dem ursprünglichen Serienmuster der Terminserie darstellt, verwenden Sie die [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\))-Eigenschaft von Exception. Mit den Methoden und Eigenschaften des zurückgegebenen AppointmentItem können Sie die Eigenschaften der Terminausnahme festlegen.

Wenn Sie mit Terminserien arbeiten, müssen Sie vorherige Verweise freigeben, neue Verweise auf das Terminserienelement abrufen, bevor Sie das Element öffnen oder bearbeiten, und diese Verweise freigeben, sobald Sie Ihre Änderungen abgeschlossen und gespeichert haben. Diese Vorgehensweise gilt für das sich wiederholende **AppointmentItem**-Objekt und alle [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\))- oder [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\))-Objekte. Um einen Verweis in Visual Basic freizugeben, legen Sie dieses vorhandene Objekt auf „Nothing“ fest. Geben Sie in C\# den Arbeitsspeicher für dieses Objekt explizit frei.

Beachten Sie Folgendes: Selbst wenn Sie den Verweis freigegeben haben und versuchen, einen neuen Verweise abzurufen, zeigt der neue Verweis weiterhin auf eine veraltete Kopie des Objekts, wenn immer noch ein aktiver Verweis auf eines der obigen Objekte vorhanden ist, der von einem anderen Add-In oder von Outlook verwendet wird. Deshalb ist es wichtig, dass Sie die Verweise freigeben, sobald Sie die Bearbeitung der Terminserie abgeschlossen haben.

Im folgenden Codebeispiel ändert CreateExceptionExample den Betreff der im Thema [Suchen nach einem bestimmten Termin in einer Terminserie](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md) erstellten Terminserie. Anschließend wird mit der AppointmentItem-Eigenschaft des resultierenden Exception-Objekts das AppointmentItem-Objekt abgerufen, das der Terminausnahme entspricht. CreateExceptionExample ändert dann die Start- und Endzeit der Terminausnahme.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateExceptionExample()
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
            Outlook.AppointmentItem myInstance =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (myInstance != null)
            {
                myInstance.Subject = "My Exception";
                myInstance.Save();
                Outlook.RecurrencePattern newPattern =
                    appt.GetRecurrencePattern();
                Outlook.Exception myException =
                    newPattern.Exceptions[1];
                if (myException != null)
                {
                    Outlook.AppointmentItem myNewInstance =
                        myException.AppointmentItem;
                    myNewInstance.Start =
                        DateTime.Parse("7/21/2006 1:00 PM");
                    myNewInstance.End =
                        DateTime.Parse("7/21/2006 2:00 PM");
                    myNewInstance.Save();
                }
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

