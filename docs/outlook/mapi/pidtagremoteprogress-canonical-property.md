---
title: PidTagRemoteProgress (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e1f57fd95ff38ef102cd74b0035dbb6b553259c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569351"
---
# <a name="pidtagremoteprogress-canonical-property"></a>PidTagRemoteProgress (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält eine Zahl, die den Status einer remote Übertragungstyp angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REMOTE_PROGRESS  <br/> |
|Kennung:  <br/> |0x3E0B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie keine Übertragung ausgeführt wird, sollten diese Eigenschaft auf 1 festgelegt. Wenn eine Übertragung ausgeführt wird, sollte es auf einen anderen Wert zwischen 0 und 100, der angibt, die Übertragung Prozent der Fertigstellung festgelegt werden.
  
Der numerische Statuscode zugeordnete Text wird in der Eigenschaft **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) angezeigt.
  
Die folgenden Kennzeichen können für diese Eigenschaft festgelegt werden:
  
MSGSTATUS_REMOTE_DELETE
  
> Übertragung der Nachricht wird gelöscht.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> Die Nachrichtenübermittlung wird gerade durchgeführt.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

