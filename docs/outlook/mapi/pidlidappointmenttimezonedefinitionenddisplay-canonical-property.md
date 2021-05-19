---
title: PidLidAppointmentTimeZoneDefinitionEndDisplay (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345381"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionEndDisplay (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Datenstrom, der dem dauerhaften Format einer [TZDEFINITION-Struktur](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) zu ordnet, der die Beschreibung für die Zeitzone speichert, die verwendet wird, wenn die Endzeit eines Termins oder einer Besprechungsanfrage mit einer einzigen Instanz ausgewählt wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Lange ID (LID):  <br/> |0x0000825F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Hinweise

Microsoft Office Outlook 2003 oder früheren Versionen und Lösungen, die auf #A0 (Collaboration Data Objects, CDO) 1.2.1 basieren und das Kalenderaktualisierungstool für Outlook oder Microsoft Exchange Server nicht ausgeführt haben, speichern Sie die Start- und Endzeit von Terminen und Besprechungsanfragen in koordinierter Weltzeit (Coordinated Universal Time, UTC). Diese Clients speichern keine Informationen für die Zeitzone, in der der Termin oder die Besprechungsanfrage erstellt wird.
  
Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und Lösungen, die auf CDO 1.2.1 basieren, die das Outlook- oder Exchange Server-Kalenderupdatetool ausgeführt haben, verwenden **dispidApptTZDefEndDisplay,** um die Zeitzone für die Endzeit zu speichern. **dispidApptTZDefEndDisplay** zeigt den Termin oder die Besprechung in der ursprünglich geplanten Zeitzone an und bestimmt, ob die Endzeit angepasst werden soll, wenn sich die Regeln der Zeitzone ändern. Wenn diese Eigenschaft fehlt, wird die zeitzone verwendet, die durch die **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) -Eigenschaft angegeben wird. Wenn **dispidApptTZDefStartDisplay** fehlt oder ungültig ist, wird die aktuelle lokale Zeitzone angenommen. **dispidApptTZDefEndDisplay** wird nur zu Anzeigezwecken verwendet und nicht in der Serienerweiterung verwendet. 
  
Ein Parser muss vorsichtig sein, wenn er einen Datenstrom aus **dispidApptTZDefEndDisplay** liest oder **wenn er TZDEFINITION** für die Verpflichtung zu einer binären Eigenschaft wie **dispidApptTZDefEndDisplay** in einem Datenstrom beibehalten. Weitere Informationen finden Sie unter [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefEndDisplay** gibt Zeitzoneninformationen für die **eigenschaft dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) an. Das Format, die Einschränkungen und die Berechnung von **dispidApptTZDefEndDisplay** sind identisch mit der in der **eigenschaft dispidApptTZDefStartDisplay** angegebenen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

