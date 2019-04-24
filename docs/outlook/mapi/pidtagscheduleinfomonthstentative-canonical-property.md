---
title: Kanonische Pidtagscheduleinfomonthstentative (-Eigenschaft
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
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359759"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>Kanonische Pidtagscheduleinfomonthstentative (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Monate mit Vorbehalt in der Frei/Gebucht-Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Kennung:  <br/> |0x6851  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Frei/Gebucht  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Anzahl der Werte in dieser Eigenschaft muss zwischen null und der Anzahl der Monate liegen, die vom Veröffentlichungszeitraum abgedeckt werden, also die Periode zwischen **PR_FREEBUSY_PUBLISH_START** ([Pidtagfreebusypublishstart (](pidtagfreebusypublishstart-canonical-property.md)) und **PR_FREEBUSY_PUBLISH_END **([Pidtagfreebusypublishend (](pidtagfreebusypublishend-canonical-property.md))-Eigenschaften.
  
Jeder Wert dieser Eigenschaft enthält einen Monat und ein Jahr. Dieser Wert wird mithilfe des Ausdrucks "Year × 16 + Month" berechnet, wobei Year und Month auf dem gregorianischen Kalender basieren. Die Werte werden in aufsteigender Reihenfolge sortiert und im Little-Endian-Format codiert. Wenn ein Ereignis über mehrere Monate oder mehrere Jahre verteilt ist, muss für jeden der Monate, die in den Veröffentlichungszeitraum fallen, ein Wert vorhanden sein. Wenn im Veröffentlichungszeitraum keine zaghaften Ereignisse vorhanden sind, dürfen diese Eigenschaft und **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([pidtagscheduleinfofreebusytentative (](pidtagscheduleinfofreebusytentative-canonical-property.md)) nicht festgelegt oder gelöscht werden, wenn Sie bereits vorhanden sind. Andernfalls muss diese Eigenschaft festgelegt werden.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

