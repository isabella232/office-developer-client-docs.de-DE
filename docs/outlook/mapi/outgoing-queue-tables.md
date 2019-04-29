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
# <a name="outgoing-queue-tables"></a><span data-ttu-id="6a6a0-103">Tabellen für ausgehende Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="6a6a0-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="6a6a0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a6a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a6a0-105">Eine Tabelle für ausgehende Warteschlangen enthält Informationen zu allen ausgehenden Nachrichten für einen Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="6a6a0-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="6a6a0-106">Nachrichtenspeicher Anbieter implementieren ausgehende Warteschlangentabellen für die zu verwendende MAPI-Spooler.</span><span class="sxs-lookup"><span data-stu-id="6a6a0-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="6a6a0-107">Speicher, die das Senden oder empfangen von Nachrichten nicht unterstützen, müssen diese Tabelle nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="6a6a0-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="6a6a0-108">Um auf eine Tabelle für ausgehende Warteschlangen zuzugreifen, ruft der MAPI-Spooler die [IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="6a6a0-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="6a6a0-109">Es ist erforderlich, dass Nachrichten vorverarbeitet und an den Transportanbieter in der gleichen Reihenfolge übermittelt werden, in der Sie von der Clientanwendung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="6a6a0-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="6a6a0-110">Die MAPI-Spooler wurde entwickelt, um Nachrichten aus dem Nachrichtenspeicher in aufsteigender Reihenfolge der Übermittlungszeit zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="6a6a0-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="6a6a0-111">Aufgrund dieser Anforderung kann es einige Verzögerungen geben, bevor einige Nachrichten in der Tabelle für ausgehende Warteschlangen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6a6a0-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="6a6a0-112">Nachrichtenspeicher sollten entweder die Sortierung in der Tabelle für ausgehende Warteschlangen zulassen, sodass der MAPI-Spooler die Nachrichten nach der Übermittlungszeit sortieren kann, oder die Standardsortierreihenfolge sollte von aufsteigender Übermittlungszeit sein.</span><span class="sxs-lookup"><span data-stu-id="6a6a0-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="6a6a0-113">Die Tabelle für ausgehende Warteschlangen muss Benachrichtigungen senden, wenn sich der Inhalt der Warteschlange ändert.</span><span class="sxs-lookup"><span data-stu-id="6a6a0-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="6a6a0-114">Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in Tabellen für ausgehende Warteschlangen:</span><span class="sxs-lookup"><span data-stu-id="6a6a0-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a6a0-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6a6a0-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6a6a0-116">**PR_DISPLAY_BCC** ([Pidtagdisplaybcc (](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6a6a0-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="6a6a0-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6a6a0-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6a6a0-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6a6a0-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="6a6a0-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6a6a0-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6a6a0-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6a6a0-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="6a6a0-121">**PR_MESSAGE_SIZE** ([Pidtagmessagesize (](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6a6a0-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6a6a0-122">**PR_PRIORITY** ([Pidtagpriority (](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6a6a0-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="6a6a0-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6a6a0-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6a6a0-124">**PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6a6a0-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="6a6a0-125">**PR_SUBMIT_FLAGS** ([Pidtagsubmitflags (](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6a6a0-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="6a6a0-126">Weitere Informationen zur Verwendung der Tabelle für ausgehende Warteschlangen finden Sie unter [Senden von Nachrichten mithilfe von Nachrichtenspeicher Anbietern](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="6a6a0-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a6a0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a6a0-127">See also</span></span>



[<span data-ttu-id="6a6a0-128">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="6a6a0-128">MAPI Tables</span></span>](mapi-tables.md)

