---
title: Kanonische PidTagRowType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6722d02f549979381e20a5179b573c027773e72b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599558"
---
# <a name="pidtagrowtype-canonical-property"></a>Kanonische PidTagRowType-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der den Typ einer Zeile in einer Tabelle angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ROW_TYPE  <br/> |
|Kennung:  <br/> |0x0FF5  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI nicht datenübertragungsfähig  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird nur in Inhaltstabellen angezeigt. Eine Kategorie ist nur vorhanden, wenn sie Elemente enthält.
  
Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
TBL_LEAF_ROW 
  
> Stellt tatsächliche Daten anstelle einer Kategoriezeile dar.
    
TBL_EMPTY_CATEGORY 
  
> Derzeit nicht verwendet.
    
TBL_EXPANDED_CATEGORY 
  
> Die Kategorie wird erweitert. Die Benutzeroberfläche zeigt dies in der Regel mit dem Minuszeichen ( - ) daneben an.
    
TBL_COLLAPSED_CATEGORY 
  
> Die Kategorie ist reduziert. Die Benutzeroberfläche zeigt dies in der Regel mit dem Pluszeichen (+) daneben an.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Enthält zulässige Vorgänge für die zentralen Tabellenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagRowid-Eigenschaft](pidtagrowid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

