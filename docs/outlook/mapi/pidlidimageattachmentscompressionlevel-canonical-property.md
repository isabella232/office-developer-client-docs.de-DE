---
title: PidLidImageAttachmentsCompressionLevel (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8600cc7071fbe5c08d5df074f9bf59f4320b7f18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413829"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a>PidLidImageAttachmentsCompressionLevel (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Komprimierungsstufe, die auf Bildanlagen angewendet werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidImgAttchmtsCompressLevel  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x00008593  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Laufzeitkonfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Es folgen gültige Komprimierungsstufen:
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

