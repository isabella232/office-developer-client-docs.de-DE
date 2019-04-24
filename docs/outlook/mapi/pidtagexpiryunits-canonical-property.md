---
title: Kanonische Pidtagexpiryunits (-Eigenschaft
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
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316408"
---
# <a name="pidtagexpiryunits-canonical-property"></a>Kanonische Pidtagexpiryunits (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt die Zeiteinheit, in der die **PR_EXPIRY_NUMBER** ([pidtagexpirynumber (](pidtagexpirynumber-canonical-property.md))-Eigenschaft multipliziert wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EXPIRY_UNITS  <br/> |
|Kennung:  <br/> |0x3FEE  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Bei dieser Eigenschaft muss es sich um einen der folgenden Werte handeln:
  
|||
|:-----|:-----|
|Pidtagexpiryunits (  <br/> |Beschreibung (TimeOf)  <br/> |
|0x00000000  <br/> |Minuten, zum Beispiel 60 Sekunden  <br/> |
|0x00000001  <br/> |Stunden, beispielsweise 60x60 Sekunden  <br/> |
|0x00000002  <br/> |Tag, beispielsweise 24x60x60 Sekunden  <br/> |
|0x00000003  <br/> |Woche, beispielsweise 7x24x60x60 Sekunden  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

