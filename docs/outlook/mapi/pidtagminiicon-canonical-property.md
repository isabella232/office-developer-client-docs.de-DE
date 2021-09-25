---
title: PidTagMiniIcon (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96d477576f0d5fc8f94ec9e8d7e3f2fd3879aad1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595196"
---
# <a name="pidtagminiicon-canonical-property"></a>PidTagMiniIcon (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmap mit einem Symbol in halber Größe für ein Formular.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MINI_ICON  <br/> |
|Kennung:  <br/> |0x0FFC  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft enthält ein Bild mit 32 × 32 Pixeln eines Symbols, das dem Inhalt eines Symbols entspricht. ICO-Datei, aber nur die obere linke 16 × 16 Pixel werden als signifikant betrachtet. Diese Eigenschaft wird normalerweise aus der kopiert. ICO-Datei, die in der SmallIcon-Zeile des entsprechenden [Description]-Abschnitts der Formularkonfigurationsdatei angegeben ist.
  
 **Hinweis** Einige Plattformen unterstützen keine Symbole mit 16 × 16 Pixeln. Das Format 32 × 32 dieser Eigenschaft kann in einem solchen Fall verwendet werden, aber Clientanwendungen sollten Anzeigeinkonsistenzen beachten. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagIcon-Eigenschaft](pidtagicon-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

