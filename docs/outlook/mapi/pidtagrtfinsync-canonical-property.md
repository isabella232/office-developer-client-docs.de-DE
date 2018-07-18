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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 85e517601d291f144652befa267d8fd8f76dea64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795016"
---
# <a name="pidtagrtfinsync-canonical-property"></a>PidTagRtfInSync (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält True, wenn die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft auf denselben Textinhalt wie die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft für diese Nachricht verfügt.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RTF_IN_SYNC  <br/> |
|Bezeichner:  <br/> |0x0E1F  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |E-Mail  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert "true" bedeutet, denen die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft, die nur-Text-Version dieser Nachricht und die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft, die Version von Rich Text Format (RTF), mit Ausnahme von identisch sind Leerzeichen in **PR_BODY** und Formatierungen im **PR_RTF_COMPRESSED**. Der Text in den beiden Versionen umfasst die gleichen Zeichen in der gleichen Reihenfolge.
  
Der Wert FALSE bedeutet, dass die beiden Versionen für Textinhalt nicht synchronisiert sind, jedoch werden von der Funktion [RTFSync](rtfsync.md) synchronisiert werden können. Eine Version geändert wurde und die andere Version hat nicht. 
  
Kein Wert bedeutet, dass die beiden Versionen, wenn beide vorhanden sind oder jemals vorhanden waren, synchronisiert werden können. Eine Version wurde gelöscht oder geändert, sodass Produktivitätssteigerungen, dass die Synchronisierung nicht mehr möglich ist.
  
Eine Clientanwendung, die **PR_RTF_COMPRESSED** geändert hat sollte der Wert in dieser Eigenschaft zum Erzwingen der Synchronisierung FALSE festgelegt. RTF-fähigen Nachrichtenspeicher sollten die Synchronisierung mit **RTFSync** während eines Anrufs [IMAPIProp::SaveChanges](imapiprop-savechanges.md) durchführen. RTF-fähigen Clients sollte die Einstellung von **PR_RTF_IN_SYNC** vor dem Lesen **PR_RTF_COMPRESSED**überprüfen, und rufen Sie **RTFSync** zuerst bei Bedarf. 
  
Wenn **PR_BODY** Änderungen an einen anderen Wert als deren Leerraum wurde, muss der Nachrichtenspeicher **PR_RTF_IN_SYNC** , um die Synchronisierung zu beenden löschen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
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

