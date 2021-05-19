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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e0a8f49f96bf4c4f8518dddbe52e8692f7b6645a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339872"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a>PidTagAttachAdditionalInformation (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Dateitypinformationen für eine Nicht-Windows-Anlage zur Verfügung.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_ADDITIONAL_INFO  <br/> |
|Kennung:  <br/> |0x370F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft stellt Metadaten zu einer bestimmten Anlage basierend auf der Codierung der Anlage bereit. Wenn beispielsweise die **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))-Eigenschaft MacBinary enthält, enthält **PR_ATTACH_ADDITIONAL_INFO** eine Zeichenfolge, die den #A0 und -Dateityp darstellt, formatiert als ":CREA:TYPE" für die codierte Macintosh-Datei. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
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

