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
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411246"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="0e9cd-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="0e9cd-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="0e9cd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e9cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e9cd-105">Vervollständigt die Empfängerliste einer Nachricht und erweitert bestimmte Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0e9cd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e9cd-106">Parameters</span></span>

 <span data-ttu-id="0e9cd-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="0e9cd-107">_lpMessage_</span></span>
  
> <span data-ttu-id="0e9cd-108">in Ein Zeiger auf die Nachricht, die die Empfängerliste hat, die verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="0e9cd-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="0e9cd-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="0e9cd-110">Out Ein Zeiger auf eine Bitmaske von Flags, die die Art der Verarbeitung steuert.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="0e9cd-111">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0e9cd-111">The following flags can be set:</span></span>
    
<span data-ttu-id="0e9cd-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="0e9cd-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="0e9cd-113">Die Nachricht muss vorverarbeitet werden, bevor Sie gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="0e9cd-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="0e9cd-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="0e9cd-115">Die MAPI-Warteschlange (anstelle des Transportanbieters, an den der Aufrufer eng gekoppelt ist) muss die Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e9cd-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e9cd-116">Return value</span></span>

<span data-ttu-id="0e9cd-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e9cd-117">S_OK</span></span> 
  
> <span data-ttu-id="0e9cd-118">Die Empfängerliste der Nachricht wurde erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e9cd-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e9cd-119">Remarks</span></span>

<span data-ttu-id="0e9cd-120">Die **IMAPISupport:: ExpandRecips** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="0e9cd-121">Nachrichtenspeicher Anbieter rufen **ExpandRecips** auf, um MAPI aufzufordern, die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="0e9cd-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="0e9cd-122">Erweitern Sie bestimmte persönliche Verteilerlisten zu ihren Komponenten Empfängern.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="0e9cd-123">Ersetzen Sie alle Anzeigenamen, die mit den ursprünglichen Namen geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="0e9cd-124">Markieren Sie alle doppelten Einträge.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="0e9cd-125">Lösen Sie alle einmaligen Adressen.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="0e9cd-126">Überprüfen Sie, ob die Nachricht eine Vorverarbeitung erfordert, und legen Sie, falls dies der Fall ist, die Kennzeichnung fest, auf die durch _lpulFlags_ auf NEEDS_PREPROCESSING verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="0e9cd-127">**ExpandRecips** erweitert alle Verteilerlisten mit dem Nachrichten Adresstyp MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0e9cd-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0e9cd-128">Notes to callers</span></span>

<span data-ttu-id="0e9cd-129">Rufen Sie **ExpandRecips** immer als Teil der Nachrichtenverarbeitung auf.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="0e9cd-130">Rufen Sie einen der ersten Aufrufe in der **ExpandRecips** -Implementierung der [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="0e9cd-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0e9cd-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e9cd-131">See also</span></span>



[<span data-ttu-id="0e9cd-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="0e9cd-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="0e9cd-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e9cd-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

