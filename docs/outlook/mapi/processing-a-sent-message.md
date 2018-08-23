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
ms.openlocfilehash: bd86e5d06e868ebc540d8eb779c059089045cd8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574181"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="54dff-103">Verarbeiten einer gesendeten Nachricht</span><span class="sxs-lookup"><span data-stu-id="54dff-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="54dff-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54dff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54dff-105">Ausgehende Nachrichten, nachdem sie gesendet wurden, kann im Postausgang bleiben gesendete Nachrichten-Ordner, in einen Ordner gehalten festgelegte verschoben oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="54dff-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="54dff-106">Die Art der Verarbeitung hängt davon ab, unabhängig davon, ob Sie die Nachricht Speichereigenschaften festgelegt haben:</span><span class="sxs-lookup"><span data-stu-id="54dff-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="54dff-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54dff-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="54dff-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54dff-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="54dff-109">**PR_DELETE_AFTER_SUBMIT** ist eine boolesche Eigenschaft, die andernfalls true zurück, wenn Nachrichten gelöscht werden soll, nachdem sie gesendet werden, und FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="54dff-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="54dff-110">**PR_SENTMAIL_ENTRYID** ist die Eintrags-ID eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="54dff-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="54dff-111">Wenn diese Eigenschaft festgelegt ist, sollten Sie gesendete Nachrichten in den Ordner, die von diesem Eintrag Bezeichner dargestellte verschieben.</span><span class="sxs-lookup"><span data-stu-id="54dff-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="54dff-112">Die gespeicherten Nachrichten in der Regel haben die Identität des letzten Nachrichtenspeichers oder transport-Anbieter dies veranlassen.</span><span class="sxs-lookup"><span data-stu-id="54dff-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="54dff-113">Entweder der anderen, oder keine dieser Eigenschaften sollte Set, jedoch nicht beide.</span><span class="sxs-lookup"><span data-stu-id="54dff-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="54dff-114">Wenn Sie **PR_SENTMAIL_ENTRYID**festlegen, muss es einen gültigen Eintrag Bezeichner enthalten.</span><span class="sxs-lookup"><span data-stu-id="54dff-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="54dff-115">In der folgenden Tabelle wird beschrieben, wie diese Eigenschaften auswirken, was Sie mit gesendete Nachrichten machen.</span><span class="sxs-lookup"><span data-stu-id="54dff-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54dff-116">Wenn weder-Eigenschaft festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="54dff-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="54dff-117">Lassen Sie die Nachricht in den Ordner, von dem sie (in der Regel im Ordner Postausgang) gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="54dff-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="54dff-118">Wenn **PR_SENTMAIL_ENTRYID** festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="54dff-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="54dff-119">Verschieben der Nachricht in den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="54dff-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="54dff-120">Wenn **PR_DELETE_AFTER_SUBMIT** festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="54dff-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="54dff-121">Löschen der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="54dff-121">Delete the message.</span></span>  <br/> |
   

