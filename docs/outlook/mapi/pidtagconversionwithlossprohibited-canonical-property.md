---
title: Kanonische PidTagConversionWithLossProhibited-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: eee70d97c35c7f115e424905b9e36f3dfa392c02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794277"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>Kanonische PidTagConversionWithLossProhibited-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält True, wenn ein Message Transfer Agent (MTA) verboten wird tätigen Nachricht Text Konvertierungen, die Informationen verloren gehen. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|Bezeichner:  <br/> |0x000d  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Allgemeine Konfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Beispiel für die Art der Konvertierung wird nicht zulässig ist die "Verlust" Zuordnung von Unicode (zwei Bytes pro Zeichen) in einer Einzel-Byte-Zeichensatz. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

