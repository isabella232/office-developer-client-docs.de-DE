---
title: Kanonische PidTagControlId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 163a7e88bdb6f6c22a608af2b5a0af961f033779
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583507"
---
# <a name="pidtagcontrolid-canonical-property"></a>Kanonische PidTagControlId-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen eindeutigen Bezeichner für ein Steuerelement, das in einem Dialogfeld verwendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTROL_ID  <br/> |
|Kennung:  <br/> |0x3F07  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Anzeigetabelle  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft enthält einen eindeutigen Bezeichner für das Steuerelement. Dieser Bezeichner sollte eine [GUID-Struktur](guid.md) und einen binären Wert vom Typ **LONG** enthalten. Alle Steuerelemente im Dialogfeld sollten die gleiche **GUID** verwenden, um den Dienstanbieter zu identifizieren, und jedes Steuerelement sollte einen eindeutigen **LONG-Wert** verwenden, um sicherzustellen, dass die Steuerelemente nicht kollidieren. 
  
Diese Eigenschaft wird in Benachrichtigungen verwendet. Beispielsweise müssen Benachrichtigungen, die an die Anzeigetabelle gesendet werden, diese Eigenschaft festlegen, um das zu aktualisierende Steuerelement eindeutig zu identifizieren. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

