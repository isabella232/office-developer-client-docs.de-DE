---
title: PidTagScheduleInfoFreeBusyTentative (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385116"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>PidTagScheduleInfoFreeBusyTentative (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Blöcke von Zeiten für die der Frei/Gebucht-Status mit Vorbehalt ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|Kennung:  <br/> |0x6852  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Frei/Gebucht-Informationen  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft hat viele Werte als die Anzahl von Werten in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)). Jede Binärwert stellt einen Monat und entspricht dem Wert der selben Index **PR_SCHDINFO_MONTHS_TENTATIVE**. Die binäre Werte werden in der gleichen Reihenfolge wie die Werte in **PR_SCHDINFO_MONTHS_TENTATIVE**sortiert.
  
Jede Binärwert hat mindestens 4-BYTE-Blöcken und einzelnen Elementen durch die Start- und Endzeit in der zweiten zwei Bytes in little-Endian-Format in den ersten beiden Bytes enthält. Die Anfangszeit ist die Anzahl der Minuten zwischen Mitternacht koordinierte Weltzeit (UTC), der den ersten Tag des Monats und die Startzeit des Ereignisses in UTC. Die Endzeit ist die Anzahl der Minuten zwischen den ersten Tag des Monats Mitternacht UTC und Zeit für das Ende des Ereignisses in UTC. Die 4-BYTE-Blöcken werden in aufsteigender Reihenfolge sortiert.
  
Ein Block mit Startzeit als die Anfangszeit des ersten Blocks und Endzeit als Zeit für das Ende des letzten Blocks werden aufeinander folgende oder überlappende Blöcke Zeitraum zusammengeführt. Wenn ein Ereignis über mehrere Monate oder Jahre verteilt ist, wird das Ereignis in mehrere Blöcke, eine pro Monat geteilt. Wenn keine mit Vorbehalt Ereignisse in der Veröffentlichung Bereich vorhanden sind, hat diese Eigenschaft und die **PR_SCHDINFO_MONTHS_TENTATIVE** muss nicht festgelegt werden oder gelöscht werden müssen, wenn sie bereits vorhanden. Andernfalls muss diese Eigenschaft festgelegt werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
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

