---
title: Kanonische PidTagRecipientReassignmentProhibited-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0176485ca9b84260176e3be8ec9c8f42cf755cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794914"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>Kanonische PidTagRecipientReassignmentProhibited-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt an, ob weitere Empfänger hinzufügen, wenn die Nachricht weitergeleitet für die e-Mail-Nachricht nicht zulässig ist.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Bezeichner:  <br/> |0x002B  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird basierend auf der e-Mail-Nachricht **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) Wert festgelegt. **PR_SENSITIVITY** festgelegt ist "0 x 00000000" (normal) oder "0 x 00000003" (vertraulich), diese Eigenschaft auf "0 x 00" oder nicht vorhanden ist, was bedeutet, dass das Hinzufügen festgelegt werden muss zusätzliche oder andere Empfänger der e-Mail-Nachricht zulässig ist. Wenn die e-Mail-Objekts **PR_SENSITIVITY** auf "0 x 00000001" (personal) oder "0 x 00000002" (privat) festgelegt ist, diese Eigenschaft muss festgelegt werden "0 x 01" zum Hinzufügen von zusätzlicher oder anderen Empfängern dieser e-Mail über Weiterleitung zu verhindern. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

