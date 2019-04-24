---
title: Kanonische Pidlidimageattachmentscompressionlevel (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8600cc7071fbe5c08d5df074f9bf59f4320b7f18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357582"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a>Kanonische Pidlidimageattachmentscompressionlevel (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Komprimierungsstufe für Bildanlagen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidImgAttchmtsCompressLevel  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long-ID (Deckel):  <br/> |0x00008593  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Laufzeitkonfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Es folgen die folgenden gültigen Komprimierungsstufen:
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

