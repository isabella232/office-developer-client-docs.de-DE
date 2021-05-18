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
  
Der Text einer Nachricht kann mithilfe von Nur-Text oder formatiertem Text gespeichert und übertragen werden. Formatierter Text verbessert den Nachrichtentext, indem er seine Darstellung z. B. mit einer oder mehreren Schriftarten, Schriftgrößen oder Textfarben ändert. Es wird empfohlen, dass alle Clients und wann immer möglich alle Nachrichtenspeicheranbieter formatierten Text unterstützen. Die Unterstützung formatierter Texte in Nachrichten bietet einen Mehrwert, indem die Nachrichten lesbarkeit verbessert und die Nachrichtenverarbeitung einfacher und effizienter wird.
  
Formatierter Text kann auf unterschiedliche Weise implementiert werden. Die gängigste Methode ist das Rich Text Format (RTF). MAPI definiert drei durchlässige Eigenschaften zum Halten von Nachrichtentextinformationen: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) für Nur-Text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) für HTML und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) für komprimierten RTF-Text. Da die formatierte Version eines Nachrichtentexts doppelt so groß wie die Version ohne Formatierung sein kann, wird der RTF-Text komprimiert, bevor er mit der Nachricht übertragen und in der PR_RTF_COMPRESSED **gespeichert** wird. Wenn es an der Zeit ist, die Nachricht auf dem Bildschirm anzuzeigen, wird sie mithilfe einer Hilfsfunktion, die von MAPI bereitgestellt wird, nicht komprimiert. 
  
MAPI definiert diese beiden Nachrichtentexteigenschaften und -mechanismen für die Konvertierung zwischen diesen, sodass RTF-übergreifende Clients mit Clients und Messagingsystemen zusammenarbeiten können, die formatierten Text nicht unterstützen.
  
### 

[Synchronisieren von Text und Formatierung](synchronizing-text-and-formatting.md)
  
> Beschreibt, wie RTF-Nachrichtentext mit der Formatierung synchronisiert wird.
    
[Unterstützen von formatierten Text in ausgehenden Nachrichten: Clientaufgaben](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Beschreibt die Verantwortlichkeiten der Clientanwendung für die Unterstützung formatierten Texts in ausgehenden Nachrichten.
    
[Unterstützen von formatierten Text in eingehenden Nachrichten: Clientzu zuständigkeiten](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Beschreibt die Verantwortlichkeiten der Clientanwendung für die Unterstützung formatierten Texts in eingehenden Nachrichten.
    
[Unterstützen von formatierten Text: Nachrichten Store Verantwortlichkeiten](supporting-formatted-text-message-store-responsibilities.md)
  
> Beschreibt die Aufgaben des Nachrichtenspeichers für die Unterstützung formatierten Texts.
    
[Unterstützen von formatierten Text: Rendern von Anlagen](supporting-formatted-text-rendering-attachments.md)
  
> Beschreibt, wie Sie auswählen, wo Anlagen gerendert werden.
    
[Unterstützen von formatierten Text: Gateway-Verantwortlichkeiten](supporting-formatted-text-gateway-responsibilities.md)
  
> Beschreibt die Verantwortlichkeiten des Gateways für ausgehende und eingehende formatierte Textnachrichten.
    

