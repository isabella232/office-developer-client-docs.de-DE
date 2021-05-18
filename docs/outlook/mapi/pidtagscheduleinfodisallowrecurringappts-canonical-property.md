---
title: PidTagScheduleInfoDisallowRecurringAppts (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowRecurringAppts
api_type:
- COM
ms.assetid: 61e082dd-f5bc-479b-990a-c9c0360f883e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 678fd982505cc2bc910af9ef131f852a7f0c919a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330100"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a>PidTagScheduleInfoDisallowRecurringAppts (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn die automatische Antwort auf Terminserien ablehnend ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_DISALLOW_RECURRING_APPTS  <br/> |
|Kennung:  <br/> |0x686E  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Frei/Gebucht  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nur dann sinnvoll, wenn der Wert **der PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) -Eigenschaft TRUE ist. Das Fehlen dieser Eigenschaft gibt an, dass besprechungsserien akzeptiert werden müssen. Dies ist keine erforderliche Eigenschaft.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

