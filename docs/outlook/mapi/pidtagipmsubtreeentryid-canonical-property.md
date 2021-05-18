---
title: PidTagIpmSubtreeEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 815685696dfc93bb6241f608ca0157e87e758e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412730"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a>PidTagIpmSubtreeEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID des Stammverzeichnisses der Ordnerunterstruktur für zwischenpersonale Nachrichten (IPM) in der Ordnerstruktur des Nachrichtenspeichers. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IPM_SUBTREE_ENTRYID  <br/> |
|Kennung:  <br/> |0x35E0  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Ordner  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft stellt den Stamm der IPM-Hierarchie dar. IPM-Clients sollten keine Ordner anzeigen, die keine Unterordner des Ordners sind, der durch diese Eigenschaft dargestellt wird.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

