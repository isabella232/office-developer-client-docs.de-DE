---
title: Freigeben von Kalenderinformationen per E-Mail
TOCTitle: Share calendar information through email
ms:assetid: 3382010c-0a16-4dca-a99e-669e9178354e
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609881(v=office.15)
ms:contentKeyID: 55119817
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d6e1031e5d4b387aee7297dd91584f0916b4f00b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608942"
---
# <a name="share-calendar-information-through-email"></a>Freigeben von Kalenderinformationen per E-Mail

In diesem Beispiel wird gezeigt, wie Informationen aus einem Kalender mithilfe einer E-Mail-Nachricht im iCalendar-Format freigegeben werden.

## <a name="example"></a>Beispiel

Das iCalendar-Format ermöglicht das Senden von Elementen an andere Outlook- oder Nicht-Outlook-Clients über Standard-Internet-Mailformate und -Protokolle. Im Codebeispiel wird das [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) -Objekt verwendet, das den Export von Informationen aus einem Kalenderordner in das iCalendar-Format unterstützt.

Zuerst wird [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) für den standardmäßigen Kalenderordner aufgerufen, um ein **CalendarSharing**-Objekt abzurufen. Dann werden die Eigenschaften des **CalendarSharing**-Objekts festgelegt, um die Exportkriterien, wie Datumsbereich der Kalenderinformation, die Zulässigkeit von Anhängen und Einzelheiten zu Besprechungen anzugeben, die als privat gekennzeichnet sind.

Damit die Kalenderinformation dann per E-Mail gesendet wird, wird durch das Codebeispiel die [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\))-Methode des **CalendarSharing**-Objekts aufgerufen.

Wenn Sie dieses Codebeispiel mit Visual Studio testen, müssen Sie beim Importieren des **Microsoft.Office.Interop.Outlook**-Namespace zuerst einen Verweis auf die Microsoft Outlook 15.0-Objektbibliothekskomponente hinzufügen und die Outlook-Variable angeben. Die **Imports**- oder **using**-Anweisung darf nicht direkt vor den Funktionen im Codebeispiel stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie der Import und die Zuweisung in Visual Basic und C\# ausgeführt werden.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub SendNextWeekToAddress(ByVal sendToAddresses As String)
    If String.IsNullOrEmpty(sendToAddresses) Then
        Throw New ArgumentException( _
            "Parameter must contain a value.", "sendToAddress")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = False
    exporter.RestrictToWorkingHours = False
    exporter.StartDate = DateTime.Today.Date
    exporter.EndDate = DateTime.Today.Date.AddDays(7)

    '' Create a new mail item
    Dim calendarMail As Outlook.MailItem = exporter.ForwardAsICal _
        (Outlook.OlCalendarMailFormat. _
        olCalendarMailFormatDailySchedule)
    calendarMail.To = sendToAddresses
    calendarMail.Send()
    calendarMail.Display()
End Sub
```

```csharp
private void SendNextWeekToAddress(string sendToAddresses)
{
    if (string.IsNullOrEmpty(sendToAddresses))
        throw new ArgumentException(
        "sendToAddress","Parameter must contain a value.");
    Outlook.Folder calendar = 
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = false;
    exporter.RestrictToWorkingHours = false;
    exporter.StartDate = DateTime.Today.Date;
    exporter.EndDate = DateTime.Today.Date.AddDays(7);

    // Create a new mail item
    Outlook.MailItem calendarMail = 
        exporter.ForwardAsICal(Outlook.OlCalendarMailFormat.
        olCalendarMailFormatDailySchedule);
    calendarMail.To = sendToAddresses;
    ((Outlook.MailItemClass)calendarMail).Send();
    ((Outlook.MailItemClass)calendarMail).Display(Type.Missing);
}
```

## <a name="see-also"></a>Siehe auch

- [Calendar](calendar.md)

