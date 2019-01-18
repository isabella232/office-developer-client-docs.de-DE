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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698715"
---
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a><span data-ttu-id="b1942-102">Erstellen eines Termins mit Startzeit in der Pacific Time-Zone und Endzeit in der Eastern Time-Zone</span><span class="sxs-lookup"><span data-stu-id="b1942-102">Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone</span></span>

<span data-ttu-id="b1942-p101">Gelegentlich kann ein Termin einen Zeitraum überspannen, in dem der Benutzer möglicherweise in eine andere Zeitzone gereist ist, als in der er sich bei Beginn des Termins befand. In diesem Beispiel wird ein Termin erstellt, der in der Pacific Time-Zone (UTC-8) beginnt und in der Eastern Time-Zone (UTC-5) endet.</span><span class="sxs-lookup"><span data-stu-id="b1942-p101">Occasionally, an appointment may span over a period of time during which the user may have traveled to a different time zone than when the appointment starts. This example creates an appointment that begins in the Pacific Time Zone (UTC-8) and ends in the Eastern Time Zone (UTC-5).</span></span>

## <a name="example"></a><span data-ttu-id="b1942-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b1942-105">Example</span></span>

<span data-ttu-id="b1942-p102">In diesem Codebeispiel wird das [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) -Objekt verwendet, das alle in Microsoft Windows erkannten Zeitzonen darstellt. Außerdem wird das [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) -Objekt verwendet, um die [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) -Eigenschaft und die [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) -Eigenschaft des [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) -Objekts abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b1942-p102">This code sample uses the [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) object that represents all the time zones recognized in Microsoft Windows. It also uses the [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) object to set or get the [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) property and the [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) property on the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="b1942-108">Outlook zeigt alle Datumsangaben in lokaler Uhrzeit an, die in der aktuellen Zeitzone des Benutzers ausgedrückt sind, welche von den Einstellungen des Benutzers in der Windows-Systemsteuerung gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="b1942-108">Outlook displays all dates in local time, which is expressed in the user's current time zone, controlled by the user's settings in the Windows Control Panel.</span></span> <span data-ttu-id="b1942-109">Outlook legt auch die Eigenschaften wie [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) und [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) in der lokalen Uhrzeit fest oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="b1942-109">Outlook also sets or gets properties, such as [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), in local time.</span></span> <span data-ttu-id="b1942-110">Outlook speichert jedoch Datums-und Uhrzeitwerte in UTC statt in der lokalen Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="b1942-110">However, Outlook stores date and time values as Coordinated Universal Time (UTC) rather than local time.</span></span> <span data-ttu-id="b1942-111">Wenn Sie mit den internen Wert von Appointment.Start mit dem [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))-Objekt prüfen, stellen Sie fest, dass der interne Datums- und Uhrzeitwert dem lokalen Datums- und Uhrzeitwert entspricht, der in den entsprechenden UTC-Datums- und Uhrzeitwert konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b1942-111">If you examine the internal value of Appointment.Start by using the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object, you would find the internal date and time value is equal to the local date and time value converted to the equivalent UTC date and time value.</span></span>

<span data-ttu-id="b1942-112">In Outlook werden Zeitzoneninformationen verwendet, um einen Termin beim Speichern zur richtigen UTC-Zeit und beim Anzeigen des Elements im Kalender zur richtigen lokalen Zeit zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b1942-112">Outlook uses the time zone information to map the appointment to the correct UTC time when it saves an appointment, and into the correct local time when it displays the item in the calendar.</span></span> <span data-ttu-id="b1942-113">Eine Änderung von StartTimeZone wirkt sich auf den Wert von Appointment.Start aus, der immer in der lokalen Zeitzone ausgedrückt wird, dargestellt durch die [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\))-Eigenschaft des von [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)) zurückgegebenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="b1942-113">Changing StartTimeZone affects the value of Appointment.Start, which is always expressed in the local time zone, represented by the [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) property of the object returned by [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)).</span></span> <span data-ttu-id="b1942-114">Ebenso wirkt sich eine Änderung von EndTimeZoneauf den Wert von Appointment.End aus, der immer in der lokalen Zeit ausgedrückt wird, dargestellt durch die CurrentTimeZone-Eigenschaft des von Application.TimeZones zurückgegebenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="b1942-114">Similarly, changing EndTimeZone affects the value of Appointment.End, which is always expressed in the local time zone, represented by the CurrentTimeZone property of the object returned by Application.TimeZones.</span></span>

<span data-ttu-id="b1942-115">Sie können eine bestimmte Zeitzone vom TimeZones-Objekt abrufen, indem Sie den vom Gebietsschema unabhängigen Schlüssel für TimeZone in der Windows-Registrierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1942-115">You can retrieve a specific TimeZone from the TimeZones object by using the locale-independent key for the TimeZone in the Windows registry.</span></span> <span data-ttu-id="b1942-116">Die vom Gebietsschema unabhängigen TimeZone-Schlüssel werden unter dem folgenden Schlüssel aufgelistet: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.</span><span class="sxs-lookup"><span data-stu-id="b1942-116">Locale-independent TimeZone keys are listed under the following key: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.</span></span>

<span data-ttu-id="b1942-117">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="b1942-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b1942-118">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b1942-118">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b1942-119">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="b1942-119">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


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

## <a name="see-also"></a><span data-ttu-id="b1942-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1942-120">See also</span></span>

- [<span data-ttu-id="b1942-121">Termine</span><span class="sxs-lookup"><span data-stu-id="b1942-121">Appointments</span></span>](appointments.md)

