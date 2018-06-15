---
title: Kanonische PidTagControlId-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 799f83b397cbef9d7dcb6c9a88154b88afe35675
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19794255"
---
# <a name="pidtagcontrolid-canonical-property"></a>Kanonische PidTagControlId-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einen eindeutigen Bezeichner für ein Steuerelement in einem Dialogfeld verwendet. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_CONTROL_ID  <br/> |
|Bezeichner:  <br/> |0x3F07  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Zeigt die MAPI-Tabelle  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält einen eindeutigen Bezeichner für das Steuerelement. Dieser Bezeichner sollte eine [GUID](guid.md) -Struktur und den Wert vom Typ **LONG**binary enthalten. Alle Steuerelemente im Dialogfeld sollte dieselbe **GUID** zum Identifizieren des Dienstanbieters verwenden, und jedes Steuerelement sollte eine eindeutige verwenden **LONG** -Wert, um sicherzustellen, dass die Steuerelemente nicht kollidieren. 
  
Diese Eigenschaft wird in Benachrichtigungen verwendet. Senden von Benachrichtigungen für die Anzeige-Tabelle müssen beispielsweise zur eindeutigen Identifizierung des Steuerelements so aktualisieren Sie diese Eigenschaft festgelegt. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

