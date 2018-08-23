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
ms.openlocfilehash: 5514e0553f719e2e875aad7001bb38a6a52e8e08
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589777"
---
# <a name="pidtagminiicon-canonical-property"></a>PidTagMiniIcon (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine Bitmap eines Symbols halber Größe für ein Formular enthält.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MINI_ICON  <br/> |
|Kennung:  <br/> |0x0FFC  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft enthält ein Bild mit 32 x 32 Pixeln eines Symbols, identisch mit den Inhalt ein. Gelten erhebliche ICO-Datei, aber nur der oberen linken Ecke 16 x 16 Pixel. Diese Eigenschaft wird normalerweise übernommen aus der. ICO-Datei in der SmallIcon-Zeile der entsprechenden Abschnitt der Konfigurationsdatei Formular [Beschreibung] angegeben.
  
 **Hinweis** Einige Plattformen werden nicht unterstützt 16 x 16 Pixel-Symbol. Das Format 32 x 32 dieser Eigenschaft kann in einem solchen Fall verwendet werden, aber Clientanwendungen Beachten der Anzeige Inkonsistenzen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagIcon (kanonische Eigenschaft)](pidtagicon-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

