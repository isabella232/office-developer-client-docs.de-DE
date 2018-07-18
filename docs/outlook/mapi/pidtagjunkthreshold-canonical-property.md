---
title: PidTagJunkThreshold (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0f8484e195b1cda8e1d633133cdff89c571d8ecd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794538"
---
# <a name="pidtagjunkthreshold-canonical-property"></a>PidTagJunkThreshold (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt an, wie aggressiv eingehenden e-Mail-Nachrichten in den Junk-e-Mail-Ordner gesendet werden soll.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_JUNK_THRESHOLD  <br/> |
|Bezeichner:  <br/> |0x6101  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft entspricht der hoch / niedrig / keine Einstellung filtern. Der Wert "0xFFFFFFFF" gibt an, dass Spam-Filterung nicht angewendet werden soll, jedoch Sperrlisten weiterhin angewendet werden müssen. Der Wert "0 x 80000000" gibt an, dass alle e-Mails Spam außer diese Nachrichten von Absendern in der Liste vertrauenswürdiger Absender oder an Empfänger in der Liste vertrauenswürdiger Empfänger gesendet. Werte für dieses sind wie folgt:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0xFFFFFFFF  <br/> |Keine Spamfilterung  <br/> |
|0 x 00000006  <br/> |Niedrige Spamfilterung  <br/> |
|0 x 00000003  <br/> |Hohe Spamfilterung  <br/> |
|0 x 80000000  <br/> |Nur vertrauenswürdige Listen  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.
    
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

