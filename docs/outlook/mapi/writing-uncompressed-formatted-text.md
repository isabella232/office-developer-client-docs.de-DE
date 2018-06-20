---
title: Schreiben von nicht komprimierten formatierter Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9baf3397255d6138caaad84de5ff5621bd6c9555
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795869"
---
# <a name="writing-uncompressed-formatted-text"></a>Schreiben von nicht komprimierten formatierter Text

  
  
**Betrifft**: Outlook 
  
Bei der Vorbereitung zum Senden einer Nachricht mit formatierten Text, legen Sie entweder die Nachricht **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft in komprimierten oder nicht komprimierten Text. Schreiben von komprimierten Text in der **PR_RTF_COMPRESSED** -Eigenschaft ist ein sehr CPU-intensiver Vorgang und kann die Leistung erheblich beeinträchtigen. 
  
Zur Verbesserung der Leistung der formatierte Nachrichten entweder senden:
  
- Aktualisieren Sie die CPU, eine Lösung, die nicht immer plausibel ist.
    
    - Oder -
    
- Schreiben von nicht komprimierten Text in der **PR_RTF_COMPRESSED** -Eigenschaft. 
    
Das Verfahren zum Festlegen von **PR_RTF_COMPRESSED** mit nicht komprimierten Text ist die gleichen wie für das Festlegen der Steuerelementvorlage mit komprimierten Text mit einer Ausnahme. Beim Aufruf von [WrapCompressedRTFStream](wrapcompressedrtfstream.md)festlegen Sie STORE_UNCOMPRESSED_RTF das Flag im _UlFlags_ -Parameter. Festlegen der nicht komprimierten Text hat den Nachteil, dass sie die Größe der Nachrichten erhöht. 
  

