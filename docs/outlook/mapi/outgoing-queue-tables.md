---
title: Tabellen für ausgehende Warteschlange
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c5f136a0d26b7519bc1b7b3d8f448f5f382767ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591254"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="debb6-103">Tabellen für ausgehende Warteschlange</span><span class="sxs-lookup"><span data-stu-id="debb6-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="debb6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="debb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="debb6-105">Eine ausgehende Warteschlangentabelle enthält Informationen zu allen ausgehenden Nachrichten für einen Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="debb6-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="debb6-106">Nachricht Anbieter implementieren ausgehende Warteschlange Tabellen für die MAPI-Warteschlange verwendet.</span><span class="sxs-lookup"><span data-stu-id="debb6-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="debb6-107">Speicher, die nicht das Senden oder Empfangen von Nachrichten muss in dieser Tabelle nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="debb6-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="debb6-108">Die MAPI-Warteschlange die [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) -Methode aufgerufen, um eine ausgehende Warteschlangentabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="debb6-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="debb6-109">Es ist eine Voraussetzung, dass Nachrichten vorverarbeitet und an der Adressbuchhierarchie in der gleichen Reihenfolge übermittelt werden, wie sie von der Clientanwendung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="debb6-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="debb6-110">Die MAPI-Warteschlange dient zum Akzeptieren von Nachrichten aus dem Nachrichtenspeicher in aufsteigender Reihenfolge der Zeitpunkt der Übermittlung.</span><span class="sxs-lookup"><span data-stu-id="debb6-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="debb6-111">Aufgrund dieser Anforderung kann es einige Zeit dauern bevor einige Nachrichten in der ausgehenden Warteschlangentabelle angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="debb6-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="debb6-112">Nachrichtenspeicher sollte entweder zulassen, damit die MAPI-Warteschlange der Nachrichten vom Zeitpunkt der Übermittlung sortieren oder die Sortierreihenfolge werden sollte, aufsteigend Zeitpunkt der Übermittlung der ausgehenden Warteschlangentabelle sortieren.</span><span class="sxs-lookup"><span data-stu-id="debb6-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="debb6-113">Die ausgehende Warteschlangentabelle muss Benachrichtigungen senden, wenn der Inhalt der Warteschlange geändert wird.</span><span class="sxs-lookup"><span data-stu-id="debb6-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="debb6-114">Die folgenden Eigenschaften bilden die erforderliche Spalte in ausgehenden Warteschlange Tabellen festzulegen:</span><span class="sxs-lookup"><span data-stu-id="debb6-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="debb6-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="debb6-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="debb6-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="debb6-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="debb6-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="debb6-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="debb6-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="debb6-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="debb6-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="debb6-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="debb6-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="debb6-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="debb6-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="debb6-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="debb6-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="debb6-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="debb6-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="debb6-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="debb6-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="debb6-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="debb6-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="debb6-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="debb6-126">Weitere Informationen darüber, wie die ausgehende Warteschlangentabelle verwendet wird finden Sie unter [Nachrichten Zeichenfolgeneigenschaften verwenden Nachricht senden](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="debb6-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="debb6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="debb6-127">See also</span></span>



[<span data-ttu-id="debb6-128">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="debb6-128">MAPI Tables</span></span>](mapi-tables.md)

