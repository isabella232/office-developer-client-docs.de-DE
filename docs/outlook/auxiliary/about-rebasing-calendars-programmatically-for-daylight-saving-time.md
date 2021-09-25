---
title: Informationen zum Ausführen eines programmgesteuerten Kalender-Rebase für Sommerzeit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: In diesem Thema wird dieser Zeitraum zwischen Dem Spring und Fall als DST-Zeitraum bezeichnet.
ms.openlocfilehash: fba3238543630d3960e41abae427a9757c387639
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614472"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Informationen zum Ausführen eines programmgesteuerten Kalender-Rebase für Sommerzeit

In vielen Ländern wird sommerliche Sommerzeit (Daylight Saving Time, DST) beobachtet, indem die Uhr aktualisiert wird, sodass die Nacht länger sommert. Dies geschieht in der Regel durch festlegen der Uhr eine Stunde im Voraus im Federn und die Uhr eine Stunde zurück im Herbst. In diesem Thema wird dieser Zeitraum zwischen Dem Spring und Fall als DST-Zeitraum bezeichnet. In den meisten Ländern gelten eigene Vorschriften für den Zeitpunkt, an dem DST beginnt und endet. Die Daten des DST-Zeitraums können sich von Jahr zu Jahr ändern, und Benutzer müssen ihren Microsoft Outlook Kalender jedes Mal aktualisieren, wenn sich die DST-Bestimmungen ändern. 
  
Wenn Sie eine Version von Windows verwenden, die Windows Vista oder höher ist oder Windows automatische Update aktiviert ist, sind Sie möglicherweise nicht von der Änderung in DST betroffen. Andernfalls sollten Sie DST-Updates für Windows installieren. Unabhängig davon, ob die Updates automatisch, in Ihrem Auftrag von einer IT-Abteilung oder selbst als Privatbenutzer installiert werden, werden bei einigen vorhandenen Terminen, die während des DST-Zeitraums auftreten, möglicherweise falsche Zeiten angezeigt, nachdem die DST-Updates für Windows installiert wurden. Dies gilt sowohl für Terminserien als auch für Einzelinstanztermine. Sie müssen diese Termine aktualisieren, damit sie in Outlook, in Outlook Web App und in Anwendungen, die auf CdO (Collaboration Data Objects) basieren, korrekt angezeigt werden. Das Aktualisieren falsch angezeigter Termine in Kalendern aufgrund von DST wird als Neubasierung von Kalendern bezeichnet.
  
Outlook stellt Tools für Benutzer bereit, und Exchange Server bietet Administratoren Tools zum Neubasisn von Kalendern. Outlook stellt das Tool zum Aktualisieren von Zeitzonendaten für Outlook Benutzer bereit. Mit diesem Tool können Benutzer ihre eigenen Kalender aktualisieren. Exchange Server bietet das Exchange Kalenderaktualisierungstool, das Administratoren dabei hilft, Probleme zu vermeiden, die durch die umfassende Bereitstellung des Outlook-Tools für alle Benutzer entstehen, und um sicherzustellen, dass jeder Benutzer das Outlook-Tool ordnungsgemäß ausführt.
  
Zusätzlich dazu, dass Benutzer das Time Zone Data Update-Tool oder Administratoren ausführen, um das Exchange Kalenderaktualisierungstool auszuführen, können MAPI-Clientsoftwareentwickler von Drittanbietern eine DLL Tzmovelib.dll herunterladen. Mithilfe dieser Assembly können Entwickler die gleichen APIs verwenden, die Outlook und Exchange Server in ihren Tools für die Kalenderumbasierung verwenden. 

In der folgenden Liste sind die APIs für die Kalenderumbasierung aufgeführt:
  
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
    
Zum Schreiben eines Tools zum Neubasieren von Terminen mithilfe der KALENDER-APIs können Sie das folgende Verfahren verwenden:
  
1. Verwenden Sie **"IOlkApptRebaser::BeginEnumerateAppointments"** und **"IOlkApptRebaser::EndEnumerateAppointments",** um Termine zu suchen, die kandidaten für die Neubasierung sind. Stellen Sie bei Bedarf Informationen bereit, damit der Benutzer entscheiden kann, welche Termine neu erstellt werden sollen. Alternativ können Sie mapi oder das Outlook-Objektmodell verwenden, um die Zeit- und Serieninformationen für einen Termin zu untersuchen, indem Sie die Eigenschaften **PidLidAppointmentTimeZoneDefinitionStartDisplay,** **PidLidAppointmentTimeZoneDefinitionEndDisplay** und **PidLidAppointmentTimeZoneDefinitionRecur** analysieren. 
    
2. Verwenden Sie **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments** und **IOlkApptRebaser::EndRebaseAppointments,** um den Termin neu zubasen. 
    
Um die Tzmovelib.dll Assembly abzurufen, laden Sie das OutlookTimeZoneMoveLibRedist.exe redistributable Installer und die Headerdatei Tzmovelib.h unter [Outlook 2010: Auxiliary Reference Redistributable Installer and Header File for Rebasing Calendars](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)herunter. Dieser Download funktioniert für Outlook 2010 und neuere Versionen von Outlook. OutlookTimeZoneMoveLibRedist.exe installiert die Tzmovelib.dll-Assemblydatei in "C:\Programme\MsExTmz". Beachten Sie, dass Drittanbieter-Kalender-Neubasierungsanwendungen nur das Installationsprogramm, OutlookTimeZoneMoveLibRedist.exe weitervertreiben können und die Assembly, Tzmovelib.dll oder andere extrahierte Komponenten nicht separat vom Installationsprogramm weitervertreiben dürfen.
  
## <a name="see-also"></a>Siehe auch

- [Informationen zum Beibehalten von TZDEFINITION in einem Stream, um eine binäre Eigenschaft zu übernehmen](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZDEFINITION-Struktur](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZREG-Struktur](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Lesen von Zeitzoneneigenschaften aus einem Termin](how-to-read-time-zone-properties-from-an-appointment.md)
- [Hilfe und Supportcenter für Sommerzeit](https://support.microsoft.com/gp/cp_dst)
- [So behandeln Sie Sommerzeit mithilfe des Exchange Kalenderaktualisierungstools](https://support.microsoft.com/kb/941018)
- [Vorgehensweise Beheben von Zeitzonenänderungen mithilfe des Tools zum Aktualisieren von Zeitzonen für Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

