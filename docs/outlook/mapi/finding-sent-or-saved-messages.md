---
title: Suchen nach gesendeten oder gespeicherten Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 86373fae2753df66d4456cc0fc00f8b289977650
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437420"
---
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="539ed-103">Suchen nach gesendeten oder gespeicherten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="539ed-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="539ed-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="539ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="539ed-105">**So suchen Sie nach allen ausgehenden Nachrichten, die Sie gespeichert oder gesendet haben**</span><span class="sxs-lookup"><span data-stu-id="539ed-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="539ed-106">Rufen Sie [IMsgStore:: CompareEntryIDs](imsgstore-compareentryids.md) auf, um den Ordner mit den gesendeten Nachrichten mit dem Ordner zu vergleichen, der die eingehenden Nachrichten enthält.</span><span class="sxs-lookup"><span data-stu-id="539ed-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="539ed-107">Legen Sie den Parameter _lpEntryID1_ auf **PR_IPM_SENTMAIL_ENTRYID** ([pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md)) und den _LpEntryID2_ -Parameter fest, um auf **PR_PARENT_ENTRYID** ([pidtagparententryid (](pidtagparententryid-canonical-property.md)) zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="539ed-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="539ed-108">Beachten Sie, dass diese Strategie nicht funktioniert, wenn Sie Nachrichten entweder löschen, nachdem Sie gesendet wurden oder eine der gesendeten Nachrichten in einen anderen Ordner verschoben haben.</span><span class="sxs-lookup"><span data-stu-id="539ed-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="539ed-109">Wenn Sie bei der Untersuchung einer eingehenden Nachricht feststellen, dass die Eigenschaften, die normalerweise von einem Transportanbieter festgelegt werden, nicht vorhanden sind, können Sie davon ausgehen, dass die Nachricht nie von einem Transportanbieter behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="539ed-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="539ed-110">Zu diesen Eigenschaften zählen:</span><span class="sxs-lookup"><span data-stu-id="539ed-110">These properties include:</span></span>
  
- <span data-ttu-id="539ed-111">**PR_RECEIVED_BY** -Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="539ed-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="539ed-112">**PR_MESSAGE_DOWNLOAD_TIME** ([Pidtagmessagedownloadtime (](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="539ed-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="539ed-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([Pidtagtransportmessageheaders (](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="539ed-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="539ed-114">**PR_MESSAGE_TO_ME** ([Pidtagmessagetome (](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="539ed-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="539ed-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="539ed-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="539ed-116">**PR_MESSAGE_RECIP_ME** ([Pidtagmessagerecipientme (](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="539ed-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

