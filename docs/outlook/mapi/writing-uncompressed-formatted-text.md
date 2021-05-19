---
title: Schreiben von nicht komprimierten formatierten Texten
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
# <a name="writing-uncompressed-formatted-text"></a>Schreiben von nicht komprimierten formatierten Texten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie das Senden einer Nachricht mit formatiertem Text **vorbereiten,** legen Sie entweder die eigenschaft PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) der Nachricht auf komprimierten oder nicht komprimierten Text festgelegt. Das Schreiben von komprimiertem Text in **PR_RTF_COMPRESSED** ist ein sehr CPU-intensiver Vorgang und kann sich erheblich auf die Leistung auswirken. 
  
Um die Leistung des Sendens formatierter Nachrichten zu verbessern, führen Sie entweder die
  
- Aktualisieren Sie die CPU, eine Lösung, die nicht immer plausibel ist.
    
    - Oder -
    
- Schreiben Sie unkomprimierten Text in die **PR_RTF_COMPRESSED** Eigenschaft. 
    
Das Verfahren zum Festlegen **PR_RTF_COMPRESSED** mit nicht komprimiertem Text ist identisch mit dem Festlegen mit komprimiertem Text, mit einer Ausnahme. Legen Sie [beim Aufrufen von WrapCompressedRTFStream](wrapcompressedrtfstream.md)das STORE_UNCOMPRESSED_RTF im  _ulFlags-Parameter_ ein. Das Festlegen von nicht komprimierten Text hat den Nachteil, dass die Größe von Nachrichten erhöht wird. 
  

