---
title: Tabellen für ausgehende Warteschlangen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437574"
---
# <a name="outgoing-queue-tables"></a>Tabellen für ausgehende Warteschlangen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Tabelle für ausgehende Warteschlangen enthält Informationen zu allen ausgehenden Nachrichten für einen Nachrichtenspeicher. Nachrichtenspeicheranbieter implementieren ausgehende Warteschlangentabellen für den zu verwendenden MAPI-Spooler. Speicher, die das Senden oder Empfangen von Nachrichten nicht unterstützen, müssen diese Tabelle nicht implementieren. 
  
Für den Zugriff auf eine ausgehende Warteschlangentabelle ruft der MAPI-Spooler die [IMsgStore::GetOutgoingQueue-Methode](imsgstore-getoutgoingqueue.md) auf. 
  
Es ist erforderlich, dass Nachrichten in der gleichen Reihenfolge vorverarbeitet und an den Transportanbieter übermittelt werden, wie sie von der Clientanwendung gesendet wurden. Der MAPI-Spooler wurde entwickelt, um Nachrichten aus dem Nachrichtenspeicher in aufsteigender Reihenfolge der Übermittlungszeit zu akzeptieren. Aufgrund dieser Anforderung kann es zu verzögerungen kommen, bevor einige Nachrichten in der Tabelle für ausgehende Warteschlangen angezeigt werden. 
  
Nachrichtenspeicher sollten entweder die Sortierung in der ausgehenden Warteschlangentabelle zulassen, damit der MAPI-Spooler die Nachrichten nach Übermittlungszeit sortieren kann, oder die Standardsortierreihenfolge sollte durch aufsteigende Übermittlungszeit festgelegt werden. 
  
Die Tabelle für ausgehende Warteschlangen muss Benachrichtigungen senden, wenn sich der Inhalt der Warteschlange ändert.
  
Die folgenden Eigenschaften stellen den erforderlichen Spaltensatz in ausgehenden Warteschlangentabellen zusammen:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Weitere Informationen zur Verwendung der Tabelle für ausgehende Warteschlangen finden Sie unter [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

