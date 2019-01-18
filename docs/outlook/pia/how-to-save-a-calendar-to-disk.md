---
title: Speichern eines Kalenders auf einem Datenträger
TOCTitle: Save a calendar to disk
ms:assetid: f1b57bd0-c972-4b86-8870-f26290f28050
ms:mtpsurl: https://msdn.microsoft.com/library/Bb647583(v=office.15)
ms:contentKeyID: 55119827
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b07df7458f80b751077358ac3c53ad41032d1080
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712505"
---
# <a name="save-a-calendar-to-disk"></a><span data-ttu-id="61a8c-102">Speichern eines Kalenders auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="61a8c-102">Save a calendar to disk</span></span>

<span data-ttu-id="61a8c-103">Dieses Beispiel zeigt, wie Sie einen ganzen Kalender auf der Festplatte im ICS-Dateiformat (iCalendar) speichern.</span><span class="sxs-lookup"><span data-stu-id="61a8c-103">This example shows how to save an entire calendar to disk in the iCalendar (.ics) file format.</span></span>

## <a name="example"></a><span data-ttu-id="61a8c-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="61a8c-104">Example</span></span>

<span data-ttu-id="61a8c-p101">In diesem Codebeispiel wird das [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) -Objekt verwendet, das das Speichern eines ganzen Kalenders oder eines Bereichs von Terminen aus einem Kalender auf einem Datenträger unterstützt. ICS-Dateien werden in Outlook automatisch so optimiert, dass Terminserien nicht als einzelne Termine in der ICS-Datei gespeichert werden. Je nach der Größe des gespeicherten Kalenders kann das Speichern auf einem Datenträger einige Zeit in Anspruch nehmen. Während des Speicherns des Kalenders scheint das Outlook-Fenster dem Benutzer gegenüber nicht zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="61a8c-p101">This code sample uses the [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object that supports saving a whole calendar or a range of appointments from the calendar to disk. Outlook automatically optimizes an .ics file so that recurring appointments are not saved as individual appointments in the .ics file. Depending on the size of the calendar being saved, saving a calendar to disk can take a significant amount of time. While saving the calendar, the Outlook window appears unresponsive to the user.</span></span>

<span data-ttu-id="61a8c-p102">Im Codebeispiel wird zunächst [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) für den Standardordner für Kalender aufgerufen, um ein **CalendarSharing**-Objekt abzurufen. Dann werden Eigenschaften des **CalendarSharing**-Objekts festgelegt, um Kriterien für den Export anzugeben, z. B. ob der ganze Kalender gespeichert werden soll und Details von als privat gekennzeichneten Terminen eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61a8c-p102">The code sample first calls [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) on the default Calendar folder to obtain a **CalendarSharing** object. Then it sets properties of the **CalendarSharing** object to specify criteria for the export, such as whether to save the entire calendar and include details of appointments that are marked "private".</span></span>

<span data-ttu-id="61a8c-111">Damit die Kalenderinformation im ICS-Dateiformat gespeichert werden, wird durch das Codebeispiel die [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\))-Methode des **CalendarSharing**-Objekts aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="61a8c-111">To save the calendar information in .ics file format, the code sample calls the [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) method of the **CalendarSharing** object.</span></span>

<span data-ttu-id="61a8c-112">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="61a8c-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="61a8c-113">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="61a8c-113">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="61a8c-114">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="61a8c-114">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SaveCalendarToDisk(ByVal calendarFileName As String)
    If String.IsNullOrEmpty(calendarFileName) Then
        Throw New ArgumentException( _
        "Parameter must contain a value.", "calendarFileName")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder(_
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = _
        calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = True
    exporter.RestrictToWorkingHours = False
    exporter.IncludeWholeCalendar = True

    '' Save the calendar to disk
    exporter.SaveAsICal(calendarFileName)
End Sub
```


```csharp
private void SaveCalendarToDisk(string calendarFileName)
{
    if (string.IsNullOrEmpty(calendarFileName))
        throw new ArgumentException("calendarFileName", 
        "Parameter must contain a value.");

    Outlook.Folder calendar = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar) as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = true;
    exporter.RestrictToWorkingHours = false;
    exporter.IncludeWholeCalendar = true;

    // Save the calendar to disk
    exporter.SaveAsICal(calendarFileName);
}
```

## <a name="see-also"></a><span data-ttu-id="61a8c-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61a8c-115">See also</span></span>

- [<span data-ttu-id="61a8c-116">Kalender</span><span class="sxs-lookup"><span data-stu-id="61a8c-116">Calendar</span></span>](calendar.md)

