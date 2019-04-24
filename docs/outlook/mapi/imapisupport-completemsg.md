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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331507"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="ad19e-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="ad19e-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="ad19e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad19e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad19e-105">Führt die Nachbearbeitung für eine Nachricht aus.</span><span class="sxs-lookup"><span data-stu-id="ad19e-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="ad19e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad19e-106">Parameters</span></span>

 <span data-ttu-id="ad19e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ad19e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ad19e-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="ad19e-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ad19e-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ad19e-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="ad19e-110">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ad19e-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ad19e-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ad19e-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="ad19e-112">in Ein Zeiger auf die Eintrags-ID der zu verarbeitenden Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ad19e-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ad19e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad19e-113">Return value</span></span>

<span data-ttu-id="ad19e-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad19e-114">S_OK</span></span> 
  
> <span data-ttu-id="ad19e-115">Die Nachbearbeitung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ad19e-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad19e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad19e-116">Remarks</span></span>

<span data-ttu-id="ad19e-117">Die **IMAPISupport:: CompleteMsg** -Methode wird für Nachrichtenspeicher Anbieter-Support Objekte implementiert und nur von Nachrichtenspeicher Anbietern aufgerufen, die eng mit Transportanbietern verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="ad19e-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="ad19e-118">Eng gekoppelte Speicheranbieter rufen **IMAPISupport:: CompleteMsg** auf, um den MAPI-Spooler anzuweisen, eine Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="ad19e-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ad19e-119">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ad19e-119">Notes to callers</span></span>

<span data-ttu-id="ad19e-120">**CompleteMsg** nur aufrufen, wenn Sie eng mit einem Transportanbieter verbunden sind, können Sie alle Empfänger der Nachricht verarbeiten, und eine der folgenden Bedingungen ist vorhanden:</span><span class="sxs-lookup"><span data-stu-id="ad19e-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="ad19e-121">Die Nachricht wurde vorverarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ad19e-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="ad19e-122">Die Nachricht erfordert die Nachbearbeitung durch den MAPI-Spooler.</span><span class="sxs-lookup"><span data-stu-id="ad19e-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad19e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad19e-123">See also</span></span>



[<span data-ttu-id="ad19e-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad19e-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

