---
title: PidTagRtfInSync (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357876"
---
# <a name="pidtagrtfinsync-canonical-property"></a>PidTagRtfInSync (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält **TRUE, wenn die PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) denselben Textinhalt wie die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft für diese Nachricht hat.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RTF_IN_SYNC  <br/> |
|Kennung:  <br/> |0x0E1F  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |E-Mails  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert TRUE bedeutet, dass die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft, die Nur-Text-Version dieser Nachricht und die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft, die Rich Text Format (RTF)-Version, mit Ausnahme von Leerzeichen in **PR_BODY** und Formatierung in **PR_RTF_COMPRESSED identisch sind.** Der Text in den beiden Versionen besteht aus denselben Zeichen in derselben Sequenz.
  
Der Wert FALSE bedeutet, dass die beiden Versionen nicht für Textinhalte synchronisiert werden, sondern von der [RTFSync-Funktion synchronisiert werden](rtfsync.md) können. Eine Version wurde geändert, die andere version nicht. 
  
Kein Wert bedeutet, dass die beiden Versionen, sofern vorhanden oder jemals vorhanden, nicht synchronisiert werden können. Eine Version wurde so radikal gelöscht oder geändert, dass eine Synchronisierung nicht mehr möglich ist.
  
Eine Clientanwendung, die **PR_RTF_COMPRESSED** geändert hat, sollte in dieser Eigenschaft den Wert FALSE festlegen, um die Synchronisierung zu erzwingen. RTF-benachrichtigungsspeicher sollten die Synchronisierung mithilfe von **RTFSync** während eines [IMAPIProp::SaveChanges-Aufrufs](imapiprop-savechanges.md) ausführen. RTF- aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary. 
  
Wenn **PR_BODY** änderungen an einem anderen Leerzeichen als dem Leerzeichen vorgenommen haben, muss der Nachrichtenspeicher PR_RTF_IN_SYNC **löschen,** um die Synchronisierung zu beenden. 
  
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

