---
title: PidTagExpiryUnits (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c978fb3b23955d37c34c8f78f9a9a974245e0d8f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579082"
---
# <a name="pidtagexpiryunits-canonical-property"></a>PidTagExpiryUnits (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt die Zeiteinheit, in der sich die **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) -Eigenschaft multipliziert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EXPIRY_UNITS  <br/> |
|Kennung:  <br/> |0x3FEE  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft muss, falls festgelegt, einer der folgenden Werte sein:
  
|||
|:-----|:-----|
|PidTagExpiryUnits  <br/> |Beschreibung (TimeOf)  <br/> |
|0x00000000  <br/> |Minuten, z. B. 60 Sekunden  <br/> |
|0x00000001  <br/> |Stunden, z. B. 60 x 60 Sekunden  <br/> |
|0x00000002  <br/> |Tag, z. B. 24 x 60 x 60 Sekunden  <br/> |
|0x00000003  <br/> |Woche, z. B. 7x24x60x60 Sekunden  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
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

