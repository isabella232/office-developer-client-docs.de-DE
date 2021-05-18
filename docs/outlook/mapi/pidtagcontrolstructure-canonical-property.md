---
title: PidTagControlStructure (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlStructure
api_type:
- HeaderDef
ms.assetid: 02910389-b346-431c-a282-dedbc9f7dfc6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cf91620042f916d51f27be50d15f72db537ad5f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412947"
---
# <a name="pidtagcontrolstructure-canonical-property"></a>PidTagControlStructure (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Zeiger auf eine Struktur für ein Steuerelement, das in einem Dialogfeld verwendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTROL_STRUCTURE  <br/> |
|Kennung:  <br/> |0x3F01  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Anzeigetabelle  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft stellt einen langen Zeiger dar, der in eine der Steuerelementstrukturen umgleitt wird. Zu den Steuerelementstrukturen gehören:
  
|||
|:-----|:-----|
|[DTBLBUTTON](dtblbutton.md) <br/> |[DTBLCHECKBOX](dtblcheckbox.md) <br/> |
|[DTBLCOMBOBOX](dtblcombobox.md) <br/> |[DTBLDDLBX](dtblddlbx.md) <br/> |
|[DTBLEDIT](dtbledit.md) <br/> |[DTBLGROUPBOX](dtblgroupbox.md) <br/> |
|[DTBLLABEL](dtbllabel.md) <br/> |[DTBLLBX](dtbllbx.md) <br/> |
|[DTBLMVDDLBOX](dtblmvddlbox.md) <br/> |[DTBLMVLISTBOX](dtblmvlistbox.md) <br/> |
|[DTBLPAGE](dtblpage.md) <br/> |[DTBLRADIOBUTTON](dtblradiobutton.md) <br/> |
   
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

