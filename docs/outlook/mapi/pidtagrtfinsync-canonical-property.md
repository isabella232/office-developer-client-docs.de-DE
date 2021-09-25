---
title: PidTagRtfInSync (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 72a94f6063dcc1abd1ca5c17d8bc048baad7953e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604215"
---
# <a name="pidtagrtfinsync-canonical-property"></a>PidTagRtfInSync (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RTF_IN_SYNC  <br/> |
|Kennung:  <br/> |0x0E1F  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |E-Mails  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert TRUE bedeutet, dass die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft, die Nur-Text-Version dieser Nachricht und die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft, die RTF-Version (Rich Text Format) identisch sind, mit Ausnahme von Leerzeichen in **PR_BODY** und Formatierung in **PR_RTF_COMPRESSED**. Der Text in den beiden Versionen besteht aus denselben Zeichen in derselben Sequenz.
  
Der Wert FALSE bedeutet, dass die beiden Versionen nicht für Textinhalte synchronisiert werden, sondern von der [RTFSync-Funktion](rtfsync.md) synchronisiert werden können. Eine Version wurde geändert, die andere nicht. 
  
Kein Wert bedeutet, dass die beiden Versionen nicht synchronisiert werden können, wenn beide versionen vorhanden sind oder jemals vorhanden sind. Eine Version wurde gelöscht oder so stark geändert, dass eine Synchronisierung nicht mehr möglich ist.
  
Eine Clientanwendung, die **PR_RTF_COMPRESSED** geändert hat, sollte in dieser Eigenschaft den Wert FALSE festlegen, um die Synchronisierung zu erzwingen. RTF-fähige Nachrichtenspeicher sollten die Synchronisierung mit **RTFSync** während eines [IMAPIProp::SaveChanges-Aufrufs](imapiprop-savechanges.md) durchführen. RTF-fähige Clients sollten die Einstellung von **PR_RTF_IN_SYNC** überprüfen, bevor **sie PR_RTF_COMPRESSED** lesen, und **RTFSync** bei Bedarf zuerst aufrufen. 
  
Wenn **PR_BODY** Änderungen an anderen Elementen als dem Leerzeichen vorgenommen hat, muss der Nachrichtenspeicher **PR_RTF_IN_SYNC** löschen, um die Synchronisierung zu beenden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

