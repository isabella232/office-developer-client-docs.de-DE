---
title: Kanonische Pidlidappointmenttimezonedefinitionenddisplay (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345381"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>Kanonische Pidlidappointmenttimezonedefinitionenddisplay (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Stream, der dem beibehaltenen Format einer [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) -Struktur zugeordnet wird, in der die Beschreibung für die Zeitzone gespeichert wird, die verwendet wird, wenn die Endzeit eines einzelnen Termins oder einer Besprechungsanfrage ausgewählt ist. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Deckel):  <br/> |0x0000825F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Microsoft Office Outlook 2003 oder früher und Lösungen, die auf Collaboration Data Objects (CDO) 1.2.1 basieren und nicht das Kalender Aktualisierungstool für Outlook oder Microsoft Exchange Server ausgeführt haben, speichern Sie die Startzeit und die Endzeit der einzelnen Instanz. Termine und Besprechungsanfragen in koordinierter weltZeit (UTC). Diese Clients speichern keine Informationen für die Zeitzone, in der der Termin oder die Besprechungsanfrage erstellt wird.
  
Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und auf CDO 1.2.1 basierende Lösungen, die das Outlook-oder Exchange Server-Kalender Aktualisierungstool ausgeführt haben, verwenden **dispidApptTZDefEndDisplay** zum Speichern der Zeitzone für die Endzeit. **dispidApptTZDefEndDisplay** zeigt den Termin oder die Besprechung in der ursprünglich geplanten Zeitzone an und bestimmt, ob die Endzeit angepasst werden sollte, wenn sich die Regeln der Zeitzone ändern. Fehlt diese Eigenschaft, wird die von der **dispidApptTZDefStartDisplay** ([pidlidappointmenttimezonedefinitionstartdisplay (](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md))-Eigenschaft angegebene Zeitzone verwendet. Wenn **dispidApptTZDefStartDisplay** fehlt oder ungültig ist, wird die aktuelle lokale Zeitzone angenommen. **dispidApptTZDefEndDisplay** wird nur zu Anzeigezwecken verwendet und nicht in der Serienerweiterung verwendet. 
  
Ein Parser muss beim Lesen eines von **dispidApptTZDefEndDisplay**abgerufenen Streams oder beim Speichern von **TZDEFINITION** in einem Stream für die Verpflichtung zu einer binären Eigenschaft wie **dispidApptTZDefEndDisplay**vorsichtig sein. Weitere Informationen finden Sie unter [Informationen zum Speichern von TZDEFINITION in einem Stream, um eine binäre Eigenschaft zu über](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)nehmen.
  
 **dispidApptTZDefEndDisplay** gibt Zeitzoneninformationen für die **dispidApptEndWhole** ([pidlidappointmentendwhole (](pidlidappointmentendwhole-canonical-property.md))-Eigenschaft an. Das Format, die Einschränkungen und die Berechnung von **dispidApptTZDefEndDisplay** sind identisch mit den Angaben in der **dispidApptTZDefStartDisplay** -Eigenschaft. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

