---
title: PidTagAttachContentId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachContentId
api_type:
- HeaderDef
ms.assetid: 46f31089-3b66-41a2-8094-e3db52464b9f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 049eaab7c1ec8289a9b553ecdc8000a08cbde942
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575085"
---
# <a name="pidtagattachcontentid-canonical-property"></a>PidTagAttachContentId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Inhaltsidentifikationsheader einer MIME-Nachrichtenanlage (Multipurpose Internet Mail Extensions). 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W  <br/> |
|Kennung:  <br/> |0x3712  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften werden für die MHTML-Unterstützung verwendet. Sie stellen den Inhaltsidentifikationsheader für den entsprechenden MIME-Textkörper dar. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
## <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

