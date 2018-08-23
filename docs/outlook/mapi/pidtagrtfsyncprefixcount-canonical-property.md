---
title: PidTagRtfSyncPrefixCount (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncPrefixCount
api_type:
- COM
ms.assetid: c2b15ac5-9e89-4ee2-812d-102d0b2ac56e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 32344d81d929b0f78a5f883cd9860d838ba25bb8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568441"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a>PidTagRtfSyncPrefixCount (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine Anzahl von Zeichen, die vor der signifikanten Zeichen der Nachricht angezeigt werden ignoriert.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RTF_SYNC_PREFIX_COUNT  <br/> |
|Kennung:  <br/> |0x1010  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Nachricht  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Anzahl der Anfangszeichen enthält keine Leerzeichen.
  
Diese Eigenschaft ist eine zusätzliche Rich Text Format (RTF)-Eigenschaft. RTF-Hilfs-Eigenschaften werden von der Funktion [RTFSync](rtfsync.md) verwendet und nicht direkt von Clientanwendungen verwendet werden sollen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.
    
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

