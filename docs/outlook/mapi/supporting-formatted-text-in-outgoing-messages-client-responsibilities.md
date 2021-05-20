---
title: Unterstützen von formatierten Text in Clientaufgaben für ausgehende Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431603"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Unterstützen von formatierten Text in ausgehenden Nachrichten: Clientaufgaben

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen legen die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft, die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft oder die **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) -Eigenschaft für eine ausgehende Nachricht. Clients, die nur Nur-Text unterstützen, legen nur die **PR_BODY** fest. RtF-bewusste Clients (Rich Text  Format) können PR_BODY- und **PR_RTF_COMPRESSED-Eigenschaften** oder nur **PR_RTF_COMPRESSED** festlegen, abhängig vom verwendeten Nachrichtenspeicheranbieter. HTML- aware clients set **the PR_HTML** property. 
  
Es ist wichtig, dass ein Client die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft des Nachrichtenspeichers überprüft, um zu bestimmen, ob der Speicher RTF unterstützt. Wenn der Nachrichtenspeicher nicht RTF-bewusst ist, legt  ein RTF-bewusster Client die Eigenschaften PR_BODY und **PR_RTF_COMPRESSED** für jede ausgehende Nachricht fest. 
  
Wenn der Nachrichtenspeicher RTF-bewusst ist, muss nur **die PR_RTF_COMPRESSED** festgelegt werden. 
  
 **Zum Festlegen PR_RTF_COMPRESSED und sicherstellen, dass der Synchronisierungsprozess bei Bedarf ausgeführt wird, müssen RTF-bewusste Clients**
  
1. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) auf, um die **PR_RTF_COMPRESSED-Eigenschaft** zu öffnen, indem Sie sowohl die MAPI_CREATE als auch MAPI_MODIFY festlegen. MAPI_CREATE stellt sicher, dass alle neuen Daten alte Daten ersetzen und MAPI_MODIFY sie ersetzen können. 
    
2. Rufen Sie die [WrapCompressedRTFStream-Funktion](wrapcompressedrtfstream.md) auf, und übergeben Sie STORE_UNCOMPRESSED_RTF, wenn der Nachrichtenspeicher das STORE_UNCOMPRESSED_RTF-Bit in seiner **PR_STORE_SUPPORT_MASK-Eigenschaft** fest, um eine nicht komprimierte Version des PR_RTF_COMPRESSED-Datenstroms zu erhalten, der von **OpenProperty** zurückgegeben wird. 
    
3. Schreiben Sie die Nachrichtentextdaten in den nicht komprimierten Datenstrom, der von **WrapCompressedRTFStream zurückgegeben wird.**
    
4. Commit und Freigabe der nicht komprimierten und komprimierten Datenströme.
    
Wenn der Nachrichtenspeicheranbieter zu diesem Zeitpunkt RTF unterstützt, haben Sie alles erforderliche getan. Sie können vom Nachrichtenspeicheranbieter abhängig sein, um den Synchronisierungsprozess und die Erstellung der **PR_BODY-Eigenschaft** zu verarbeiten, falls erforderlich. Wenn der Nachrichtenspeicheranbieter rtF jedoch nicht unterstützt, müssen Sie die [RTFSync-Funktion](rtfsync.md) aufrufen, um den Text mit der Formatierung zu synchronisieren, indem Sie RTF_SYNC_RTF_CHANGED festlegen. 
  

