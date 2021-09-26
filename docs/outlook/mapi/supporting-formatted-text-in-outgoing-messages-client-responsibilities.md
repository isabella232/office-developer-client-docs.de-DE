---
title: Unterstützen von formatiertem Text in Den Zuständigkeiten des Clients für ausgehende Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b5cf44ddaafcfd30637516e90ef9a62caf265ed8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591010"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Unterstützen von formatiertem Text in ausgehenden Nachrichten: Clientaufgaben

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen legen die **eigenschaft PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), die **eigenschaft PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder die **eigenschaft PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) für eine ausgehende Nachricht fest. Clients, die nur Nur-Text unterstützen, legen nur die **PR_BODY-Eigenschaft** fest. RtF-fähige Clients (Rich Text Format) können abhängig vom verwendeten Nachrichtenspeicheranbieter sowohl **PR_BODY** als auch **PR_RTF_COMPRESSED** Eigenschaften oder nur **PR_RTF_COMPRESSED** festlegen. HTML-fähige Clients legen die **PR_HTML-Eigenschaft** fest. 
  
Es ist wichtig, dass ein Client die **Eigenschaft PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) des Nachrichtenspeichers überprüft, um festzustellen, ob der Speicher RTF unterstützt. Wenn der Nachrichtenspeicher nicht RTF-fähig ist, legt ein RTF-fähiger Client die **Eigenschaften PR_BODY** und **PR_RTF_COMPRESSED** für jede ausgehende Nachricht fest. 
  
Wenn der Nachrichtenspeicher RTF-fähig ist, muss nur die **eigenschaft PR_RTF_COMPRESSED** festgelegt werden. 
  
 **RtF-fähige Clients, um PR_RTF_COMPRESSED festzulegen und sicherzustellen, dass der Synchronisierungsprozess bei Bedarf erfolgt**
  
1. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) auf, um die **PR_RTF_COMPRESSED-Eigenschaft** zu öffnen, indem Sie sowohl die MAPI_CREATE als auch MAPI_MODIFY Flags festlegen. MAPI_CREATE stellt sicher, dass alle neuen Daten alte Daten ersetzen, und MAPI_MODIFY ermöglicht es Ihnen, diese Ersetzungen vorzunehmen. 
    
2. Rufen Sie die [WrapCompressedRTFStream-Funktion](wrapcompressedrtfstream.md) auf, und übergeben Sie STORE_UNCOMPRESSED_RTF, wenn der Nachrichtenspeicher das STORE_UNCOMPRESSED_RTF Bit in seiner **PR_STORE_SUPPORT_MASK-Eigenschaft** festlegt, um eine nicht komprimierte Version des von **OpenProperty** zurückgegebenen PR_RTF_COMPRESSED Datenstroms abzurufen. 
    
3. Schreiben Sie die Nachrichtentextdaten in den nicht komprimierten Stream, der von **WrapCompressedRTFStream** zurückgegeben wird.
    
4. Übernehmen und freigeben Sie sowohl den unkomprimierten als auch den komprimierten Datenstrom.
    
Wenn der Nachrichtenspeicheranbieter RTF unterstützt, haben Sie nun alle erforderlichen Schritte ausgeführt. Sie können vom Nachrichtenspeicheranbieter abhängig sein, um den Synchronisierungsprozess und ggf. die Erstellung der **PR_BODY-Eigenschaft** zu verarbeiten. Wenn der Nachrichtenspeicheranbieter RTF jedoch nicht unterstützt, müssen Sie die [RTFSync-Funktion](rtfsync.md) aufrufen, um den Text mit der Formatierung zu synchronisieren, indem Sie das RTF_SYNC_RTF_CHANGED Flag festlegen. 
  

