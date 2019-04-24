---
title: Verwenden des Dialogfelds „Namen auswählen“ zum Abrufen und Zuweisen von Empfängern zu einem Termin
TOCTitle: Use the Select Names dialog box to obtain and assign recipients to an appointment
ms:assetid: b9bcb341-1912-425c-8d75-ed5be233145a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184636(v=office.15)
ms:contentKeyID: 55119878
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 408d2fbdc3c89b7f2bad1fe9c2c76c1f47ae05ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335378"
---
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a>Verwenden des Dialogfelds „Namen auswählen“ zum Abrufen und Zuweisen von Empfängern zu einem Termin

In diesem Beispiel wird gezeigt, wie das Dialogfeld **Namen auswählen** zum Abrufen und Zuweisen von Empfängern zu einem Termin verwendet wird.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Zum Anzeigen des Dialogfelds **Namen auswählen** rufen Sie die [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) -Methode des [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) -Objekts auf. Nachdem das Dialogfeld **Namen auswählen** angezeigt wurde, wird die Codeausführung angehalten, bis der Benutzer auf **OK** klickt oder das Dialogfeld schließt. Verwenden Sie die [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) -Eigenschaft des **SelectNamesDialog**-Objekts, um anfänglich im Dialogfeld angezeigte Empfänger festzulegen oder die im Dialogfeld ausgewählten Empfänger abzurufen. Die Eigenschaft gibt eine [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) -Auflistung zurück, die **SelectNamesDialog** zugeordnet ist. Zum Hinzufügen eines [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) -Objekts zur **Recipients**-Auflistung für **SelectNamesDialog** verwenden Sie die [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) -Methode für die Auflistung und geben die [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) -Eigenschaft des **Recipient**-Objekts an.

Im folgenden Codebeispiel erstellt DemoSelectNamesDialogRecipients ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt und legt einige seiner Eigenschaften fest. Anschließend wird ein **SelectNamesDialog**-Objekt erstellt und mit der [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) -Methode ein Besprechungsanzeigemodus für das Dialogfeld **Namen auswählen** festgelegt. Im Beispiel wird die **Resource**-Empfängerauswahl mit der Zeichenfolge "Conf Room 36/2739" aufgefüllt. Nachdem das Dialogfeld dem Benutzer angezeigt wurde, zählt der Code die **Recipients**-Auflistung auf, die dieser Instanz von **SelectNamesDialog** zugeordnet ist, und fügt diese Empfänger dem erstellten Termin hinzu. Schließlich wird in dem Beispiel die Besprechungsanfrage für den Benutzer angezeigt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoSelectNamesDialogRecipients()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Subject = "Team Morale Event";
    appt.Start = DateTime.Parse("5/17/2007 11:00 AM");
    appt.End = DateTime.Parse("5/17/2007 12:00 PM");
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    snd.SetDefaultDisplayMode(
        Outlook.OlDefaultSelectNamesDisplayMode.olDefaultMeeting);
    Outlook.Recipient confRoom =
        snd.Recipients.Add("Conf Room 36/2739");
    // Explicitly specify Recipient.Type.
    confRoom.Type = (int)Outlook.OlMeetingRecipientType.olResource;
    snd.Recipients.ResolveAll();
    snd.Display();
    // Add Recipients to meeting request.
    Outlook.Recipients recips = snd.Recipients;
    if (recips.Count > 0)
    {
        foreach (Outlook.Recipient recip in recips)
        {
            appt.Recipients.Add(recip.Name);
        }
    }
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a>Siehe auch

- [Empfänger](recipients.md)

