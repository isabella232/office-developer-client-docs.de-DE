---
title: Schreiben von nicht komprimiertem formatiertem Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426324"
---
# <a name="writing-uncompressed-formatted-text"></a>Schreiben von nicht komprimiertem formatiertem Text

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim Vorbereiten des Sendens einer Nachricht mit formatiertem Text legen Sie die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft der Nachricht auf komprimierten oder nicht komprimierten Text fest. Das Schreiben von komprimiertem Text in der **PR_RTF_COMPRESSED** -Eigenschaft ist ein sehr CPU-intensiver Vorgang und kann die Leistung erheblich beeinträchtigen. 
  
Um die Leistung beim Senden formatierter Nachrichten zu verbessern, können Sie Folgendes tun:
  
- Upgraden Sie die CPU, eine Lösung, die nicht immer plausibel ist.
    
    - Oder
    
- Schreiben Sie unkomprimierten Text in der **PR_RTF_COMPRESSED** -Eigenschaft. 
    
Die Vorgehensweise zum Festlegen von **PR_RTF_COMPRESSED** mit unkomprimiertem Text ist identisch mit der Einstellung für den komprimierten Text mit einer Ausnahme. Legen Sie beim Aufrufen von [WrapCompressedRTFStream](wrapcompressedrtfstream.md)die STORE_UNCOMPRESSED_RTF-Kennzeichnung im _ulFlags_ -Parameter fest. Das Festlegen von nicht komprimiertem Text hat den Nachteil, dass die Größe der Nachrichten erhöht wird. 
  

