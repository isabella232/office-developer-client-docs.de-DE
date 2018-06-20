---
title: Kanonische PidTagRulesTable-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 945dabec4ee34d38d2474c918e779d894f4a917c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795050"
---
# <a name="pidtagrulestable-canonical-property"></a>Kanonische PidTagRulesTable-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Tabelle mit allen Regeln in einen Ordner angewendet.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RULES_TABLE  <br/> |
|Bezeichner:  <br/> |0x3FE1  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Serverseitige Regeln  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist auf alle Ordnerobjekte auf einem Exchange-Server, denen Regeln vorhanden. Werte enthalten, die in dieser Eigenschaft werden beim Lesen und Ändern der Regeln verwendet. Sie können die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode mit der **IID_IExchangeModifyTable** Interface Identifier verwenden, erhalten eine [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) -Schnittstelle für die Regeltabelle für einen Ordner. Sie können diese Schnittstelle zum Lesen und ändern diese Regeln verwenden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet. 
    
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

