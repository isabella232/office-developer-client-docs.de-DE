---
title: PidTagParentDisplay (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ce9fea80a2dfed25002e5500dd4defaf5ff04421
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794784"
---
# <a name="pidtagparentdisplay-canonical-property"></a>PidTagParentDisplay (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält den Anzeigenamen des Ordners, in dem eine Nachricht während eines Suchvorgangs gefunden wurde.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W  <br/> |
|Bezeichner:  <br/> |0x0E05  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI Übertragungseinehit  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften ist nicht für jedes Objekt. Sie können nur in der Inhaltstabelle eines Ordners Suchergebnisse angezeigt werden.
  
Diese Eigenschaften und **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) Eigenschaften sind nicht miteinander verknüpft. Zielgerichtet auf völlig andere Kontexte.
  
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

