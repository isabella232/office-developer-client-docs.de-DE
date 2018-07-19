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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2bded946a1fc7d7ab181d3953defa24e247c003c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792379"
---
# <a name="imapisupportdosentmail"></a><span data-ttu-id="b0b34-103">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="b0b34-103">IMAPISupport::DoSentMail</span></span>

  
  
<span data-ttu-id="b0b34-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0b34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0b34-105">Verarbeitet eine gesendete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b0b34-105">Processes a sent message.</span></span>
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="b0b34-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0b34-106">Parameters</span></span>

 <span data-ttu-id="b0b34-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b0b34-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b0b34-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="b0b34-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b0b34-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="b0b34-109">_lpMessage_</span></span>
  
> <span data-ttu-id="b0b34-110">[in] Ein Zeiger auf die ge�ffneten Nachricht f�r die eine Nachricht im Ordner speichern gesendete Elemente vorgesehen generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0b34-110">[in] A pointer to the open message for which a message should be generated in the folder designated to hold sent items.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b0b34-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0b34-111">Return value</span></span>

<span data-ttu-id="b0b34-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0b34-112">S_OK</span></span> 
  
> <span data-ttu-id="b0b34-113">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b0b34-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0b34-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0b34-114">Remarks</span></span>

<span data-ttu-id="b0b34-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span><span class="sxs-lookup"><span data-stu-id="b0b34-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span></span>
  
 <span data-ttu-id="b0b34-118">**DoSentMail** f�hrt die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="b0b34-118">**DoSentMail** performs the following tasks:</span></span> 
  
- <span data-ttu-id="b0b34-119">Überprüft die Nachricht für die **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft, um festzustellen, ob die Nachricht nach dem Senden gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0b34-119">Checks the message for the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to determine whether the message should be deleted after sending.</span></span>
    
- <span data-ttu-id="b0b34-120">Bestimmt den Speicherort des Ordners "Gesendete Elemente".</span><span class="sxs-lookup"><span data-stu-id="b0b34-120">Determines the location of the Sent Items folder.</span></span>
    
- <span data-ttu-id="b0b34-121">Initiiert die Nachricht Hook Verarbeitung f�r alle Hook auf den Ordner Gesendete Objekte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0b34-121">Initiates message hook processing for any hooks set on the Sent Items folder.</span></span>
    
- <span data-ttu-id="b0b34-122">Verschiebt die Nachricht im Ordner Gesendete Elemente, Ordner Gel�schte Objekte, oder in einen anderen Ordner.</span><span class="sxs-lookup"><span data-stu-id="b0b34-122">Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.</span></span>
    
- <span data-ttu-id="b0b34-123">Gibt die Nachricht frei.</span><span class="sxs-lookup"><span data-stu-id="b0b34-123">Releases the message.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0b34-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0b34-124">See also</span></span>



[<span data-ttu-id="b0b34-125">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="b0b34-125">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="b0b34-126">Kanonische PidTagDeleteAfterSubmit-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b0b34-126">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)
  
[<span data-ttu-id="b0b34-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0b34-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

