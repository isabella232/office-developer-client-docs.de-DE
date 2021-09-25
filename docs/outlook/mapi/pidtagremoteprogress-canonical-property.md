---
title: PidTagRemoteProgress (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 033c1f5ce189033dab2a749ccefb5229c8db9379
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594979"
---
# <a name="pidtagremoteprogress-canonical-property"></a>PidTagRemoteProgress (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält eine Zahl, die den Status einer Remoteübertragung angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REMOTE_PROGRESS  <br/> |
|Kennung:  <br/> |0x3E0B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn keine Übertragung ausgeführt wird, sollte diese Eigenschaft auf 1 festgelegt werden. Wenn eine Übertragung ausgeführt wird, sollte sie auf einen Wert zwischen 0 und 100 festgelegt werden, der den Prozentsatz des Abschlusses der Übertragung angibt.
  
Der dem numerischen Statuscode zugeordnete Text wird in der **eigenschaft PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) angezeigt.
  
Für diese Eigenschaft können die folgenden Flags festgelegt werden:
  
MSGSTATUS_REMOTE_DELETE
  
> Die Nachrichtenübertragung wird gelöscht.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> Die Nachrichtenübertragung wird gerade ausgeführt.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

