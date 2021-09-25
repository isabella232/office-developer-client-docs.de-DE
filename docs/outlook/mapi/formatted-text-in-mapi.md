---
title: Formatierter Text in MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 139eec84a6ea76b7328fc7fe42c648e56f861d75
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614185"
---
# <a name="formatted-text-in-mapi"></a>Formatierter Text in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Text einer Nachricht kann mit Nur-Text oder formatiertem Text gespeichert und übertragen werden. Formatierter Text verbessert den Nachrichtentext, indem seine Darstellung geändert wird, z. B. mit einer oder mehreren Schriftarten, Schriftgraden oder Textfarben. Es wird empfohlen, dass alle Clients und, wann immer möglich, alle Nachrichtenspeicheranbieter formatierten Text unterstützen. Die Unterstützung von formatiertem Text in Nachrichten bietet einen Mehrwert, indem die Lesbarkeit von Nachrichten verbessert und die Nachrichtenverarbeitung einfacher und effizienter wird.
  
Formatierter Text kann auf unterschiedliche Weise implementiert werden. Die gängigste Methode ist das Rich-Text-Format (RTF). MAPI definiert drei datenübertragungsfähige Eigenschaften zum Halten von Nachrichtentextinformationen: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) für Nur-Text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) für HTML und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) für RTF-Text, der komprimiert wurde. Da die formatierte Version eines Nachrichtentexts doppelt so groß sein kann wie die Version ohne Formatierung, wird der RTF-Text komprimiert, bevor er mit der Nachricht übertragen und in der **PR_RTF_COMPRESSED-Eigenschaft** gespeichert wird. Wenn es an der Zeit ist, die Nachricht auf dem Bildschirm anzuzeigen, wird sie mithilfe einer von MAPI bereitgestellten Hilfsprogrammfunktion nicht komprimiert. 
  
MAPI definiert diese beiden Nachrichtentexteigenschaften und Mechanismen für die Konvertierung zwischen ihnen, sodass RTF-fähige Clients mit Clients und Messagingsystemen zusammenarbeiten können, die formatierten Text nicht unterstützen.
  
### 

[Synchronisieren von Text und Formatierung](synchronizing-text-and-formatting.md)
  
> Beschreibt, wie RTF-Nachrichtentext mit der Formatierung synchronisiert bleibt.
    
[Unterstützen von formatiertem Text in ausgehenden Nachrichten: Clientaufgaben](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Beschreibt die Zuständigkeiten der Clientanwendung für die Unterstützung von formatiertem Text in ausgehenden Nachrichten.
    
[Unterstützen von formatiertem Text in eingehenden Nachrichten: Verantwortlichkeiten des Clients](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Beschreibt die Zuständigkeiten der Clientanwendung für die Unterstützung von formatiertem Text in eingehenden Nachrichten.
    
[Unterstützen von formatiertem Text: Nachrichten Store Zuständigkeiten](supporting-formatted-text-message-store-responsibilities.md)
  
> Beschreibt die Zuständigkeiten des Nachrichtenspeichers für die Unterstützung von formatiertem Text.
    
[Unterstützen von formatiertem Text: Rendern von Anlagen](supporting-formatted-text-rendering-attachments.md)
  
> Beschreibt, wie sie auswählen, wo Anlagen gerendert werden.
    
[Unterstützen von formatiertem Text: Gateway-Zuständigkeiten](supporting-formatted-text-gateway-responsibilities.md)
  
> Beschreibt die Zuständigkeiten des Gateways für ausgehende und eingehende formatierte Textnachrichten.
    

