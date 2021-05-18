---
title: PidTagMiniIcon (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405415"
---
# <a name="pidtagminiicon-canonical-property"></a>PidTagMiniIcon (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmap eines Halbformatsymbols für ein Formular.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MINI_ICON  <br/> |
|Kennung:  <br/> |0x0FFC  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft enthält ein 32-× 32-Pixel-Bild eines Symbols, das mit dem Inhalt eines identisch ist. ICO-Datei, aber nur die obere linke 16 × 16 Pixel werden als signifikant betrachtet. Diese Eigenschaft wird normalerweise aus der kopiert. ICO-Datei, die in der SmallIcon-Zeile des entsprechenden Abschnitts [Beschreibung] der Formularkonfigurationsdatei angegeben ist.
  
 **Hinweis** Einige Plattformen unterstützen keine Symbole mit 16 × 16 Pixeln. Das 32-× 32-Format dieser Eigenschaft ist in einem solchen Fall verwendbar, clientanwendungen sollten jedoch Anzeigeinkonsistenzen beachten. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagIcon (kanonische Eigenschaft)](pidtagicon-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

