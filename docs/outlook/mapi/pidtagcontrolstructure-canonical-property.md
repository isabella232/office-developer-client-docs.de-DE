---
title: Kanonische PidTagControlStructure-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagControlStructure
api_type:
- HeaderDef
ms.assetid: 02910389-b346-431c-a282-dedbc9f7dfc6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c5317bd7b7c423b69333f1ee35a5086c0d7b3646
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563728"
---
# <a name="pidtagcontrolstructure-canonical-property"></a>Kanonische PidTagControlStructure-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Zeiger auf eine Struktur für ein Steuerelement, das in einem Dialogfeld verwendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTROL_STRUCTURE  <br/> |
|Kennung:  <br/> |0x3F01  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Anzeigetabelle  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft stellt einen langen Zeiger dar, der in eine der Steuerelementstrukturen umgewandelt wird. Zu den Steuerelementstrukturen gehören:
  
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
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

