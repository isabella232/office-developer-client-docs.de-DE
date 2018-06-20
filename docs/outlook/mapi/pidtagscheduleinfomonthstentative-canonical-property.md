---
title: Kanonische PidTagScheduleInfoMonthsTentative-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 20620a5835e627eb7543a03037f9be75db6739ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795100"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>Kanonische PidTagScheduleInfoMonthsTentative-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die Monate in der Nachricht Frei/Gebucht-Informationen mit Vorbehalt markiert.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Bezeichner:  <br/> |0x6851  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Frei/Gebucht-Informationen  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Anzahl von Werten in dieser Eigenschaft muss zwischen 0 (null) und die Anzahl der Monate nach der Veröffentlichung der Zeitraum zwischen dem **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) und **PR_FREEBUSY_PUBLISH_END ist Bereich abgedeckt **([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md))-Eigenschaften.
  
Jeder Wert in dieser Eigenschaft hat einen Monat und Jahr, die in dem er codiert. Dies wird mithilfe des Ausdrucks "Jahr × 16 + Monat", in dem Jahr und Monat der gregorianische Kalender basieren auf berechnet. Die Werte in aufsteigender Reihenfolge sortiert sind und in little-Endian-Format codiert werden. Wenn ein Ereignis über mehrere Monate oder Jahre mehrere verteilt ist, muss ein Wert für die Monate, die in der Veröffentlichung Bereich fallen vorhanden sein. Wenn keine mit Vorbehalt Ereignisse in der Veröffentlichung Bereich vorhanden sind, hat diese Eigenschaft und die **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) muss nicht festgelegt werden oder gelöscht werden müssen, wenn sie bereits vorhanden. Andernfalls muss diese Eigenschaft festgelegt werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

