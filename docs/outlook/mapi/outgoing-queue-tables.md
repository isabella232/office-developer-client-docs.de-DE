---
title: Tabellen für ausgehende Warteschlangen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d952047087fd550ca6f5e2826af5671bb23aece7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555930"
---
# <a name="outgoing-queue-tables"></a>Tabellen für ausgehende Warteschlangen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Tabelle mit ausgehenden Warteschlangen enthält Informationen zu allen ausgehenden Nachrichten für einen Nachrichtenspeicher. Nachrichtenspeicheranbieter implementieren ausgehende Warteschlangentabellen für den MAPI-Spooler, der verwendet werden soll. Speicher, die das Senden oder Empfangen von Nachrichten nicht unterstützen, müssen diese Tabelle nicht implementieren. 
  
Um auf eine Tabelle mit ausgehenden Warteschleifen zuzugreifen, ruft der MAPI-Spooler die [IMsgStore::GetOutgoingQueue-Methode](imsgstore-getoutgoingqueue.md) auf. 
  
Es ist erforderlich, dass Nachrichten in derselben Reihenfolge vorverarbeitet und an den Transportanbieter übermittelt werden, in der sie von der Clientanwendung gesendet wurden. Der MAPI-Spooler ist so konzipiert, dass Nachrichten aus dem Nachrichtenspeicher in aufsteigender Reihenfolge der Übermittlungszeit akzeptiert werden. Aufgrund dieser Anforderung kann es einige Verzögerungen geben, bevor einige Nachrichten in der Tabelle der ausgehenden Warteschlange angezeigt werden. 
  
Nachrichtenspeicher sollten entweder die Sortierung in der Tabelle der ausgehenden Warteschlange zulassen, damit der MAPI-Spooler die Nachrichten nach Übermittlungszeit sortieren kann, oder die Standardsortierreihenfolge sollte nach aufsteigender Übermittlungszeit erfolgen. 
  
Die Tabelle für ausgehende Warteschlangen muss Benachrichtigungen senden, wenn sich der Inhalt der Warteschlange ändert.
  
Die folgenden Eigenschaften bilden die erforderliche Spalte, die in ausgehenden Warteschlangentabellen festgelegt ist:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Weitere Informationen zur Verwendung der Tabelle für ausgehende Warteschlangen finden Sie unter [Senden von Nachrichten mithilfe von Nachrichten Store Anbietern.](sending-messages-by-using-message-store-providers.md)
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

