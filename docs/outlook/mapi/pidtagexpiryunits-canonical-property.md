---
title: PidTagExpiryUnits (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316408"
---
# <a name="pidtagexpiryunits-canonical-property"></a>PidTagExpiryUnits (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt die Zeiteinheit, in der **die PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) -Eigenschaft multipliziert wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EXPIRY_UNITS  <br/> |
|Kennung:  <br/> |0x3FEE  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Hinweise

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
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

