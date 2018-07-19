---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9da9a13f87eac097fba078da1f1d6c3f78f69c0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792637"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="8b82c-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="8b82c-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="8b82c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8b82c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8b82c-105">Aktiviert den Nachricht-Speicher-Anbieter für die Verarbeitung für eine gesendete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8b82c-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="8b82c-106">Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8b82c-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="8b82c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b82c-107">Parameters</span></span>

 <span data-ttu-id="8b82c-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8b82c-108">_ulFlags_</span></span>
  
> <span data-ttu-id="8b82c-109">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="8b82c-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8b82c-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8b82c-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="8b82c-111">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="8b82c-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8b82c-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8b82c-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="8b82c-113">[in] Ein Zeiger auf die Eintrags-ID der Nachricht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8b82c-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8b82c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b82c-114">Return value</span></span>

<span data-ttu-id="8b82c-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b82c-115">S_OK</span></span> 
  
> <span data-ttu-id="8b82c-116">Verarbeitung für die gesendete Nachricht war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8b82c-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="8b82c-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8b82c-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8b82c-118">Die Nachrichtenanbieter unterstützt keine Verarbeitung von gesendeten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="8b82c-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="8b82c-119">Dieser Fehlerwert wird zurückgegeben, wenn der Aufrufer nicht die MAPI-Warteschlange befindet.</span><span class="sxs-lookup"><span data-stu-id="8b82c-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b82c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b82c-120">Remarks</span></span>

<span data-ttu-id="8b82c-121">Die **IMsgStore::FinishedMsg** -Methode führt die Verarbeitung für eine gesendete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8b82c-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="8b82c-122">Löschen der Nachricht in einem anderen Ordner oder beide Aktionen verschieben betreffen diese Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="8b82c-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="8b82c-123">Die Art der Verarbeitung hängt davon ab, ob die **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) und **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) Eigenschaften festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8b82c-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8b82c-124">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="8b82c-124">Notes to implementers</span></span>

<span data-ttu-id="8b82c-125">Entsperren Sie in der Implementierung der **FinishedMsg**die Nachricht vom _LpEntryID_ , und führen Sie die entsprechende Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="8b82c-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="8b82c-126">Die Zielnachricht wird immer gesperrt werden. die MAPI-Warteschlange übergibt die Eintrags-ID für eine nicht gesperrte Nachricht nie an **FinishedMsg**.</span><span class="sxs-lookup"><span data-stu-id="8b82c-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="8b82c-127">Es ist möglich, dass weder **PR_DELETE_AFTER_SUBMIT** oder **PR_SENTMAIL_ENTRYID** festgelegt ist, beide festgelegt werden oder mindestens eine der anderen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8b82c-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="8b82c-128">Die folgende Tabelle beschreibt die Aktion, die Sie basierend auf der Einstellungen ausgeführt werden soll:</span><span class="sxs-lookup"><span data-stu-id="8b82c-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b82c-129">Wenn weder-Eigenschaft festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="8b82c-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="8b82c-130">Lassen Sie die Nachricht in den Ordner, von dem sie (in der Regel im Ordner Postausgang) gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8b82c-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="8b82c-131">Wenn beide Eigenschaften festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8b82c-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="8b82c-132">Verschieben der Nachricht in den angegebenen Ordner, falls gewünscht, und löschen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="8b82c-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="8b82c-133">Wenn PR_SENTMAIL_ENTRYID festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="8b82c-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="8b82c-134">Verschieben der Nachricht in den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="8b82c-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="8b82c-135">Wenn PR_DELETE_AFTER_SUBMIT festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="8b82c-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="8b82c-136">Löschen der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8b82c-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="8b82c-137">Nachdem Sie die geeignete Aktion durchgeführt haben, rufen Sie die [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8b82c-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b82c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b82c-138">See also</span></span>



[<span data-ttu-id="8b82c-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="8b82c-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="8b82c-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8b82c-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

