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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359774"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>PidTagScheduleInfoFreeBusyTentative (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Zeitblöcke, für die der Frei/Gebucht-Status zaglos ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|Kennung:  <br/> |0x6852  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Frei/Gebucht  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft hat so viele Werte wie die Anzahl der Werte in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)). Jeder binäre Wert stellt einen Monat dar und entspricht dem Wert am gleichen Index in **PR_SCHDINFO_MONTHS_TENTATIVE**. Die binären Werte werden in der gleichen Reihenfolge wie die Werte in **PR_SCHDINFO_MONTHS_TENTATIVE.**
  
Jeder binäre Wert verfügt über einen oder mehrere 4-BYTE-Blöcke, und jeder von ihnen enthält die Startzeit in den ersten beiden Bytes und die Endzeit in den zweiten beiden Bytes im Little-Endian-Format. Die Startzeit ist die Anzahl der Minuten zwischen Mitternacht koordinierter Weltzeit (UTC) des ersten Tages des Monats und der Startzeit des Ereignisses in UTC. Die Endzeit ist die Anzahl der Minuten zwischen Mitternacht UTC des ersten Tages des Monats und der Endzeit des Ereignisses in UTC. Die 4-BYTE-Blöcke werden in aufsteigender Reihenfolge sortiert.
  
Aufeinander folgende oder überlappende Zeitblöcke werden mit der Startzeit als Startzeit des ersten Blocks und endzeit als Endzeit des letzten Blocks in einem Block zusammengeführt. Wenn ein Ereignis über mehrere Monate oder Jahre verteilt ist, wird das Ereignis in mehrere Blöcke aufgeteilt, einen für jeden Monat. Wenn im Veröffentlichungsbereich keine zagvollen Ereignisse vorhanden sind, dürfen diese Eigenschaft **und** PR_SCHDINFO_MONTHS_TENTATIVE nicht festgelegt oder gelöscht werden, wenn sie bereits vorhanden sind. Andernfalls muss diese Eigenschaft festgelegt werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
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

