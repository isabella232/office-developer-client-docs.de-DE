---
title: Schreiben von unkomprimiertem formatiertem Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bfa6527b177f5dcedc3c1f10a0f36c3c6301a5bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619428"
---
# <a name="writing-uncompressed-formatted-text"></a>Schreiben von unkomprimiertem formatiertem Text

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie das Senden einer Nachricht mit formatiertem Text vorbereiten, legen Sie entweder die **eigenschaft PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) der Nachricht auf komprimierten oder nicht komprimierten Text fest. Das Schreiben von komprimiertem Text in der **PR_RTF_COMPRESSED-Eigenschaft** ist ein sehr CPU-intensiver Vorgang und kann sich erheblich auf die Leistung auswirken. 
  
Um die Leistung des Sendens formatierter Nachrichten zu verbessern, müssen Sie die folgenden Aktionen ausführen:
  
- Aktualisieren Sie die CPU, eine Lösung, die nicht immer sehr gut ist.
    
    - Oder -
    
- Schreiben Sie unkomprimierten  Text in die PR_RTF_COMPRESSED-Eigenschaft. 
    
Die Vorgehensweise zum Festlegen **von PR_RTF_COMPRESSED** mit nicht komprimiertem Text ist identisch mit dem Festlegen mit komprimiertem Text, mit einer Ausnahme. Legen Sie beim Aufrufen von [WrapCompressedRTFStream](wrapcompressedrtfstream.md)das flag STORE_UNCOMPRESSED_RTF im  _UlFlags-Parameter_ fest. Das Festlegen von unkomprimiertem Text hat den Nachteil, dass die Größe von Nachrichten erhöht wird. 
  

