---
title: Tabellen für ausgehende Warteschlangen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348503"
---
# <a name="outgoing-queue-tables"></a>Tabellen für ausgehende Warteschlangen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Tabelle für ausgehende Warteschlangen enthält Informationen zu allen ausgehenden Nachrichten für einen Nachrichtenspeicher. Nachrichtenspeicher Anbieter implementieren ausgehende Warteschlangentabellen für die zu verwendende MAPI-Spooler. Speicher, die das Senden oder empfangen von Nachrichten nicht unterstützen, müssen diese Tabelle nicht implementieren. 
  
Um auf eine Tabelle für ausgehende Warteschlangen zuzugreifen, ruft der MAPI-Spooler die [IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md) -Methode auf. 
  
Es ist erforderlich, dass Nachrichten vorverarbeitet und an den Transportanbieter in der gleichen Reihenfolge übermittelt werden, in der Sie von der Clientanwendung gesendet wurden. Die MAPI-Spooler wurde entwickelt, um Nachrichten aus dem Nachrichtenspeicher in aufsteigender Reihenfolge der Übermittlungszeit zu akzeptieren. Aufgrund dieser Anforderung kann es einige Verzögerungen geben, bevor einige Nachrichten in der Tabelle für ausgehende Warteschlangen angezeigt werden. 
  
Nachrichtenspeicher sollten entweder die Sortierung in der Tabelle für ausgehende Warteschlangen zulassen, sodass der MAPI-Spooler die Nachrichten nach der Übermittlungszeit sortieren kann, oder die Standardsortierreihenfolge sollte von aufsteigender Übermittlungszeit sein. 
  
Die Tabelle für ausgehende Warteschlangen muss Benachrichtigungen senden, wenn sich der Inhalt der Warteschlange ändert.
  
Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in Tabellen für ausgehende Warteschlangen:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([Pidtagdisplaybcc (](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([Pidtagmessagesize (](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([Pidtagpriority (](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([Pidtagsubmitflags (](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Weitere Informationen zur Verwendung der Tabelle für ausgehende Warteschlangen finden Sie unter [Senden von Nachrichten mithilfe von Nachrichtenspeicher Anbietern](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

