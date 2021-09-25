---
title: Kanonische PidTagBody-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1b4d8d6c3820d0e2954f556f6217cacc1f1a0ea2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571213"
---
# <a name="pidtagbody-canonical-property"></a>Kanonische PidTagBody-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Nachrichtentext.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_BODY, PR_BODY_A, PR_BODY_W  <br/> |
|Kennung:  <br/> |0x1000  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften werden in der Regel nur in einer zwischenmenschlichen Nachricht (Interpersonal Message, IPM) verwendet. 
  
Nachrichtenspeicher, die RTF (Rich Text Format) unterstützen, ignorieren alle Änderungen an Leerzeichen im Nachrichtentext. Wenn **PR_BODY** zum ersten Mal gespeichert wird, generiert und speichert der Nachrichtenspeicher auch die **eigenschaft PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), die RTF-Version des Nachrichtentexts. Wenn die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) anschließend aufgerufen wird und **PR_BODY** geändert wurde, ruft der Nachrichtenspeicher die [RTFSync-Funktion](rtfsync.md) auf, um die Synchronisierung mit der RTF-Version sicherzustellen. Wenn nur Leerzeichen geändert wurden, bleiben die Eigenschaften unverändert. Dadurch bleiben alle nichttrivialen RTF-Formatierungen erhalten, wenn die Nachricht nicht RTF-fähige Clients und Messagingsysteme durchsucht. 
  
Der Wert für diese Eigenschaft muss auf der Codeseite des Betriebssystems ausgedrückt werden, auf dem die MAPI ausgeführt wird. 
  
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



[PidTagRtfInSync (kanonische Eigenschaft)](pidtagrtfinsync-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

