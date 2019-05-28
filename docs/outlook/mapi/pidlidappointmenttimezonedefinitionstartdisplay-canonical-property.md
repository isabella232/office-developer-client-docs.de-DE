---
title: Kanonische pidlidappointmenttimezonedefinitionstartdisplay (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345017"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Kanonische pidlidappointmenttimezonedefinitionstartdisplay (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Datenstrom, der dem beibehaltenen Format einer [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) -Struktur zugeordnet wird, in der die Beschreibung für die Zeitzone gespeichert wird, die verwendet wird, wenn die Startzeit eines Einzelinstanz-Termins oder einer Besprechungsanfrage ausgewählt wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Eigenschaftengruppe:  <br/> |PSETID_Appointment  <br/> |
|Lange ID (LID):  <br/> |0x0000825E  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Hinweise

Microsoft Office Outlook 2003 oder früher und Lösungen, die auf Zusammenarbeits Datenobjekten (CDO) 1.2.1 basieren und das Tool zum Aktualisieren von Kalendern für Outlook oder Exchange Server nicht ausgeführt haben, speichern Sie die Startzeit und die Endzeit der einzelnen Instanzen. Termine und Besprechungsanfragen in koordinierter Weltzeit (Coordinated Universal Time, UTC). Diese Clients speichern keine Informationen für die Zeitzone, in der der Termin oder die Besprechungsanfrage erstellt wird.
  
Versionen von Outlook seit Microsoft Office Outlook 2007 und auf CDO 1.2.1 basierende Lösungen, die das Outlook-oder Exchange Server-Kalender Update Tool ausgeführt haben, verwenden diese Eigenschaft zum Speichern der Zeitzone für die Startzeit. Die **dispidApptTZDefStartDisplay** -Eigenschaft zeigt den Termin oder die Besprechung in der ursprünglichen Zeitzone an, die geplant wurde. Er bestimmt, ob die Startzeit angepasst werden soll, wenn sich die Regeln der Zeitzone ändern. Wenn diese Eigenschaft nicht vorhanden ist, wird die aktuelle lokale Zeitzone angenommen. Diese Eigenschaft wird nur für Anzeigezwecke verwendet und wird bei der Serienerweiterung nicht verwendet. 
  
Ein Parser muss vorsichtig sein, wenn er einen Stream liest, der von dieser Eigenschaft abgerufen wird, oder wenn er **TZDEFINITION** in einem Stream zur Bindung an eine binäre Eigenschaft wie **dispidApptTZDefStartDisplay**beibehält. Weitere Informationen finden Sie unter [about persistent TZDEFINITION to a Stream to Commit to a binary Property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Diese Eigenschaft gibt Zeitzoneninformationen für die **dispidApptStartWhole** ([pidlidappointmentstartwhole (](pidlidappointmentstartwhole-canonical-property.md))-Eigenschaft an. Der Wert von **dispidApptTZDefStartDisplay** wird verwendet, um Startdatum und-Uhrzeit für Anzeigezwecke von UTC in die lokale Zeitzone zu konvertieren. Für jede von dieser Eigenschaft angegebene **TZRULE** darf das TZRULE_FLAG_RECUR_CURRENT_TZREG-Flag nicht festgelegt werden. Wenn beispielsweise **TZRULE** die effektive Regel ist, muss der Wert des Felds **TZRULE** "0x0002" lauten. Andernfalls muss es sich um "0x0000" handeln. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen..
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage-und Antwortnachrichten an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Definitionen von Datentypen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

