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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 13e2ac93e7e3ba46bf25b26e76bd44c15f2b89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793624"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a>PidLidImageAttachmentsCompressionLevel (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Definiert eine Komprimierungsebene auf Bildanlagen angewendet.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidImgAttchmtsCompressLevel  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008593  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Laufzeit-Konfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Im folgenden sind die gültigen Komprimierung Ebenen:
  
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
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

