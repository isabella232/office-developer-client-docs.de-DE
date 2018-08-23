---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 379fdc47f35fb183dd0bf551e421422abb106c0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591010"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="99e47-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="99e47-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="99e47-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99e47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99e47-105">Schließt eine Nachricht Empfängerliste bestimmten Verteilerlisten erweitern.</span><span class="sxs-lookup"><span data-stu-id="99e47-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="99e47-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99e47-106">Parameters</span></span>

 <span data-ttu-id="99e47-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="99e47-107">_lpMessage_</span></span>
  
> <span data-ttu-id="99e47-108">[in] Ein Zeiger auf die Nachricht mit der Empfängerliste verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="99e47-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="99e47-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="99e47-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="99e47-110">[out] Ein Zeiger auf eine Bitmaske aus Flags, die den Typ der Verarbeitung steuert, das auftritt.</span><span class="sxs-lookup"><span data-stu-id="99e47-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="99e47-111">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="99e47-111">The following flags can be set:</span></span>
    
<span data-ttu-id="99e47-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="99e47-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="99e47-113">Die Nachricht muss vorverarbeitet werden, bevor es gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="99e47-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="99e47-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="99e47-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="99e47-115">Die MAPI-Warteschlange (anstelle der Adressbuchhierarchie, dem der Aufrufer eng verknüpft ist) muss die Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="99e47-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99e47-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="99e47-116">Return value</span></span>

<span data-ttu-id="99e47-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="99e47-117">S_OK</span></span> 
  
> <span data-ttu-id="99e47-118">Liste der Empfänger die Nachricht wurde erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="99e47-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99e47-119">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="99e47-119">Remarks</span></span>

<span data-ttu-id="99e47-120">Die **IMAPISupport::ExpandRecips** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="99e47-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="99e47-121">Nachricht Anbieter Aufrufen **ExpandRecips** um auffordern, MAPI, um die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="99e47-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="99e47-122">Erweitern Sie bestimmte persönlichen Verteilerlisten, an die Empfänger der Komponente.</span><span class="sxs-lookup"><span data-stu-id="99e47-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="99e47-123">Ersetzen Sie alle Anzeigenamen, die geändert wurden mit den ursprünglichen Namen.</span><span class="sxs-lookup"><span data-stu-id="99e47-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="99e47-124">Doppelte Einträge zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="99e47-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="99e47-125">Alle einmalige-Adressen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="99e47-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="99e47-126">Überprüfen Sie, ob die Nachricht vorverarbeitung benötigt, und wenn dies der Fall ist, legen Sie das Flag auf _LpulFlags_ auf NEEDS_PREPROCESSING zeigt.</span><span class="sxs-lookup"><span data-stu-id="99e47-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="99e47-127">**ExpandRecips** erweitert alle Verteilerlisten, die den messaging Adresstyp MAPIPDL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="99e47-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="99e47-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="99e47-128">Notes to callers</span></span>

<span data-ttu-id="99e47-129">Rufen Sie immer **ExpandRecips** als Teil der Verarbeitung von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="99e47-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="99e47-130">Rufen Sie **ExpandRecips** eine der ersten Aufrufe in der Implementierung der [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="99e47-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99e47-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99e47-131">See also</span></span>



[<span data-ttu-id="99e47-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="99e47-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="99e47-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="99e47-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

