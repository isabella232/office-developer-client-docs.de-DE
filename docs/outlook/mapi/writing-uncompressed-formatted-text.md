---
title: Schreiben von nicht komprimiertem formatierten Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d34168743926681ee7169a593e302755b193aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577044"
---
# <a name="writing-uncompressed-formatted-text"></a>Schreiben von nicht komprimiertem formatierten Text

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bei der Vorbereitung zum Senden einer Nachricht mit formatierten Text, legen Sie entweder die Nachricht **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft in komprimierten oder nicht komprimierten Text. Schreiben von komprimierten Text in der **PR_RTF_COMPRESSED** -Eigenschaft ist ein sehr CPU-intensiver Vorgang und kann die Leistung erheblich beeinträchtigen. 
  
Zur Verbesserung der Leistung der formatierte Nachrichten entweder senden:
  
- Aktualisieren Sie die CPU, eine Lösung, die nicht immer plausibel ist.
    
    - Oder -
    
- Schreiben von nicht komprimierten Text in der **PR_RTF_COMPRESSED** -Eigenschaft. 
    
Das Verfahren zum Festlegen von **PR_RTF_COMPRESSED** mit nicht komprimierten Text ist die gleichen wie für das Festlegen der Steuerelementvorlage mit komprimierten Text mit einer Ausnahme. Beim Aufruf von [WrapCompressedRTFStream](wrapcompressedrtfstream.md)festlegen Sie STORE_UNCOMPRESSED_RTF das Flag im _UlFlags_ -Parameter. Festlegen der nicht komprimierten Text hat den Nachteil, dass sie die Größe der Nachrichten erhöht. 
  

