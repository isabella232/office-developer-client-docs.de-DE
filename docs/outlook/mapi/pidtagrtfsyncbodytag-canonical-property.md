---
title: PidTagRtfSyncBodyTag (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24ef1d4e3e936426aea8216119e8ada9f6122e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331178"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a>PidTagRtfSyncBodyTag (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält wichtige Zeichen, die am Anfang des Nachrichtentexts angezeigt werden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W  <br/> |
|Kennung:  <br/> |0x1008  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Nachricht  <br/> |
   
## <a name="remarks"></a>Hinweise

Die [RTFSync-Funktion](rtfsync.md) verwendet das Texttag, um den Anfang des Nachrichtentexts anzugeben. Wenn der Text geändert wird, wird das Tag verwendet, um den Anfang des vorherigen Texts zu finden. 
  
Diese Eigenschaften sind Rich Text Format-Hilfseigenschaften. Sie werden von der **RTFSync-Funktion** verwendet und sind nicht für die direkte Verwendung durch Clientanwendungen vorgesehen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.
    
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

