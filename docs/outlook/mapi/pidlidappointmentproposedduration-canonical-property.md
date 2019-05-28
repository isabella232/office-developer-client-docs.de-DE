---
title: Kanonische pidlidappointmentproposedduration (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentProposedDuration
api_type:
- COM
ms.assetid: 37806778-a19a-4905-a845-525d3912bf9e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 56a652e630af70d4cfde12995951a352a1aa97e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356378"
---
# <a name="pidlidappointmentproposedduration-canonical-property"></a>Kanonische pidlidappointmentproposedduration (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den vorgeschlagenen Wert für die **dispidApptDuration** ([pidlidappointmentduration (](pidlidappointmentduration-canonical-property.md))-Eigenschaft für einen Leistungsindikator Vorschlag an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptProposedDuration  <br/> |
|Eigenschaftengruppe:  <br/> |PSETID_Appointment  <br/> |
|Lange ID (LID):  <br/> |0x00008256  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn dieser Wert festgelegt ist, muss er der Anzahl von Minuten zwischen den Eigenschaften **dispidApptProposedStartWhole** ([pidlidappointmentproposedstartwhole (](pidlidappointmentproposedstartwhole-canonical-property.md)) und **dispidApptProposedEndWhole** ([pidlidappointmentproposedendwhole (](pidlidappointmentproposedendwhole-canonical-property.md)) entsprechen.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.
    
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

