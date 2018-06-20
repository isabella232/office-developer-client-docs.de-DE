---
title: Kanonische PidTagStatusString-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ea24b5e721317668c8f43278a5e4c38d73b3e91c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795200"
---
# <a name="pidtagstatusstring-canonical-property"></a>Kanonische PidTagStatusString-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Meldung, die den aktuellen Status einer Sitzung Ressource angibt. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Bezeichner:  <br/> |0x3E08  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-status  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften geben Dienstanbieter und MAPI-die Möglichkeit, bestimmte Informationen über den Status einer Sitzung Ressource, wie die integrierte Adressbuch oder einem bestimmten Dienstanbieter anzugeben. Diese Eigenschaft erläutert und liefert zusätzliche Informationen über einen Statuscode oder die Eigenschaft **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)). **PR_STATUS_CODE** für alle Status erforderlich ist, sind die **PR_STATUS_STRING** und die zugehörigen Eigenschaften optional. Wenn der Adressbuchhierarchie kein Wert angegeben, stellt die MAPI-Warteschlange einen Standardwert bereit. 
  
Die Zeichenfolge wird auf derselben Seite die remote Procedure call, als die MAPI-Warteschlange generiert. Übertragung über gemeinsam genutzten Speicher, statt über eine Prozessgrenze gemarshallt werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagStatusCode-Eigenschaft](pidtagstatuscode-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

