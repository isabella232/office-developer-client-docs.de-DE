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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348762"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="6a9de-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="6a9de-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="6a9de-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a9de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a9de-105">Ermöglicht dem Nachrichtenspeicher Anbieter das Ausführen der Verarbeitung für eine gesendete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6a9de-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="6a9de-106">Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6a9de-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="6a9de-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a9de-107">Parameters</span></span>

 <span data-ttu-id="6a9de-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6a9de-108">_ulFlags_</span></span>
  
> <span data-ttu-id="6a9de-109">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="6a9de-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6a9de-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6a9de-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="6a9de-111">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6a9de-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6a9de-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6a9de-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="6a9de-113">in Ein Zeiger auf die Eintrags-ID der zu verarbeitenden Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6a9de-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a9de-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a9de-114">Return value</span></span>

<span data-ttu-id="6a9de-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a9de-115">S_OK</span></span> 
  
> <span data-ttu-id="6a9de-116">Die Verarbeitung der gesendeten Nachricht war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6a9de-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="6a9de-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6a9de-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6a9de-118">Der Nachrichtenspeicher Anbieter unterstützt keine gesendete Nachrichtenverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="6a9de-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="6a9de-119">Dieser Fehlerwert wird zurückgegeben, wenn der Aufrufer nicht der MAPI-Spooler ist.</span><span class="sxs-lookup"><span data-stu-id="6a9de-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a9de-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a9de-120">Remarks</span></span>

<span data-ttu-id="6a9de-121">Die **IMsgStore:: FinishedMsg** -Methode führt eine Verarbeitung für eine gesendete Nachricht aus.</span><span class="sxs-lookup"><span data-stu-id="6a9de-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="6a9de-122">Bei dieser Verarbeitung kann es sich um das Löschen der Nachricht, die Verschiebung in einen anderen Ordner oder um beide Aktionen handeln.</span><span class="sxs-lookup"><span data-stu-id="6a9de-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="6a9de-123">Die Art der Verarbeitung hängt davon ab, ob die Eigenschaften **PR_DELETE_AFTER_SUBMIT** ([Pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md)) und **PR_SENTMAIL_ENTRYID** ([pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md)) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="6a9de-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6a9de-124">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="6a9de-124">Notes to implementers</span></span>

<span data-ttu-id="6a9de-125">Entsperren Sie in ihrer Implementierung von **FinishedMsg**die Nachricht, die von _lpEntryID_ identifiziert wurde, und führen Sie die entsprechende Verarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="6a9de-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="6a9de-126">Die Zielnachricht ist immer gesperrt; der MAPI-Spooler übergibt nie den Eintragsbezeichner für eine nicht gesperrte Nachricht an **FinishedMsg**.</span><span class="sxs-lookup"><span data-stu-id="6a9de-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="6a9de-127">Es ist möglich, dass weder **PR_DELETE_AFTER_SUBMIT** noch **PR_SENTMAIL_ENTRYID** festgelegt ist, beides festgelegt ist oder die andere festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6a9de-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="6a9de-128">In der folgenden Tabelle wird die Aktion beschrieben, die Sie auf der Grundlage der Einstellungen ergreifen sollten:</span><span class="sxs-lookup"><span data-stu-id="6a9de-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a9de-129">Wenn keine Eigenschaft festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="6a9de-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="6a9de-130">BeLassen Sie die Nachricht in dem Ordner, von dem Sie gesendet wurde (in der Regel der Postausgang).</span><span class="sxs-lookup"><span data-stu-id="6a9de-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="6a9de-131">Wenn beide Eigenschaften festgelegt sind:</span><span class="sxs-lookup"><span data-stu-id="6a9de-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="6a9de-132">Verschieben Sie die Nachricht, falls gewünscht, in den angegebenen Ordner, und löschen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="6a9de-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="6a9de-133">Wenn PR_SENTMAIL_ENTRYID festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="6a9de-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="6a9de-134">Verschieben Sie die Nachricht in den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="6a9de-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="6a9de-135">Wenn PR_DELETE_AFTER_SUBMIT festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="6a9de-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="6a9de-136">Löschen Sie die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6a9de-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="6a9de-137">Wenn Sie alle geeigneten Aktionen ausgeführt haben, rufen Sie die [IMAPISupport::D osentmail](imapisupport-dosentmail.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="6a9de-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a9de-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a9de-138">See also</span></span>



[<span data-ttu-id="6a9de-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="6a9de-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="6a9de-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6a9de-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

