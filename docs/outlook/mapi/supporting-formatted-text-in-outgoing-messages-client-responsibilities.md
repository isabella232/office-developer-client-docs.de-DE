---
title: Unterstützung von formatiertem Text in den Client Aufgaben für ausgehende Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327405"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Unterstützung von formatiertem Text in ausgehenden Nachrichten: Aufgaben des Kunden

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Client Anwendungen legen die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft, die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft oder die **PR_HTML** ([pidtaghtml (](pidtaghtml-canonical-property.md))-Eigenschaft für eine ausgehende Nachricht fest. Clients, die nur einfachen Text unterstützen, legen nur die **PR_BODY** -Eigenschaft fest. Rich Text Format (RTF)-fähige Clients können sowohl **PR_BODY** -als auch **PR_RTF_COMPRESSED** -Eigenschaften oder nur **PR_RTF_COMPRESSED**-abhängig vom verwendeten Nachrichtenspeicher Anbieter festlegen. HTML-fähige Clients legen die **PR_HTML** -Eigenschaft fest. 
  
Es ist wichtig, dass ein Client die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Nachrichtenspeichers überprüft, um zu bestimmen, ob der Speicher RTF unterstützt. Wenn der Nachrichtenspeicher nicht RTF-fähig ist, legt ein RTF-fähiger Client sowohl die **PR_BODY** -als auch die **PR_RTF_COMPRESSED** -Eigenschaft für jede ausgehende Nachricht fest. 
  
Wenn der Nachrichtenspeicher RTF-fähig ist, muss nur die **PR_RTF_COMPRESSED** -Eigenschaft festgelegt werden. 
  
 **Um PR_RTF_COMPRESSED festzulegen und sicherzustellen, dass der Synchronisierungsprozess bei Bedarf erfolgt, werden RTF-fähige Clients**
  
1. Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode auf, um die **PR_RTF_COMPRESSED** -Eigenschaft zu öffnen und sowohl die MAPI_CREATE-als auch die MAPI_MODIFY-Flags festzulegen. MAPI_CREATE stellt sicher, dass alle neuen Daten alle alten Daten ersetzen, und MAPI_MODIFY ermöglicht es Ihnen, diese Ersetzungen vorzunehmen. 
    
2. Rufen Sie die [WrapCompressedRTFStream](wrapcompressedrtfstream.md) -Funktion auf, und übergeben Sie STORE_UNCOMPRESSED_RTF, wenn der Nachrichtenspeicher das STORE_UNCOMPRESSED_RTF-Bit in seiner **PR_STORE_SUPPORT_MASK** -Eigenschaft festlegt, um eine nicht komprimierte Version des PR_RTF_COMPRESSED zu erhalten. ** **von OpenProperty **** zurückgegebener Stream.
    
3. Schreiben Sie die Nachrichten Textdaten in den unkomprimierten Stream, der von **WrapCompressedRTFStream**zurückgegeben wird.
    
4. Commit und Freigeben der unkomprimierten und komprimierten Streams.
    
Wenn der Nachrichtenspeicher Anbieter RTF unterstützt, haben Sie jetzt alle erforderlichen Schritte ausgeführt. Sie können den Synchronisierungsprozess und die Erstellung der **PR_BODY** -Eigenschaft, falls erforderlich, vom Nachrichtenspeicher Anbieter abhängig zu behandeln. Wenn der Nachrichtenspeicher Anbieter jedoch RTF nicht unterstützt, müssen Sie die [RTFSync](rtfsync.md) -Funktion aufrufen, um den Text mit der Formatierung zu synchronisieren, indem Sie das RTF_SYNC_RTF_CHANGED-Flag festlegen. 
  

