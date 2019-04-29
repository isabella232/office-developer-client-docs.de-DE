---
title: Verarbeiten einer gesendeten Nachricht
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434676"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="3a34d-103">Verarbeiten einer gesendeten Nachricht</span><span class="sxs-lookup"><span data-stu-id="3a34d-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="3a34d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a34d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a34d-105">Ausgehende Nachrichten können, nachdem Sie gesendet wurden, im Ordner Postausgang hinterlassen, in einen Ordner verschoben werden, der für gesendete Nachrichten reserviert oder gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="3a34d-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="3a34d-106">Die Art der Verarbeitung hängt davon ab, ob Sie die Eigenschaften für den Nachrichtenspeicher festgelegt haben:</span><span class="sxs-lookup"><span data-stu-id="3a34d-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="3a34d-107">**PR_DELETE_AFTER_SUBMIT** ([Pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a34d-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="3a34d-108">**PR_SENTMAIL_ENTRYID** ([Pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a34d-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="3a34d-109">**PR_DELETE_AFTER_SUBMIT** ist eine boolesche Eigenschaft, die auf true festgelegt ist, wenn Nachrichten nach dem Senden gelöscht werden sollen, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="3a34d-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="3a34d-110">**PR_SENTMAIL_ENTRYID** ist die Eintrags-ID eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="3a34d-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="3a34d-111">Wenn diese Eigenschaft festgelegt ist, sollten Sie gesendete Nachrichten in den Ordner verschieben, der durch diese Eintrags-ID dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3a34d-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="3a34d-112">Die gespeicherten Nachrichten weisen in der Regel die Identität des letzten Nachrichtenspeichers oder Transportanbieters auf, um Sie zu senden.</span><span class="sxs-lookup"><span data-stu-id="3a34d-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="3a34d-113">Entweder die eine oder die andere oder keine dieser Eigenschaften sollte festgelegt werden, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="3a34d-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="3a34d-114">Wenn Sie jedoch **PR_SENTMAIL_ENTRYID**festlegen, muss es eine gültige Eintrags-ID enthalten.</span><span class="sxs-lookup"><span data-stu-id="3a34d-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="3a34d-115">In der folgenden Tabelle wird beschrieben, wie sich diese Eigenschaften auf das Verhalten von gesendeten Nachrichten auswirken.</span><span class="sxs-lookup"><span data-stu-id="3a34d-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a34d-116">Wenn keine Eigenschaft festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="3a34d-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="3a34d-117">BeLassen Sie die Nachricht in dem Ordner, von dem Sie gesendet wurde (in der Regel der Postausgang).</span><span class="sxs-lookup"><span data-stu-id="3a34d-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="3a34d-118">Wenn **PR_SENTMAIL_ENTRYID** festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="3a34d-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="3a34d-119">Verschieben Sie die Nachricht in den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="3a34d-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="3a34d-120">Wenn **PR_DELETE_AFTER_SUBMIT** festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="3a34d-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="3a34d-121">Löschen Sie die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3a34d-121">Delete the message.</span></span>  <br/> |
   

