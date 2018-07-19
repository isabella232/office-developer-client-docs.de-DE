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
ms.openlocfilehash: 6e8b618e477475e8e7f45c266791086af63d8bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791695"
---
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="f257e-103">Suchen nach gesendeten oder gespeicherten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="f257e-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="f257e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f257e-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="f257e-105">**Um alle ausgehenden Nachrichten zu suchen, die Sie gespeichert oder gesendet**</span><span class="sxs-lookup"><span data-stu-id="f257e-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="f257e-106">Rufen Sie [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) , um den Ordner zu vergleichen, der Ihre gesendeten Nachrichten mit den Ordner enthält, die Ihre eingehenden Nachrichten enthält.</span><span class="sxs-lookup"><span data-stu-id="f257e-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="f257e-107">Legen Sie den Parameter _lpEntryID1_ So zeigen Sie auf **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) und _lpEntryID2_ **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) auf.</span><span class="sxs-lookup"><span data-stu-id="f257e-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="f257e-108">Beachten Sie, dass Sie entweder Nachrichten löschen, nachdem sie gesendet oder eine der gesendeten Nachrichten in einen anderen Ordner verschoben haben, diese Strategie nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="f257e-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="f257e-109">Wenn Sie sich bei der Prüfung einer eingehenden Nachricht feststellen, dass die Eigenschaften, die normalerweise von einem Transportanbieter festgelegt sind nicht vorhanden sind, können Sie davon ausgehen, dass die Nachricht von einem Transportanbieter nie behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="f257e-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="f257e-110">Diese Eigenschaften umfassen:</span><span class="sxs-lookup"><span data-stu-id="f257e-110">These properties include:</span></span>
  
- <span data-ttu-id="f257e-111">**PR_RECEIVED_BY** -Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f257e-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="f257e-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f257e-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="f257e-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f257e-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="f257e-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f257e-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="f257e-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f257e-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="f257e-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f257e-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

