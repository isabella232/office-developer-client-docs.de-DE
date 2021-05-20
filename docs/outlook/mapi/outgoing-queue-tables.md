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
# <a name="outgoing-queue-tables"></a><span data-ttu-id="eb95f-103">Tabellen für ausgehende Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="eb95f-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="eb95f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb95f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb95f-105">Eine Tabelle für ausgehende Warteschlangen enthält Informationen zu allen ausgehenden Nachrichten für einen Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="eb95f-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="eb95f-106">Nachrichtenspeicheranbieter implementieren ausgehende Warteschlangentabellen für den zu verwendenden MAPI-Spooler.</span><span class="sxs-lookup"><span data-stu-id="eb95f-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="eb95f-107">Speicher, die das Senden oder Empfangen von Nachrichten nicht unterstützen, müssen diese Tabelle nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="eb95f-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="eb95f-108">Für den Zugriff auf eine ausgehende Warteschlangentabelle ruft der MAPI-Spooler die [IMsgStore::GetOutgoingQueue-Methode](imsgstore-getoutgoingqueue.md) auf.</span><span class="sxs-lookup"><span data-stu-id="eb95f-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="eb95f-109">Es ist erforderlich, dass Nachrichten in der gleichen Reihenfolge vorverarbeitet und an den Transportanbieter übermittelt werden, wie sie von der Clientanwendung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="eb95f-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="eb95f-110">Der MAPI-Spooler wurde entwickelt, um Nachrichten aus dem Nachrichtenspeicher in aufsteigender Reihenfolge der Übermittlungszeit zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="eb95f-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="eb95f-111">Aufgrund dieser Anforderung kann es zu verzögerungen kommen, bevor einige Nachrichten in der Tabelle für ausgehende Warteschlangen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="eb95f-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="eb95f-112">Nachrichtenspeicher sollten entweder die Sortierung in der ausgehenden Warteschlangentabelle zulassen, damit der MAPI-Spooler die Nachrichten nach Übermittlungszeit sortieren kann, oder die Standardsortierreihenfolge sollte durch aufsteigende Übermittlungszeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="eb95f-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="eb95f-113">Die Tabelle für ausgehende Warteschlangen muss Benachrichtigungen senden, wenn sich der Inhalt der Warteschlange ändert.</span><span class="sxs-lookup"><span data-stu-id="eb95f-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="eb95f-114">Die folgenden Eigenschaften stellen den erforderlichen Spaltensatz in ausgehenden Warteschlangentabellen zusammen:</span><span class="sxs-lookup"><span data-stu-id="eb95f-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb95f-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eb95f-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eb95f-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eb95f-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="eb95f-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eb95f-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eb95f-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eb95f-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="eb95f-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eb95f-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eb95f-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eb95f-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="eb95f-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eb95f-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eb95f-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eb95f-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="eb95f-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eb95f-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eb95f-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eb95f-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="eb95f-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eb95f-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="eb95f-126">Weitere Informationen zur Verwendung der Tabelle für ausgehende Warteschlangen finden Sie unter [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="eb95f-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb95f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb95f-127">See also</span></span>



[<span data-ttu-id="eb95f-128">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="eb95f-128">MAPI Tables</span></span>](mapi-tables.md)

