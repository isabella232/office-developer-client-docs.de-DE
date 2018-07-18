---
title: Informationen zum Ausführen eines programmgesteuerten Kalender-Rebase für Sommerzeit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: 'In diesem Thema wird in diesem Zeitraum zwischen dem: Spirale und werden, die als die sommerzeitperiode bezeichnet.'
ms.openlocfilehash: 4787b2143b3f5d1f0400524f0da82e19e2cbed8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790918"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Informationen zum Ausführen eines programmgesteuerten Kalender-Rebase für Sommerzeit

Viele Länder beobachten Sommerzeit (Ziel) von Uhren vorwärts verschoben, sodass abends länger Sommerzeit haben. Dies erfolgt in der Regel durch Festlegen der Uhr eine Stunde lang in die Spirale und Einstellen der Uhr eine Stunde wieder in den fallen. In diesem Thema wird in diesem Zeitraum zwischen dem: Spirale und werden, die als die sommerzeitperiode bezeichnet. Die meisten Ländern haben ihre eigenen Vorschriften Sommerzeit beginnt und endet. Das Datum, von die sommerzeitperiode können von Jahr zu Jahr ändern, und Benutzer müssen Aktualisieren ihrer Microsoft Outlook-Kalender jedes Mal, dass die neuen Sommerzeitregeln Vorschriften ändern. 
  
Wenn Sie eine Version von Windows verwenden, Windows Vista ist, oder höher, oder Windows automatische Updates aktiviert haben, können Sie nicht durch die Änderung der Sommerzeit betroffen. Anderenfalls sollten Sie die neuen Sommerzeitregeln Updates für Windows installieren. Unabhängig davon, ob die Updates automatisch in Ihrem Auftrag von der IT-Abteilung oder von sich selbst als ein Privatbenutzer installiert sind möglicherweise einige vorhandene Termine, die auftreten, bei die sommerzeitperiode angezeigt, nach der Installation der Updates Sommerzeit für Windows falsche mehrmals . Dies gilt für Termine wiederkehrende und Einzel-Instanz. Aktualisieren Sie diese Termine um korrekt angezeigt wird in Outlook, Outlook Web App und Anwendungen, die auf der Windows-Verwaltungsinstrumentation (Collaboration Data Objects, CDO) basieren. Aktualisieren falsch angezeigten Termine in Kalendern aufgrund der Sommerzeit wird als Neuzuordnen von Kalendern bezeichnet.
  
Outlook bietet Tools für Benutzer und Exchange Server bietet Tools für Administratoren Rebase Kalender. Outlook bietet die Zeit Zeitzonendaten für Outlook-Benutzer. Mit diesem Tool können Benutzer ihre eigenen Kalender aktualisieren. Exchange Server bietet Exchange Calendar Update-Tool, das hilft Administratoren, um Probleme zu vermeiden, die bei der Bereitstellung des Outlook-Tools großem Maß an alle Benutzer und dafür sorgen, dass jeder Benutzer das Outlook-Tool ordnungsgemäß ausgeführt wird.
  
Zusätzlich zum Vertrauen in Benutzern das Ausführen der Zeit Zeitzonendaten oder Administratoren den Exchange Calendar Update-Tool ausführen, können Drittanbieter-MAPI-Client-Software-Entwicklern eine DLL sein; Tzmovelib.dll herunterladen. Mithilfe dieser Assembly können Entwickler die gleichen APIs, die Outlook und Exchange Server in ihren Kalender Neuzuordnen von Tools verwenden. 

In der folgenden Liste werden die APIs Neuzuordnen:
  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
    
- [IOlkApptRebaser](iolkapptrebaser.md)
    
- [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)
    
- [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)
    
- [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)
    
- [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)
    
- [PidLidAppointmentTimeZoneDefinitionEndDisplay](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionRecur](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionStartDisplay](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [RebaseTaskComplete](rebasetaskcomplete.md)
    
- [RebaseTaskProgress](rebasetaskprogress.md)
    
- [TZDEFINITION](tzdefinition.md)
    
- [TZREG](tzreg.md)
    
- [TZRULE](tzrule.md)
    
Um einen Termin zurücksetzungstool mithilfe des Kalenders Neuzuordnen von APIs zu schreiben, können Sie die folgende Schritte aus:
  
1. Verwenden Sie **IOlkApptRebaser::BeginEnumerateAppointments** und **IOlkApptRebaser::EndEnumerateAppointments** , um Termine zu erhalten, die zum Neuzuordnen von geeignet sind. Bei Bedarf Informationen zum Aktivieren des Benutzers entscheiden, welche Termine Rebase präsentieren. Verwenden Sie alternativ MAPI oder Outlook-Objektmodell, um die Zeit- und Serie Informationen für einen Termin zu überprüfen, indem Sie die Analyse der **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay**, und **PidLidAppointmentTimeZoneDefinitionRecur** -Eigenschaften. 
    
2. Verwenden Sie **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments**und **IOlkApptRebaser::EndRebaseAppointments** auf Basis des Termins. 
    
Die Assembly Tzmovelib.dll Herunterladen der OutlookTimeZoneMoveLibRedist.exe redistributable Installer und Headerdatei Tzmovelib.h am [Outlook 2010: Hilfs-Referenz Redistributable Installer und Headerdatei zum Neuzuordnen von Kalendern](http://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b) . Dieser Download kann für Outlook 2010 und höheren Versionen von Outlook. OutlookTimeZoneMoveLibRedist.exe installiert die Assemblydatei Tzmovelib.dll in c:\Programme\Microsoft Files\MsExTmz. Beachten Sie diesen Neuzuordnen von Anwendungen von Drittanbietern Kalender kann nur das Installationsprogramm OutlookTimeZoneMoveLibRedist.exe, verteilen und muss nicht die Assembly, Tzmovelib.dll oder andere extrahierten Komponenten separat vom Installer verteilen.
  
## <a name="see-also"></a>Siehe auch

- [Zum Speichern von TZDEFINITION in einen Stream zu einer binären Eigenschaft anvertrauen](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZDEFINITION-Struktur](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZREG-Struktur](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Lesen von Zeitzoneneigenschaften aus einem Termin](how-to-read-time-zone-properties-from-an-appointment.md)
- [Sommerzeit Hilfe- und Supportcenter](http://support.microsoft.com/gp/cp_dst)
- [Gewusst wie: Sommerzeit mithilfe des Exchange Calendar Update-Tools](http://support.microsoft.com/kb/941018)
- [Wie Adresse, Zeitzone Änderungen mithilfe der Zeit Zeitzonendaten für Microsoft Office Outlook](http://support.microsoft.com/kb/931667)

