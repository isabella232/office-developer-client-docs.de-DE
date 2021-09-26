---
title: PidTagSpamThreshold (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2b2d6b8e-e3dd-4a9b-8bb5-53add675605d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 01c0a1c0128e378bb47ce2eade6a3184da87fbb1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624489"
---
# <a name="pidtagspamthreshold-canonical-property"></a>PidTagSpamThreshold (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein long-Wert, der die Ebene der Spamfilterung angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SPAM_THRESHOLD  <br/> |
|Long ID (LID):  <br/> | 0x041B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="values"></a>Werte

Die Werte für die Spamfilterung sind wie folgt:
  
|**Spamstufe**|**Wert**|
|:-----|:-----|
|Keines  <br/> |0xFFFFFFFF  <br/> |
|Niedrig  <br/> |0x00000006  <br/> |
|Medium  <br/> |0x00000005  <br/> |
|Hoch  <br/> |0x00000003  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Microsoft Exchange Server Protokollspezifikationen bereit.
    
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

