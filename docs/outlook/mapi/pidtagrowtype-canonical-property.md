---
title: PidTagRowType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359514"
---
# <a name="pidtagrowtype-canonical-property"></a>PidTagRowType (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der den Typ einer Zeile in einer Tabelle angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ROW_TYPE  <br/> |
|Kennung:  <br/> |0x0FF5  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI nicht durchlässig  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur in Inhaltstabellen angezeigt. Eine Kategorie ist nur vorhanden, wenn sie Elemente enthält.
  
Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
TBL_LEAF_ROW 
  
> Stellt tatsächliche Daten statt einer Kategoriezeile dar.
    
TBL_EMPTY_CATEGORY 
  
> Derzeit nicht verwendet.
    
TBL_EXPANDED_CATEGORY 
  
> Die Kategorie wird erweitert. Auf der Benutzeroberfläche wird dies in der Regel mit dem Minuszeichen ( - ) daneben angezeigt.
    
TBL_COLLAPSED_CATEGORY 
  
> Die Kategorie ist reduziert. Auf der Benutzeroberfläche wird dies in der Regel mit dem Pluszeichen (+) daneben angezeigt.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Enthält zulässige Vorgänge für die Zentralen Tabellenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagRowid (kanonische Eigenschaft)](pidtagrowid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

