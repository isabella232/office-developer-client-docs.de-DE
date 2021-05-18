---
title: Informationen zum Ausführen eines programmgesteuerten Kalender-Rebase für Sommerzeit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: In diesem Thema wird dieser Zeitraum zwischen dem Frühjahr und dem Herbst als DST-Zeitraum bezeichnet.
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316954"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Informationen zum Ausführen eines programmgesteuerten Kalender-Rebase für Sommerzeit

Viele Länder beobachten sommerzeit (Sommerzeit, DST), indem sie die Uhr so vorrücken, dass die Abende länger hell sind. Dies geschieht in der Regel, indem die Uhr im Frühjahr eine Stunde voraus und die Uhr im Herbst um eine Stunde zurück festlegen wird. In diesem Thema wird dieser Zeitraum zwischen dem Frühjahr und dem Herbst als DST-Zeitraum bezeichnet. Die meisten Länder verfügen über eigene Vorschriften für den Beginn und das Ende von DST. Die Datumsangaben des DST-Zeitraums können sich von Jahr zu Jahr ändern, und Benutzer müssen ihren Microsoft Outlook kalender jedes Mal aktualisieren, wenn sich die Bestimmungen des Berichtszeitraums ändern. 
  
Wenn Sie eine Version von Windows verwenden, die Windows Vista oder höher ist, oder wenn Windows automatisches Update aktiviert ist, sind Sie möglicherweise nicht von der Änderung in DST betroffen. Andernfalls sollten Sie DST-Updates für Windows. Unabhängig davon, ob die Updates automatisch installiert werden, in Ihrem Auftrag durch eine IT-Abteilung oder selbst als Heimbenutzer, werden bei einigen vorhandenen Terminen, die während des DST-Zeitraums auftreten, möglicherweise falsche Zeiten angezeigt, nachdem die DST-Updates für Windows installiert wurden. Dies gilt sowohl für Terminserien als auch für Termine mit einer instanz. Sie müssen diese Termine so aktualisieren, dass sie ordnungsgemäß in Outlook, in Outlook Web App und in Anwendungen angezeigt werden, die auf #A0 (Collaboration Data Objects, CDO) basieren. Das Aktualisieren falsch angezeigter Termine in Kalendern aufgrund von DST wird als Neubasieren von Kalendern bezeichnet.
  
Outlook bietet Tools für Benutzer und Exchange Server bietet Tools für Administratoren zum Neubasieren von Kalendern. Outlook stellt das Time Zone Data Update Tool für benutzer Outlook zur Verfügung. Mit diesem Tool können Benutzer eigene Kalender aktualisieren. Exchange Server stellt das Exchange Calendar Update Tool zur Verfügung, das Administratoren dabei hilft, Schwierigkeiten zu vermeiden, die sich aus der bereitstellung des Outlook-Tools für alle Benutzer und damit sicherstellen, dass jeder Benutzer das tool ordnungsgemäß Outlook kann.
  
Zusätzlich zur Ausführung des Exchange-Kalenderupdatetools können Entwickler von MapI-Clientsoftware von Drittanbietern nicht nur das Time Zone Data Update Tool ausführen, sondern auch eine DLL herunterladen, die Tzmovelib.dll. Mithilfe dieser Assembly können Entwickler die gleichen APIs verwenden, die Outlook und Exchange Server in ihren Kalenderbasierungstools verwenden. 

In der folgenden Liste sind die Kalenderbasierungs-APIs aufgeführt:
  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
    
- [IOlkApptRebaser](iolkapptrebaser.md)
    
- [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)
    
- [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)
    
- [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)
    
- [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)
    
- [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [RebaseTaskComplete](rebasetaskcomplete.md)
    
- [RebaseTaskProgress](rebasetaskprogress.md)
    
- [TZDEFINITION](tzdefinition.md)
    
- [TZREG](tzreg.md)
    
- [TZRULE](tzrule.md)
    
Zum Schreiben eines Tools zum Neubasieren von Terminen mithilfe der Kalenderbasierungs-APIs können Sie das folgende Verfahren verwenden:
  
1. Verwenden **Sie IOlkApptRebaser::BeginEnumerateAppointments** und **IOlkApptRebaser::EndEnumerateAppointments,** um Termine zu finden, die kandidaten für die Neubasierung sind. Geben Sie gegebenenfalls Informationen an, damit der Benutzer entscheiden kann, welche Termine neu basisiert werden sollen. Alternativ können Sie MAPI oder das Outlook-Objektmodell verwenden, um die Zeit- und Serieninformationen für einen Termin zu untersuchen, indem Sie die **Eigenschaften PidLidAppointmentTimeZoneDefinitionStartDisplay,** **PidLidAppointmentTimeZoneDefinitionEndDisplay** und **PidLidAppointmentTimeZoneDefinitionRecur** überprüfen. 
    
2. Verwenden **Sie HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments** und **IOlkApptRebaser::EndRebaseAppointments,** um den Termin neu zu erstellen. 
    
Um die Tzmovelib.dll-Assembly zu erhalten, laden Sie das OutlookTimeZoneMoveLibRedist.exe redistributable Installer und die Tzmovelib.h-Headerdatei unter [Outlook 2010 herunter: Hilfsreferenz Redistributable Installer und Header File for Rebasing Calendars](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b). Dieser Download funktioniert für Outlook 2010 und höher versionen von Outlook. OutlookTimeZoneMoveLibRedist.exe installiert die Tzmovelib.dll in C:\Program Files\MsExTmz. Beachten Sie, dass Neubasierungsanwendungen von Drittanbietern nur das Installationsprogramm, OutlookTimeZoneMoveLibRedist.exe und nicht die Assembly, Tzmovelib.dll oder andere extrahierte Komponenten separat vom Installationsprogramm neu verteilen können.
  
## <a name="see-also"></a>Siehe auch

- [Informationen zum Beibehalten von TZDEFINITION in einem Stream, um eine binäre Eigenschaft zu übernehmen](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZDEFINITION-Struktur](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZREG-Struktur](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Lesen von Zeitzoneneigenschaften aus einem Termin](how-to-read-time-zone-properties-from-an-appointment.md)
- [Hilfe- und Supportcenter für Sommerzeit](https://support.microsoft.com/gp/cp_dst)
- [So adressiere ich Sommerzeit mithilfe des Exchange Kalenderaktualisierungstools](https://support.microsoft.com/kb/941018)
- [So adressiere ich Zeitzonenänderungen mithilfe des Time Zone Data Update Tools für Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

