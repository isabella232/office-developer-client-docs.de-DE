---
title: Kanonische PidTagSpamThreshold-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2b2d6b8e-e3dd-4a9b-8bb5-53add675605d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 24a033269b072712fea6e9957d0ffac3573ce3a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795173"
---
# <a name="pidtagspamthreshold-canonical-property"></a>Kanonische PidTagSpamThreshold-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Ein long-Wert, der angibt, die Ebene der Spam-Filterung.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SPAM_THRESHOLD  <br/> |
|Long-ID (Abdeckung):  <br/> | 0x041B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="values"></a>Werte

Die Werte für das Filtern von Spam sind wie folgt:
  
|**Spam-Ebene**|**Wert**|
|:-----|:-----|
|Keine  <br/> |0xFFFFFFFF  <br/> |
|Low  <br/> |0 x 00000006  <br/> |
|Medium  <br/> |0 x 00000005  <br/> |
|High  <br/> |0 x 00000003  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.
    
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

