---
title: Verarbeiten einer gesendeten Nachricht
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0cea1a1008ecbff698b757d6c67af5c279954656
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795300"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="1354c-103">Verarbeiten einer gesendeten Nachricht</span><span class="sxs-lookup"><span data-stu-id="1354c-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="1354c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1354c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1354c-105">Ausgehende Nachrichten, nachdem sie gesendet wurden, kann im Postausgang bleiben gesendete Nachrichten-Ordner, in einen Ordner gehalten festgelegte verschoben oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1354c-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="1354c-106">Die Art der Verarbeitung hängt davon ab, unabhängig davon, ob Sie die Nachricht Speichereigenschaften festgelegt haben:</span><span class="sxs-lookup"><span data-stu-id="1354c-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="1354c-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1354c-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="1354c-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1354c-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="1354c-109">**PR_DELETE_AFTER_SUBMIT** ist eine boolesche Eigenschaft, die andernfalls true zurück, wenn Nachrichten gelöscht werden soll, nachdem sie gesendet werden, und FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1354c-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="1354c-110">**PR_SENTMAIL_ENTRYID** ist die Eintrags-ID eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="1354c-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="1354c-111">Wenn diese Eigenschaft festgelegt ist, sollten Sie gesendete Nachrichten in den Ordner, die von diesem Eintrag Bezeichner dargestellte verschieben.</span><span class="sxs-lookup"><span data-stu-id="1354c-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="1354c-112">Die gespeicherten Nachrichten in der Regel haben die Identität des letzten Nachrichtenspeichers oder transport-Anbieter dies veranlassen.</span><span class="sxs-lookup"><span data-stu-id="1354c-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="1354c-113">Entweder der anderen, oder keine dieser Eigenschaften sollte Set, jedoch nicht beide.</span><span class="sxs-lookup"><span data-stu-id="1354c-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="1354c-114">Wenn Sie **PR_SENTMAIL_ENTRYID**festlegen, muss es einen gültigen Eintrag Bezeichner enthalten.</span><span class="sxs-lookup"><span data-stu-id="1354c-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="1354c-115">In der folgenden Tabelle wird beschrieben, wie diese Eigenschaften auswirken, was Sie mit gesendete Nachrichten machen.</span><span class="sxs-lookup"><span data-stu-id="1354c-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1354c-116">Wenn weder-Eigenschaft festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="1354c-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="1354c-117">Lassen Sie die Nachricht in den Ordner, von dem sie (in der Regel im Ordner Postausgang) gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1354c-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="1354c-118">Wenn **PR_SENTMAIL_ENTRYID** festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="1354c-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="1354c-119">Verschieben der Nachricht in den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="1354c-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="1354c-120">Wenn **PR_DELETE_AFTER_SUBMIT** festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="1354c-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="1354c-121">Löschen der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1354c-121">Delete the message.</span></span>  <br/> |
   

