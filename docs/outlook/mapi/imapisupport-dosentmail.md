---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8289b8dd2e0ab3c760e77a37b821d2fe74e4abe9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423951"
---
# <a name="imapisupportdosentmail"></a><span data-ttu-id="5c22d-103">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="5c22d-103">IMAPISupport::DoSentMail</span></span>

  
  
<span data-ttu-id="5c22d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c22d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c22d-105">Verarbeitet eine gesendete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5c22d-105">Processes a sent message.</span></span>
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="5c22d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c22d-106">Parameters</span></span>

 <span data-ttu-id="5c22d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5c22d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5c22d-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="5c22d-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5c22d-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="5c22d-109">_lpMessage_</span></span>
  
> <span data-ttu-id="5c22d-110">[in] Ein Zeiger auf die ge�ffneten Nachricht f�r die eine Nachricht im Ordner speichern gesendete Elemente vorgesehen generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c22d-110">[in] A pointer to the open message for which a message should be generated in the folder designated to hold sent items.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5c22d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c22d-111">Return value</span></span>

<span data-ttu-id="5c22d-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c22d-112">S_OK</span></span> 
  
> <span data-ttu-id="5c22d-113">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="5c22d-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5c22d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c22d-114">Remarks</span></span>

<span data-ttu-id="5c22d-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span><span class="sxs-lookup"><span data-stu-id="5c22d-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span></span>
  
 <span data-ttu-id="5c22d-118">**DoSentMail** f�hrt die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="5c22d-118">**DoSentMail** performs the following tasks:</span></span> 
  
- <span data-ttu-id="5c22d-119">Überprüft die Nachricht für die **PR_DELETE_AFTER_SUBMIT** ([pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft, um zu bestimmen, ob die Nachricht nach dem Senden gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c22d-119">Checks the message for the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to determine whether the message should be deleted after sending.</span></span>
    
- <span data-ttu-id="5c22d-120">Bestimmt den Speicherort des Ordners "Gesendete Elemente".</span><span class="sxs-lookup"><span data-stu-id="5c22d-120">Determines the location of the Sent Items folder.</span></span>
    
- <span data-ttu-id="5c22d-121">Initiiert die Nachricht Hook Verarbeitung f�r alle Hook auf den Ordner Gesendete Objekte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5c22d-121">Initiates message hook processing for any hooks set on the Sent Items folder.</span></span>
    
- <span data-ttu-id="5c22d-122">Verschiebt die Nachricht im Ordner Gesendete Elemente, Ordner Gel�schte Objekte, oder in einen anderen Ordner.</span><span class="sxs-lookup"><span data-stu-id="5c22d-122">Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.</span></span>
    
- <span data-ttu-id="5c22d-123">Gibt die Nachricht frei.</span><span class="sxs-lookup"><span data-stu-id="5c22d-123">Releases the message.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c22d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c22d-124">See also</span></span>



[<span data-ttu-id="5c22d-125">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="5c22d-125">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="5c22d-126">Kanonische PidTagDeleteAfterSubmit-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5c22d-126">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)
  
[<span data-ttu-id="5c22d-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c22d-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

