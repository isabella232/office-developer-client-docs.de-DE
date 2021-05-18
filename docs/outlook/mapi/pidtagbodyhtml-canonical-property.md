---
title: PidTagBodyHtml (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6ed59228ee06a1d3e362115a99bf4b859dfeb698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359045"
---
# <a name="pidtagbodyhtml-canonical-property"></a>PidTagBodyHtml (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Hypertext Markup Language (HTML)-Version des Nachrichtentexts. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W  <br/> |
|Kennung:  <br/> |0x1013  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften enthalten denselben Nachrichtentext wie PR_BODY_CONTENT_LOCATION **(** [PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), aber in HTML. 
  
Ein Nachrichtenspeicher, der HTML unterstützt, gibt dies **an,** indem STORE_HTML_OK in der PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) festlegen. 
  
 **Hinweis** **STORE_HTML_OK** ist nicht in Versionen von Mapidefs.h definiert, die in Microsoft® Exchange 2000 Server und früheren Versionen enthalten sind. Wenn **STORE_HTML_OK** nicht definiert ist, verwenden Sie stattdessen den Wert 0x00010000. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
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

