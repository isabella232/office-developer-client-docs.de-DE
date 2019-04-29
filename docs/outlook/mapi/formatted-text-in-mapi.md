---
title: Formatierter Text in MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f37d65e4beb328c2c92cf0c2ab28586af6bee45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408089"
---
# <a name="formatted-text-in-mapi"></a>Formatierter Text in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Text einer Nachricht kann mit nur-Text oder formatiertem Text gespeichert und übertragen werden. Formatierter Text verbessert den Nachrichtentext, indem sein Aussehen mit beispielsweise einer oder mehreren Schriftarten, Schriftgraden oder Textfarben geändert wird. Es wird empfohlen, dass alle Clients und nach Möglichkeit alle Nachrichtenspeicher Anbieter formatierten Text unterstützen. Die Unterstützung von formatiertem Text in Nachrichten bietet einen Mehrwert durch verbesserte Nachrichten Lesbarkeit und eine einfachere und effizientere Nachrichtenverarbeitung.
  
Formatierter Text kann auf verschiedene Arten implementiert werden. Die häufigste Methode ist das Rich-Text-Format (RTF). MAPI definiert drei transmitable-Eigenschaften für die Aufbewahrung von Nachrichtentext Informationen: **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)) für nur-Text, **PR_HTML** ([pidtaghtml (](pidtaghtml-canonical-property.md)) für HTML und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) für RTF-Text, der komprimiert wurde. Da die formatierte Version eines Nachrichtentexts doppelt so groß wie die Version ohne Formatierung sein kann, wird der RTF-Text komprimiert, bevor er mit der Nachricht übertragen und in der **PR_RTF_COMPRESSED** -Eigenschaft gespeichert wird. Wenn die Nachricht auf dem Bildschirm angezeigt werden soll, wird Sie mithilfe einer von MAPI bereitgestellten Hilfsfunktion unkomprimiert entpackt. 
  
MAPI definiert diese beiden Nachrichtentext Eigenschaften und-Mechanismen für die Konvertierung zwischen diesen, sodass RTF-fähige Clients mit Clients und Messagingsystemen interagieren können, die keinen formatierten Text unterstützen.
  
### 

[Synchronisieren von Text und Formatierung](synchronizing-text-and-formatting.md)
  
> Beschreibt, wie der RTF-Nachrichtentext mit der Formatierung synchronisiert bleibt.
    
[Unterstützung von formatiertem Text in ausgehenden Nachrichten: Aufgaben des Kunden](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Beschreibt die Verantwortlichkeiten der Clientanwendung für die Unterstützung von formatiertem Text in ausgehenden Nachrichten.
    
[Unterstützung von formatiertem Text in eingehenden Nachrichten: Aufgaben des Kunden](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Beschreibt die Verantwortlichkeiten der Clientanwendung für die Unterstützung von formatiertem Text in eingehenden Nachrichten.
    
[Unterstützung von formatiertem Text: Aufgaben des Nachrichtenspeichers](supporting-formatted-text-message-store-responsibilities.md)
  
> Beschreibt die Aufgaben des Nachrichtenspeichers zur Unterstützung von formatiertem Text.
    
[Unterstützung von formatiertem Text: Rendering Attachments](supporting-formatted-text-rendering-attachments.md)
  
> Beschreibt, wie Sie auswählen, wo Anlagen gerendert werden.
    
[Unterstützung von formatiertem Text: Aufgaben des Gateways](supporting-formatted-text-gateway-responsibilities.md)
  
> Beschreibt die Aufgaben des Gateways für ausgehende und eingehende formatierte Textnachrichten.
    

