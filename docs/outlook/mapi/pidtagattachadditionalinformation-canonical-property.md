---
title: PidTagAttachAdditionalInformation (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 83de3a4ad7c93b2dfee8063ab63bfbf0724a5f61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794077"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a>PidTagAttachAdditionalInformation (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Dateitypinformationen für eine nicht-Windows-Anlage enthält.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ATTACH_ADDITIONAL_INFO  <br/> |
|Bezeichner:  <br/> |0x370F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |E-Mail-Anlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft stellt die Metadaten für eine bestimmte Anlage basierend auf der Anlage-Codierung. Wenn die Eigenschaft **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) MacBinary enthält, enthält **PR_ATTACH_ADDITIONAL_INFO** beispielsweise eine Zeichenfolge, die der Ersteller der Macintosh-Datei und der Dateityp, formatiert als ":CREA:TYPE" darstellt für die codierte Macintosh-Datei. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
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

