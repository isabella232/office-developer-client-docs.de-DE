---
title: PidTagScheduleInfoMonthsTentative (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b58413809a562b6a2b1310e573e531ae7320c0e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599431"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>PidTagScheduleInfoMonthsTentative (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Monate, die in der Frei/Gebucht-Nachricht mit Vorbehalt gekennzeichnet sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Kennung:  <br/> |0x6851  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Frei/Gebucht  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Anzahl der Werte in dieser Eigenschaft muss zwischen Null und der Anzahl der Monate liegen, die vom Veröffentlichungsbereich abgedeckt werden. Dabei handelt es sich um den Zeitraum zwischen den Eigenschaften **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) und **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).
  
Jeder Wert in dieser Eigenschaft enthält einen monat- und jahrescodierten Wert. Dies wird mithilfe des Ausdrucks "Jahr × 16 + Monat" berechnet, wobei Jahr und Monat auf dem gregorianischen Kalender basieren. Die Werte werden in aufsteigender Reihenfolge sortiert und im Little-Endian-Format codiert. Wenn ein Ereignis über mehrere Monate oder mehrere Jahre verteilt ist, muss für jeden Monat, der in den Veröffentlichungsbereich fällt, ein Wert vorhanden sein. Wenn im Veröffentlichungsbereich keine Ereignisse mit Vorbehalt vorhanden sind, dürfen diese Eigenschaft und **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) nicht festgelegt oder gelöscht werden, wenn sie bereits vorhanden sind. Andernfalls muss diese Eigenschaft festgelegt werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

