---
title: Kanonische Pidtagscheduleinfofreebusymerged (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyMerged
api_type:
- COM
ms.assetid: 3ebfccb6-967a-4f8e-9d94-94c50ba65438
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8d15c6cb256fb1e80e3c94bdfe7e71bd8625aa35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338717"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a>Kanonische Pidtagscheduleinfofreebusymerged (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Zeiten, für die der Frei/Gebucht-Status auf beschäftigt oder OOF festgelegt ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_FREEBUSY_MERGED  <br/> |
|Kennung:  <br/> |0x6850  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Frei/Gebucht  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ereignisse mit dem Typ "frei/gebucht" sind in dieser Eigenschaft nicht enthalten. Das Format, die Berechnung und die Einschränkungen dieser Eigenschaft sind identisch mit denen von **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([pidtagscheduleinfofreebusytentative (](pidtagscheduleinfofreebusytentative-canonical-property.md)), beziehen sich jedoch auf Termine, die als OOF oder busy im zugeordneten Kalender gekennzeichnet sind.
  
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

