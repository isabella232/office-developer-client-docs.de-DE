---
title: Erstellen eines Termins mit Startzeit in der Pacific Time-Zone und Endzeit in der Eastern Time-Zone
TOCTitle: Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone
ms:assetid: ba19532b-df31-4384-8816-e64e6eecbe53
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623388(v=office.15)
ms:contentKeyID: 55119808
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e9a1b9d5f65d8683c08821d4cf0851f599f32030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349455"
---
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a>Erstellen eines Termins mit Startzeit in der Pacific Time-Zone und Endzeit in der Eastern Time-Zone

Gelegentlich kann ein Termin einen Zeitraum überspannen, in dem der Benutzer möglicherweise in eine andere Zeitzone gereist ist, als in der er sich bei Beginn des Termins befand. In diesem Beispiel wird ein Termin erstellt, der in der Pacific Time-Zone (UTC-8) beginnt und in der Eastern Time-Zone (UTC-5) endet.

## <a name="example"></a>Beispiel

In diesem Codebeispiel wird das [TimeZones-Objekt](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) verwendet, das alle in Microsoft Windows erkannten Zeitzonen darstellt. Außerdem wird das [TimeZone-Objekt](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) verwendet, um die [StartTimeZone-Eigenschaft](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) und die [EndTimeZone-Eigenschaft](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) für das [AppointmentItem-Objekt zu](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) festlegen oder zu erhalten.

Outlook zeigt alle Datumsangaben in Ortszeit an, die in der aktuellen Zeitzone des Benutzers ausgedrückt werden, gesteuert durch die Einstellungen des Benutzers in der Windows-Systemsteuerung. Outlook legt auch Eigenschaften wie [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) und [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\))in Ortszeit fest oder ruft diese ab. In Outlook werden Datums- und Uhrzeitwerte jedoch als koordinierte Weltzeit (Coordinated Universal Time, UTC) und nicht als Ortszeit gespeichert. Wenn Sie den internen Wert von Appointment.Start mithilfe des [PropertyAccessor-Objekts](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) untersuchen, würden Sie feststellen, dass der interne Datums- und Uhrzeitwert gleich dem lokalen Datums- und Uhrzeitwert ist, der in den entsprechenden UTC-Datums- und Uhrzeitwert konvertiert wurde.

In Outlook werden Zeitzoneninformationen verwendet, um einen Termin beim Speichern zur richtigen UTC-Zeit und beim Anzeigen des Elements im Kalender zur richtigen lokalen Zeit zuzuordnen. Das Ändern von StartTimeZone wirkt sich auf den Wert von Appointment.Start aus, der immer in der lokalen Zeitzone ausgedrückt wird, dargestellt durch die [CurrentTimeZone-Eigenschaft](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) des Objekts, das von [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\))zurückgegeben wird. Ebenso wirkt sich eine Änderung von EndTimeZoneauf den Wert von Appointment.End aus, der immer in der lokalen Zeit ausgedrückt wird, dargestellt durch die CurrentTimeZone-Eigenschaft des von Application.TimeZones zurückgegebenen Objekts.

Sie können eine bestimmte Zeitzone aus dem TimeZones-Objekt abrufen, indem Sie den ortsunabhängigen Schlüssel für die Zeitzone in der Windows-Registrierung verwenden. Locale-independent TimeZone keys are listed under the following key: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones` .

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```



```vb
Private Sub TimeZoneExample()
    Dim appt As Outlook.AppointmentItem = _
        CType(Application.CreateItem( _
        Outlook.OlItemType.olAppointmentItem), Outlook.AppointmentItem)
    Dim tzs As Outlook.TimeZones = Application.TimeZones
    ' Obtain timezone using indexer and locale-independent key
    Dim tzEastern As Outlook.TimeZone = tzs("Eastern Standard Time")
    Dim tzPacific As Outlook.TimeZone = tzs("Pacific Standard Time")
    appt.Subject = "SEA - JFK Flight"
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM")
    appt.StartTimeZone = tzPacific
    appt.End = DateTime.Parse("8/9/2006 5:30 PM")
    appt.EndTimeZone = tzEastern
    appt.Display(False)
End Sub
```



```csharp
private void TimeZoneExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    Outlook.TimeZones tzs = Application.TimeZones;
    // Obtain timezone using indexer and locale-independent key
    Outlook.TimeZone tzEastern = tzs["Eastern Standard Time"];
    Outlook.TimeZone tzPacific = tzs["Pacific Standard Time"];
    appt.Subject = "SEA - JFK Flight";
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM");
    appt.StartTimeZone = tzPacific;
    appt.End = DateTime.Parse("8/9/2006 5:30 PM");
    appt.EndTimeZone = tzEastern; 
    appt.Display(false);
}
```

## <a name="see-also"></a>Siehe auch

- [Termine](appointments.md)

