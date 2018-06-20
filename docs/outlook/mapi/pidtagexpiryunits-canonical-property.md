---
title: Kanonische PidTagExpiryUnits-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1c753bb84ccbfe2fa6869d56806fd042a6d60e9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794348"
---
# <a name="pidtagexpiryunits-canonical-property"></a>Kanonische PidTagExpiryUnits-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Beschreibt die Zeiteinheit, wenn die Eigenschaft **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) multipliziert.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_EXPIRY_UNITS  <br/> |
|Bezeichner:  <br/> |0x3FEE  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-status  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft, wenn festgelegt ist, muss einer der folgenden Werte sein:
  
|||
|:-----|:-----|
|PidTagExpiryUnits  <br/> |Beschreibung (TimeOf)  <br/> |
|0x00000000  <br/> |Minuten, beispielsweise 60 Sekunden  <br/> |
|0x00000001  <br/> |Stunden, beispielsweise 60 x 60 Sekunden  <br/> |
|0x00000002  <br/> |Am Tag, beispielsweise 24 x 60 x 60 Sekunden  <br/> |
|0 x 00000003  <br/> |Woche, beispielsweise 7x24x60x60 Sekunden  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

