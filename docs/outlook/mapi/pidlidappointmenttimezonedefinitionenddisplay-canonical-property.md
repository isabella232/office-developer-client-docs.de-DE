---
title: PidLidAppointmentTimeZoneDefinitionEndDisplay (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 442de37a31b53384a9ce4cc5ef24b8f33a6c6d6c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583926"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionEndDisplay (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Datenstrom, der dem beibehaltenen Format einer [TZDEFINITION-Struktur](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) zugeordnet ist, in dem die Beschreibung für die Zeitzone gespeichert wird, die verwendet wird, wenn die Endzeit eines Termins oder einer Besprechungsanfrage mit einer Instanz ausgewählt wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x0000825F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Microsoft Office Outlook 2003 oder früher und Lösungen, die auf Collaboration Data Objects (CDO) 1.2.1 basieren und das Kalenderaktualisierungstool für Outlook oder Microsoft Exchange Server nicht ausgeführt haben, speichern Sie die Start- und Endzeit von Terminen und Besprechungsanfragen mit einer Instanz in koordinierter Weltzeit (UTC). Diese Clients speichern keine Informationen für die Zeitzone, in der die Termin- oder Besprechungsanfrage erstellt wird.
  
Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und Lösungen, die auf CDO 1.2.1 basieren und das Outlook- oder Exchange Server Kalenderaktualisierungstool ausgeführt haben, verwenden **dispidApptTZDefEndDisplay,** um die Zeitzone für die Endzeit zu speichern. **dispidApptTZDefEndDisplay** zeigt den Termin oder die Besprechung in der ursprünglichen Zeitzone an, die geplant wurde, und bestimmt, ob die Endzeit angepasst werden soll, wenn sich die Regeln der Zeitzone ändern. Wenn diese Eigenschaft fehlt, wird die zeitzone verwendet, die von der **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) -Eigenschaft angegeben wird. Wenn **dispidApptTZDefStartDisplay** fehlt oder ungültig ist, wird die aktuelle lokale Zeitzone angenommen. **dispidApptTZDefEndDisplay** wird nur zu Anzeigezwecken verwendet und nicht bei Serienerweiterungen verwendet. 
  
Ein Parser muss vorsichtig sein, wenn er einen stream liest, der aus **dispidApptTZDefEndDisplay** abgerufen wurde, oder wenn **TZDEFINITION** in einem Stream gespeichert wird, um eine Bindung an eine binäre Eigenschaft wie **dispidApptTZDefEndDisplay** zu erhalten. Weitere Informationen finden Sie unter [Informationen zum Beibehalten von TZDEFINITION in einem Stream, um einen Commit für eine binäre Eigenschaft auszuführen.](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)
  
 **dispidApptTZDefEndDisplay** gibt Zeitzoneninformationen für die **Eigenschaft dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) an. Das Format, die Einschränkungen und die Berechnung von **dispidApptTZDefEndDisplay** entsprechen den Angaben in der **dispidApptTZDefStartDisplay-Eigenschaft.** 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

