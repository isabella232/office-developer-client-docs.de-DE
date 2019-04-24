---
title: Kanonische Pidtagspamthreshold (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2b2d6b8e-e3dd-4a9b-8bb5-53add675605d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d43a0229f232f9437d1746799534c0f2d6fba83f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346312"
---
# <a name="pidtagspamthreshold-canonical-property"></a>Kanonische Pidtagspamthreshold (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Long-Wert, der den Grad der Spamfilterung angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SPAM_THRESHOLD  <br/> |
|Long-ID (Deckel):  <br/> | 0x041B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="values"></a>Werte

Die Werte für die Spamfilterung lauten wie folgt:
  
|**Spam-Level**|**Wert**|
|:-----|:-----|
|Keine  <br/> |0xFFFFFFFF  <br/> |
|Niedrig  <br/> |0x00000006  <br/> |
|Mittel  <br/> |0x00000005  <br/> |
|Hoch  <br/> |0x00000003  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Microsoft Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Allow/Block-Listen und die Bestimmung von Junk-e-Mails.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

