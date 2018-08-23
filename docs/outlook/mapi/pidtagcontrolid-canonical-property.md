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
ms.openlocfilehash: 2868533e0383309e013bb82aaa4300a0a40e335a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577513"
---
# <a name="pidtagcontrolid-canonical-property"></a>PidTagControlId (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält einen eindeutigen Bezeichner für ein Steuerelement in einem Dialogfeld verwendet. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTROL_ID  <br/> |
|Kennung:  <br/> |0x3F07  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Zeigt die MAPI-Tabelle  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

