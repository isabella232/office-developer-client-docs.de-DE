---
title: Tabellen für ausgehende Warteschlange
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 10890c1fe430ddbc45c16908df3ac340284c9f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793321"
---
# <a name="outgoing-queue-tables"></a>Tabellen für ausgehende Warteschlange

  
  
**Betrifft**: Outlook 
  
Eine ausgehende Warteschlangentabelle enthält Informationen zu allen ausgehenden Nachrichten für einen Nachrichtenspeicher. Nachricht Anbieter implementieren ausgehende Warteschlange Tabellen für die MAPI-Warteschlange verwendet. Speicher, die nicht das Senden oder Empfangen von Nachrichten muss in dieser Tabelle nicht implementieren. 
  
Die MAPI-Warteschlange die [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) -Methode aufgerufen, um eine ausgehende Warteschlangentabelle zuzugreifen. 
  
Es ist eine Voraussetzung, dass Nachrichten vorverarbeitet und an der Adressbuchhierarchie in der gleichen Reihenfolge übermittelt werden, wie sie von der Clientanwendung gesendet wurden. Die MAPI-Warteschlange dient zum Akzeptieren von Nachrichten aus dem Nachrichtenspeicher in aufsteigender Reihenfolge der Zeitpunkt der Übermittlung. Aufgrund dieser Anforderung kann es einige Zeit dauern bevor einige Nachrichten in der ausgehenden Warteschlangentabelle angezeigt werden. 
  
Nachrichtenspeicher sollte entweder zulassen, damit die MAPI-Warteschlange der Nachrichten vom Zeitpunkt der Übermittlung sortieren oder die Sortierreihenfolge werden sollte, aufsteigend Zeitpunkt der Übermittlung der ausgehenden Warteschlangentabelle sortieren. 
  
Die ausgehende Warteschlangentabelle muss Benachrichtigungen senden, wenn der Inhalt der Warteschlange geändert wird.
  
Die folgenden Eigenschaften bilden die erforderliche Spalte in ausgehenden Warteschlange Tabellen festzulegen:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Weitere Informationen darüber, wie die ausgehende Warteschlangentabelle verwendet wird finden Sie unter [Nachrichten Zeichenfolgeneigenschaften verwenden Nachricht senden](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

