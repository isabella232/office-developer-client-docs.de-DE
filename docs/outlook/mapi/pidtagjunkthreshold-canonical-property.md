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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326852"
---
# <a name="pidtagjunkthreshold-canonical-property"></a>PidTagJunkThreshold (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, wie aggressiv eingehende E-Mails an den Junk-E-Mail-Ordner gesendet werden sollen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_JUNK_THRESHOLD  <br/> |
|Kennung:  <br/> |0x6101  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft entspricht der Filtereinstellung hoch/niedrig/keine. Der Wert "0xFFFFFFFF" gibt an, dass die Spamfilterung nicht angewendet werden soll, Blocklisten müssen jedoch weiterhin angewendet werden. Der Wert "0x80000000" gibt an, dass alle E-Mails Spam sind, mit Ausnahme der Nachrichten von Absendern in der Liste vertrauenswürdiger Absender oder gesendet an Empfänger in der Liste vertrauenswürdiger Empfänger. Die Werte dafür sind wie folgt:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0xFFFFFFFF  <br/> |Keine Spamfilterung  <br/> |
|0x00000006  <br/> |Niedrige Spamfilterung  <br/> |
|0x00000003  <br/> |Hohe Spamfilterung  <br/> |
|0x80000000  <br/> |Nur Vertrauenswürdige Listen  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Zulässig-/Sperrlisten und die Ermittlung von Junk-E-Mail-Nachrichten.
    
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

