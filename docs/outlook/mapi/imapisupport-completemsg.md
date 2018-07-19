---
title: IMAPISupportCompleteMsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: db28d9684f1bb679ce36f99346f4ecc67a1a93e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19792352"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="e0b25-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="e0b25-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="e0b25-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0b25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0b25-105">Führt Nachbearbeitung für eine Nachricht aus.</span><span class="sxs-lookup"><span data-stu-id="e0b25-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e0b25-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0b25-106">Parameters</span></span>

 <span data-ttu-id="e0b25-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e0b25-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e0b25-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="e0b25-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e0b25-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e0b25-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="e0b25-110">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="e0b25-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e0b25-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e0b25-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="e0b25-112">[in] Ein Zeiger auf die Eintrags-ID der Nachricht zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e0b25-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0b25-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0b25-113">Return value</span></span>

<span data-ttu-id="e0b25-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0b25-114">S_OK</span></span> 
  
> <span data-ttu-id="e0b25-115">Die Nachbearbeitung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e0b25-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0b25-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0b25-116">Remarks</span></span>

<span data-ttu-id="e0b25-117">Die **IMAPISupport::CompleteMsg** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert und heißt nur Zeichenfolgeneigenschaften Nachricht, die eng mit Anbietern Transport verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="e0b25-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="e0b25-118">Anbieter eng gekoppelten Aufrufen **IMAPISupport::CompleteMsg** um anzuweisen, die MAPI-Warteschlange auf eine Nachricht zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e0b25-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e0b25-119">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e0b25-119">Notes to callers</span></span>

<span data-ttu-id="e0b25-120">Rufen Sie **CompleteMsg** nur, wenn Sie eng mit eines Transportdienstes verknüpft sind, Sie alle Empfänger der Nachricht behandeln können und eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0b25-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="e0b25-121">Die Nachricht wurde vorverarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e0b25-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="e0b25-122">Die Nachricht muss Nachbearbeitung durch die MAPI-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e0b25-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0b25-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0b25-123">See also</span></span>



[<span data-ttu-id="e0b25-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0b25-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

