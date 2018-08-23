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
ms.openlocfilehash: bfaa4fd5f561c8138461db6ce8b9033c2a75b96b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580628"
---
# <a name="formatted-text-in-mapi"></a>Formatierter Text in MAPI

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Der Text einer Nachricht gespeichert werden kann und mit unformatiertem Text gesendet oder formatierter Text. Formatierter Text erhöht den Nachrichtentext durch seine Darstellung mit, beispielsweise eine oder mehrere Schriftarten, Schriftgrößen oder Textfarben ändern. Es wird empfohlen, alle Clients und möglichst unterstützen alle Nachricht Speicher-Anbieter formatierten Text. Unterstützung von formatierten Text in Nachrichten fügt Wert durch Verbesserung der Lesbarkeit Nachricht und tätigen Nachrichtenbehandlung einfacher und effizienter hinzu.
  
Formatierter Text kann in verschiedene Arten implementiert werden. Die am häufigsten verwendete Methode ist mit Rich Text Format (RTF). MAPI definiert drei Übertragungseinehit Eigenschaften zum Aufbewahren von Text Nachrichteninformationen: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) für nur-Text, **http://Schemas.Microsoft.com/mapi/proptag/0x10130102** ([PidTagHtml](pidtaghtml-canonical-property.md)) für HTML und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) für RTF-Text komprimiert wurde. Da die formatierte Version der einen Meldungstext zweimal so groß wie die Version ist, kann ohne Formatierung wird RTF-Text komprimiert, bevor sie mit der Meldung übertragen und in der Eigenschaft **PR_RTF_COMPRESSED** gespeichert wird. Wenn die Meldung auf dem Bildschirm angezeigt wird, ist es nicht komprimierten mithilfe einer Dienstprogrammfunktion von MAPI bereitgestellt. 
  
MAPI definiert diese beiden Text Nachrichteneigenschaften und Mechanismen für die Konvertierung zwischen diesen so, dass RTF-fähigen Clients mit Clients und bieten keine Unterstützung für messaging-Systemen interagieren können formatierter Text.
  
### 

[Synchronisieren von Text und Formatierung](synchronizing-text-and-formatting.md)
  
> Beschreibt, wie RTF Nachrichtentext synchronisiert mit der Formatierung beibehalten.
    
[Unterstützung von formatiertem Text in ausgehenden Nachrichten: Kundenaufgaben](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Beschreibt die Client-Anwendung Aufgaben zur Unterstützung von formatierten Texts in ausgehenden Nachrichten.
    
[Unterstützung von formatiertem Text in eingehenden Nachrichten: Kundenaufgaben](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Client-Anwendung Aufgaben zur Unterstützung von formatierten Texts in eingehenden Nachrichten beschrieben.
    
[Unterstützung von formatiertem Text: Aufgaben des Nachrichtenspeichers](supporting-formatted-text-message-store-responsibilities.md)
  
> Beschreibt Nachricht Store Verantwortung für die Unterstützung von formatierten Texts.
    
[Unterstützung von formatiertem Text: Darstellung von Anlagen](supporting-formatted-text-rendering-attachments.md)
  
> Beschreibt, wie auswählen, in dem Anlagen gerendert werden.
    
[Unterstützung von formatiertem Text: Aufgaben des Gateways](supporting-formatted-text-gateway-responsibilities.md)
  
> Beschreibt die Gateway Zuständigkeiten für ausgehenden und eingehenden formatierter Text-Nachrichten.
    

