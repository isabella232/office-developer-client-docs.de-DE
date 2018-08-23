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
ms.openlocfilehash: 6e856cc8dc131c1b6266181a954a8da9cfb1d1ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566103"
---
# <a name="pidtagrowtype-canonical-property"></a>PidTagRowType (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der den Typ einer Zeile in einer Tabelle angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ROW_TYPE  <br/> |
|Kennung:  <br/> |0x0FF5  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI Übertragungseinehit  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird nur für Tabellen Inhalt angezeigt. Eine Kategorie ist nur vorhanden, wenn er Elemente verfügt.
  
Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:
  
TBL_LEAF_ROW 
  
> Tatsächliche Daten darstellt, anstatt eine Kategoriezeile.
    
TBL_EMPTY_CATEGORY 
  
> Derzeit nicht verwendet.
    
TBL_EXPANDED_CATEGORY 
  
> Die Kategorie erweitert ist. die Benutzeroberfläche wird in der Regel dies mit dem Minuszeichen (-) neben dem angezeigt.
    
TBL_COLLAPSED_CATEGORY 
  
> Die Kategorie ausgeblendet ist; die Benutzeroberfläche wird dies in der Regel durch das Pluszeichen (+) neben dem.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Zulässige Vorgänge für die Hauptobjekte-Tabelle enthält.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagRowid (kanonische Eigenschaft)](pidtagrowid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

