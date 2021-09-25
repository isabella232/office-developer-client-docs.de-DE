---
title: PidTagRtfSyncBodyCount (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cc56dffeb1be879333b98c8469a3c16a11489148
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604207"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a>PidTagRtfSyncBodyCount (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Anzahl der wichtigen Zeichen des Nachrichtentexts.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RTF_SYNC_BODY_COUNT  <br/> |
|Kennung:  <br/> |0x1007  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Nachricht  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die [RTFSync-Funktion](rtfsync.md) berechnet die Anzahl der Zeichen im Text nur mit den Zeichen, die für die Nachricht von Bedeutung sind. Beispielsweise werden einige Leerzeichen und andere ignorierte Zeichen aus der Anzahl weggelassen. 
  
Diese Eigenschaft ist eine RTF-Hilfseigenschaft (Rich Text Format). Diese Eigenschaften werden von der **RTFSync-Funktion** verwendet und sind nicht für die direkte Verwendung durch Clientanwendungen vorgesehen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in einer effizienten Datenstromdarstellung.
    
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

