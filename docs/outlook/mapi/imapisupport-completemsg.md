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
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411190"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="ec519-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="ec519-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="ec519-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec519-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec519-105">Führt die Nachverarbeitung für eine Nachricht durch.</span><span class="sxs-lookup"><span data-stu-id="ec519-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="ec519-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec519-106">Parameters</span></span>

 <span data-ttu-id="ec519-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ec519-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ec519-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="ec519-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ec519-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ec519-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="ec519-110">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="ec519-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ec519-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ec519-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="ec519-112">[in] Ein Zeiger auf die Eintrags-ID der zu verarbeitende Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ec519-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec519-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec519-113">Return value</span></span>

<span data-ttu-id="ec519-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec519-114">S_OK</span></span> 
  
> <span data-ttu-id="ec519-115">Die Nachverarbeitung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ec519-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec519-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec519-116">Remarks</span></span>

<span data-ttu-id="ec519-117">Die **IMAPISupport::CompleteMsg-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert und nur von Nachrichtenspeicheranbietern aufgerufen, die eng mit Transportanbietern gekoppelt sind.</span><span class="sxs-lookup"><span data-stu-id="ec519-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="ec519-118">Eng gekoppelte Speicheranbieter rufen **IMAPISupport::CompleteMsg** auf, um den MAPI-Spooler anweisen, eine Nachricht nachverarbeitet zu haben.</span><span class="sxs-lookup"><span data-stu-id="ec519-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ec519-119">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ec519-119">Notes to callers</span></span>

<span data-ttu-id="ec519-120">Rufen **Sie CompleteMsg** nur auf, wenn Sie eng mit einem Transportanbieter gekoppelt sind, Sie alle Empfänger der Nachricht behandeln können, und eine der folgenden Bedingungen ist vorhanden:</span><span class="sxs-lookup"><span data-stu-id="ec519-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="ec519-121">Die Nachricht wurde vorverarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ec519-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="ec519-122">Die Nachricht erfordert die Nachverarbeitung durch den MAPI-Spooler.</span><span class="sxs-lookup"><span data-stu-id="ec519-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec519-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec519-123">See also</span></span>



[<span data-ttu-id="ec519-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec519-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

