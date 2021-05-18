---
title: Freigeben eines Frei-/Gebucht-Zeitplans innerhalb eines bestimmten Zeitraums in einem Kalender
TOCTitle: Share Free/Busy schedule within a specified period in a calendar
ms:assetid: 1d038f56-80dd-42fd-809b-f5b3a47cd5ee
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609503(v=office.15)
ms:contentKeyID: 55119824
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 00cc252dd16212e812280db70d6b7c77c2c02693
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315246"
---
# <a name="share-freebusy-schedule-within-a-specified-period-in-a-calendar"></a><span data-ttu-id="808f9-102">Freigeben eines Frei-/Gebucht-Zeitplans innerhalb eines bestimmten Zeitraums in einem Kalender</span><span class="sxs-lookup"><span data-stu-id="808f9-102">Share Free/Busy schedule within a specified period in a calendar</span></span>

<span data-ttu-id="808f9-103">In diesem Beispiel wird der Frei/Gebucht-Zeitplan einer bestimmten Woche eines Kalenders abgerufen und Einzelheiten zu freien und gebuchten Terminen sowie zum Thema des Termins angezeigt.</span><span class="sxs-lookup"><span data-stu-id="808f9-103">This example obtains the Free/Busy schedule within a specified week from a calendar and displays the free, busy, and subject details to the user.</span></span>

## <a name="example"></a><span data-ttu-id="808f9-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="808f9-104">Example</span></span>

<span data-ttu-id="808f9-p101">Dieses Codebeispiel verwendet die [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) -Methode des [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) -Objekts, um ein [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) -Objekt für den standardmäßigen Kalenderordner und eine bestimmte Woche anzurufen. Danach wird die [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) -Methode für das **CalendarSharing**-Objekt aufgerufen und die Nachricht mit einer iCalendar-Ladung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="808f9-p101">This code sample uses the [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) method of the [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object to obtain a [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object for the default Calendar folder for a specific one-week period. It then calls the [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) method on the **CalendarSharing** object and displays the message with an iCalendar payload.</span></span>

<span data-ttu-id="808f9-107">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="808f9-107">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="808f9-108">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="808f9-108">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="808f9-109">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="808f9-109">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub DemoCalendarSharing()
    ' Get instance of CalendarSharing object
    Dim calShare As Outlook.CalendarSharing = _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar). _
        GetCalendarExporter()
    ' Free busy and subject details
    calShare.CalendarDetail = _
        Outlook.OlCalendarDetail.olFreeBusyAndSubject
    ' Set start and end dates
    calShare.StartDate = DateTime.Today
    calShare.EndDate = calShare.StartDate.AddDays(1)
    ' Call ForwardAsICal method
    Dim mail As Outlook.MailItem = _
        calShare.ForwardAsICal( _
        Outlook.OlCalendarMailFormat.olCalendarMailFormatDailySchedule)
    ' Add recipient
    mail.Recipients.Add("someone@example.com")
    mail.Recipients.ResolveAll()
    ' Set subject
    Dim CalName As String = _
    Application.Session.GetDefaultFolder( _
    Outlook.OlDefaultFolders.olFolderCalendar).Name
    mail.Subject = _
        Application.Session.CurrentUser.Name & _
        CalName.PadLeft(CalName.Length + 1)
    ' Display calendar sharing item
    mail.Display(False)
End Sub
```

```csharp
private void DemoCalendarSharing()
{
    // Get instance of CalendarSharing object
    Outlook.CalendarSharing calShare =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderCalendar).
        GetCalendarExporter();
    // Free busy and subject details
    calShare.CalendarDetail =
        Outlook.OlCalendarDetail.olFreeBusyAndSubject;
    // Set start and end dates
    calShare.StartDate = DateTime.Today;
    calShare.EndDate = calShare.StartDate.AddDays(1);
    // Call ForwardAsICal method
    Outlook.MailItem mail =
        calShare.ForwardAsICal(Outlook.OlCalendarMailFormat
        .olCalendarMailFormatDailySchedule);
    // Add recipient
    mail.Recipients.Add("someone@example.com");
    mail.Recipients.ResolveAll();
    // Set subject
    string CalName =
        Application.Session.GetDefaultFolder
    (Outlook.OlDefaultFolders.olFolderCalendar).Name;
    mail.Subject =
        Application.Session.CurrentUser.Name +
        CalName.PadLeft(CalName.Length + 1);
    // Display calendar sharing item
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="808f9-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="808f9-110">See also</span></span>

- [<span data-ttu-id="808f9-111">Calendar</span><span class="sxs-lookup"><span data-stu-id="808f9-111">Calendar</span></span>](calendar.md)

