---
title: Informationen zum Ausführen eines programmgesteuerten Kalender-Rebase für Sommerzeit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: In diesem Thema wird dieser Zeitraum zwischen Frühling und Herbst als DST-Zeitraum bezeichnet.
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316954"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Informationen zum Ausführen eines programmgesteuerten Kalender-Rebase für Sommerzeit

Viele Länder beobachten Sommerzeit (DST) durch Fortschreiten von Uhren, sodass Abende längeres Tageslicht aufweisen. Dies erfolgt in der Regel durch Festlegen der Uhr eine Stunde vor dem Frühjahr, und Festlegen der Uhr eine Stunde zurück im Herbst. In diesem Thema wird dieser Zeitraum zwischen Frühling und Herbst als DST-Zeitraum bezeichnet. Die meisten Länder verfügen über eigene Regeln für den Beginn und das Ende der SOMMERzeit. Die Datumsangaben des DST-Zeitraums können sich von Jahr zu Jahr ändern, und Benutzer müssen Ihren Microsoft Outlook-Kalender jedes Mal aktualisieren, wenn sich die Sommerzeitregelungen ändern. 
  
Wenn Sie eine Windows Vista-Version oder höher verwenden oder Windows Automatic Update aktiviert haben, sind Sie möglicherweise nicht von der Änderung im DST betroffen. Andernfalls sollten Sie DST-Updates für Windows installieren. Unabhängig davon, ob die Updates automatisch, in Ihrem Namen von einer IT-Abteilung oder von Ihnen als Privatbenutzer installiert werden, werden einige vorhandene Termine, die während des DST-Zeitraums auftreten, möglicherweise fehlerhaft angezeigt, nachdem die DST-Updates für Windows installiert wurden. . Dies gilt sowohl für Terminserien als auch für Einzelinstanzen. Sie müssen diese Termine aktualisieren, damit Sie in Outlook, in Outlook Web App und in Anwendungen, die auf Collaboration Data Objects (CDO) basieren, korrekt angezeigt werden. Das Aktualisieren falsch angezeigter Termine in Kalendern aufgrund der SOMMERzeit wird als Kalender erneute Aktualisierung bezeichnet.
  
Outlook bietet Tools für Benutzer und Exchange Server stellt Tools für Administratoren zur Verfügung. Outlook stellt das Time Zone Data Update-Tool für Outlook-Benutzer bereit. Mit diesem Tool können Benutzer ihre eigenen Kalender aktualisieren. Exchange Server stellt das Exchange-Kalender Aktualisierungstool bereit, mit dem Administratoren Schwierigkeiten vermeiden können, die sich aus der Bereitstellung des Outlook-Tools für alle Benutzer ergeben, und um sicherzustellen, dass jeder Benutzer das Outlook-Tool ordnungsgemäß ausführt.
  
Zusätzlich dazu, dass Benutzer das Time Zone Data Update-Tool oder Administratoren ausführen, um das Exchange-Kalender Aktualisierungstool auszuführen, können Entwickler von Drittanbieter-MAPI-Client Software eine DLL, Tzmovelib. dll, herunterladen. Mithilfe dieser Assembly können Entwickler dieselben APIs verwenden, die Outlook und Exchange Server in Ihren Kalender-Wiederverwendungs Tools verwenden. 

In der folgenden Liste sind die Kalender-wiederbasierten APIs aufgeführt:
  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
    
- [IOlkApptRebaser](iolkapptrebaser.md)
    
- [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)
    
- [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)
    
- [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)
    
- [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)
    
- [Pidlidappointmenttimezonedefinitionenddisplay (](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [Pidlidappointmenttimezonedefinitionrecur (](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [Pidlidappointmenttimezonedefinitionstartdisplay (](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [Pidlidtimezonestruct (](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [RebaseTaskComplete](rebasetaskcomplete.md)
    
- [RebaseTaskProgress](rebasetaskprogress.md)
    
- [TZDEFINITION](tzdefinition.md)
    
- [TZREG](tzreg.md)
    
- [TZRULE](tzrule.md)
    
Sie können das folgende Verfahren verwenden, um ein Termin-Wiederverwendungs Tool mithilfe der APIs für die Kalender Zurücksetzung zu schreiben:
  
1. Verwenden Sie **IOlkApptRebaser:: beginenumerateappointmentsabgerufen** und **IOlkApptRebaser:: endenumerateappointmentsabgerufen** , um Termine zu finden, die Kandidaten für die neubasis sind. Geben Sie gegebenenfalls Informationen an, damit der Benutzer entscheiden kann, welche Termine erneut festgelegt werden sollen. Alternativ können Sie MAPI oder das Outlook-Objektmodell verwenden, um die Zeit-und Serieninformationen für einen Termin zu untersuchen, indem Sie die **pidlidappointmenttimezonedefinitionstartdisplay (**, **pidlidappointmenttimezonedefinitionenddisplay (**, -und **pidlidappointmenttimezonedefinitionrecur (** -Eigenschaft. 
    
2. Verwenden Sie **HrCreateApptRebaser**, **IOlkApptRebaser:: beginrebaseappointmentsabgerufen**und **IOlkApptRebaser:: EndRebaseAppointments** , um den Termin aufzuteilen. 
    
Um die Tzmovelib. dll-Assembly abzurufen, laden Sie das Redistributable-Installationsprogramm von OutlookTimeZoneMoveLibRedist. exe und die Tzmovelib. h-Headerdatei unter [Outlook 2010: Erweiterungs Verweis redistributAble Installer and Header File for Recalendar](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b) . Dieser Download funktioniert für Outlook 2010 und spätere Versionen von Outlook. OutlookTimeZoneMoveLibRedist. exe installiert die Tzmovelib. dll-Assemblydatei in C:\Program Files\MsExTmz. Beachten Sie, dass Drittanbieter-Kalender, die Anwendungen neu bebauen können, nur das Installationsprogramm OutlookTimeZoneMoveLibRedist. exe verteilen dürfen und die Assembly, die Tzmovelib. dll oder alle anderen extrahierten Komponenten nicht separat vom Installationsprogramm verteilen müssen.
  
## <a name="see-also"></a>Siehe auch

- [Informationen zum Beibehalten von TZDEFINITION in einem Stream, um eine binäre Eigenschaft zu übernehmen](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZDEFINITION-Struktur](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZREG-Struktur](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Lesen von Zeitzoneneigenschaften aus einem Termin](how-to-read-time-zone-properties-from-an-appointment.md)
- [Hilfe-und Support Center für Sommerzeit](https://support.microsoft.com/gp/cp_dst)
- [Behandeln von Sommerzeit mithilfe des Exchange-Kalender Aktualisierungstools](https://support.microsoft.com/kb/941018)
- [So adressieren Sie Zeitzonenänderungen mithilfe des Time Zone Data Update-Tools für Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

