---
title: Kanonische Pidtagminiicon (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356231"
---
# <a name="pidtagminiicon-canonical-property"></a>Kanonische Pidtagminiicon (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmap mit einem halben Symbol für ein Formular.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MINI_ICON  <br/> |
|Kennung:  <br/> |0x0FFC  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält ein 32 × 32-Pixel Bild eines Symbols, dasselbe wie der Inhalt von a. ICO-Datei, aber nur die oberen linken 16 × 16 Pixel gelten als signifikant. Diese Eigenschaft wird normalerweise aus der kopiert. ICO-Datei, die in der SmallIcon-Codezeile im entsprechenden Abschnitt [Description] der Formular Konfigurationsdatei angegeben ist.
  
 **Hinweis** Einige Plattformen unterstützen keine 16 × 16-Pixel-Symbole. Das 32 × 32-Format dieser Eigenschaft kann in einem solchen Fall verwendet werden, die Anzeige Inkonsistenzen sollten jedoch von Clientanwendungen beachtet werden. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagicon (-Eigenschaft](pidtagicon-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

