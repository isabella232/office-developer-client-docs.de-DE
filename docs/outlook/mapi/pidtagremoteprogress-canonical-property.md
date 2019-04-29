---
title: Kanonische Pidtagremoteprogress (-Eigenschaft
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
ms.openlocfilehash: a5a9d0796bc92514ae6d990b7328364b85bc55cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439842"
---
# <a name="pidtagremoteprogress-canonical-property"></a>Kanonische Pidtagremoteprogress (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Eigenschaft enthält eine Zahl, die den Status einer Remoteübertragung angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REMOTE_PROGRESS  <br/> |
|Kennung:  <br/> |0x3E0B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn keine Übertragung ausgeführt wird, sollte diese Eigenschaft auf 1 festgelegt werden. Wenn eine Übertragung ausgeführt wird, sollte Sie auf einen Wert zwischen 0 und 100 festgelegt werden, der den Prozentsatz der Fertigstellung des Transfers angibt.
  
Der mit dem numerischen Statuscode verknüpfte Text wird in der **PR_REMOTE_PROGRESS_TEXT** ([pidtagremoteprogresstext (](pidtagremoteprogresstext-canonical-property.md))-Eigenschaft angezeigt.
  
Für diese Eigenschaft können die folgenden Flags festgelegt werden:
  
MSGSTATUS_REMOTE_DELETE
  
> Die Nachrichtenübertragung wird gelöscht.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> Die Nachrichtenübertragung wird ausgeführt.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

