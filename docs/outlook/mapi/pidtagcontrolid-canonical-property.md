---
title: PidTagControlId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416020"
---
# <a name="pidtagcontrolid-canonical-property"></a>PidTagControlId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen eindeutigen Bezeichner für ein Steuerelement, das in einem Dialogfeld verwendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTROL_ID  <br/> |
|Kennung:  <br/> |0x3F07  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Anzeigetabelle  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft enthält einen eindeutigen Bezeichner für das Steuerelement. Dieser Bezeichner sollte eine [GUID-Struktur](guid.md) und einen binären Wert vom Typ **LONG enthalten.** Alle Steuerelemente im Dialogfeld sollten dieselbe **GUID** verwenden, um den Dienstanbieter zu identifizieren, und jedes Steuerelement sollte einen eindeutigen **LONG-Wert** verwenden, um sicherzustellen, dass die Steuerelemente nicht kollidieren. 
  
Diese Eigenschaft wird in Benachrichtigungen verwendet. Beispielsweise müssen in der Anzeigetabelle gesendete Benachrichtigungen diese Eigenschaft so festlegen, dass das zu aktualisierende Steuerelement eindeutig identifiziert wird. 
  
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

