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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361047"
---
# <a name="save-a-calendar-to-disk"></a>Speichern eines Kalenders auf einem Datenträger

Dieses Beispiel zeigt, wie Sie einen ganzen Kalender auf der Festplatte im ICS-Dateiformat (iCalendar) speichern.

## <a name="example"></a>Beispiel

In diesem Codebeispiel wird das [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) -Objekt verwendet, das das Speichern eines ganzen Kalenders oder eines Bereichs von Terminen aus einem Kalender auf einem Datenträger unterstützt. ICS-Dateien werden in Outlook automatisch so optimiert, dass Terminserien nicht als einzelne Termine in der ICS-Datei gespeichert werden. Je nach der Größe des gespeicherten Kalenders kann das Speichern auf einem Datenträger einige Zeit in Anspruch nehmen. Während des Speicherns des Kalenders scheint das Outlook-Fenster dem Benutzer gegenüber nicht zu reagieren.

Im Codebeispiel wird zunächst [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) für den Standardordner für Kalender aufgerufen, um ein **CalendarSharing**-Objekt abzurufen. Dann werden Eigenschaften des **CalendarSharing**-Objekts festgelegt, um Kriterien für den Export anzugeben, z. B. ob der ganze Kalender gespeichert werden soll und Details von als privat gekennzeichneten Terminen eingeschlossen werden sollen.

Damit die Kalenderinformation im ICS-Dateiformat gespeichert werden, wird durch das Codebeispiel die [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\))-Methode des **CalendarSharing**-Objekts aufgerufen.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Calendar](calendar.md)

