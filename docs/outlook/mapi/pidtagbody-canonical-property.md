---
title: PidTagBody (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326635"
---
# <a name="pidtagbody-canonical-property"></a>PidTagBody (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Nachrichtentext.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_BODY, PR_BODY_A, PR_BODY_W  <br/> |
|Kennung:  <br/> |0x1000  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften werden in der Regel nur in einer zwischenpersönlichen Nachricht (IPM) verwendet. 
  
Nachrichtenspeicher, die Rich Text Format (RTF) unterstützen, ignorieren alle Änderungen an Leerzeichen im Nachrichtentext. Wenn **PR_BODY** zum ersten Mal gespeichert wird, generiert und speichert der Nachrichtenspeicher auch die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft, die #A0 des Nachrichtentexts. Wenn die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) anschließend aufgerufen wird und **PR_BODY** geändert wurde, ruft der Nachrichtenspeicher die [RTFSync-Funktion](rtfsync.md) auf, um die Synchronisierung mit der RTF-Version sicherzustellen. Wenn nur Leerzeichen geändert wurden, bleiben die Eigenschaften unverändert. Dadurch wird jede nichttriviale RTF-Formatierung beibehalten, wenn die Nachricht über nicht RTF-wahrneige Clients und Messagingsysteme geht. 
  
Der Wert für diese Eigenschaft muss auf der Codeseite des Betriebssystems ausgedrückt werden, auf dem MAPI ausgeführt wird. 
  
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



[PidTagRtfInSync (kanonische Eigenschaft)](pidtagrtfinsync-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

