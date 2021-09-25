---
title: PidTagJunkThreshold (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 82fe1f1d12e37e9eb1cc1dbddc7e14da54feb058
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599952"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft entspricht der Filtereinstellung Hoch /Niedrig/ Keine. Der Wert "0xFFFFFFFF" gibt an, dass die Spamfilterung nicht angewendet werden soll, sperrlisten müssen jedoch weiterhin angewendet werden. Der Wert "0x80000000" gibt an, dass alle E-Mails Spam sind, mit Ausnahme der Nachrichten von Absendern in der Liste der vertrauenswürdigen Absender oder gesendet an Empfänger in der Liste der vertrauenswürdigen Empfänger. Die Werte hierfür sind wie folgt:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0xFFFFFFFF  <br/> |Keine Spamfilterung  <br/> |
|0x00000006  <br/> |Geringe Spamfilterung  <br/> |
|0x00000003  <br/> |Hohe Spamfilterung  <br/> |
|0x80000000  <br/> |Nur Vertrauenswürdige Listen  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Zulassungs-/Sperrlisten und die Ermittlung von Junk-E-Mail-Nachrichten.
    
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

