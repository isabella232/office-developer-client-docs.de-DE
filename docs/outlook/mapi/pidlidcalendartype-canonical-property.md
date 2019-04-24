---
title: Kanonische Pidlidcalendartype (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6a33559a3e047890153f6a8e0ab40e49c2bf80cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341993"
---
# <a name="pidlidcalendartype-canonical-property"></a>Kanonische Pidlidcalendartype (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Wert des Felds CalendarType aus der **dispidApptRecur** ([pidlidappointmentrecur (](pidlidappointmentrecur-canonical-property.md))-Eigenschaft an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |LID_CALENDAR_TYPE  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Meeting  <br/> |
|Long-ID (Deckel):  <br/> |0x0000001C  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die Besprechungsanfrage eine wiederkehrende Reihe oder eine Ausnahme darstellt, ist dies der Wert des Felds CalendarType aus der **dispidApptRecur** -Eigenschaft. Andernfalls wird diese Eigenschaft nicht festgelegt, und es wird angenommen, dass Sie 0 ist. 
  
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

