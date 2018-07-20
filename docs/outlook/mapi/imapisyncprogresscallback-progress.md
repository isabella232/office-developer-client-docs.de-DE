---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 12624ef6212f9113041bf5cf3a82e2b7df6eca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792428"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="61a8c-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61a8c-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="61a8c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61a8c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61a8c-105">Aktualisiert den Status im Dialogfeld senden/empfangen.</span><span class="sxs-lookup"><span data-stu-id="61a8c-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="61a8c-106">Diese Funktion wird in regelmäßigen Abständen Speicheranbieter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="61a8c-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="61a8c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="61a8c-107">Parameters</span></span>

 <span data-ttu-id="61a8c-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="61a8c-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="61a8c-109">Ein Zeiger auf eine Zeichenfolge, die den aktuellen Status Schritt wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61a8c-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="61a8c-110">Zum Aktualisieren des Fortschritts NULL kann sein.</span><span class="sxs-lookup"><span data-stu-id="61a8c-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="61a8c-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="61a8c-111">**ulIndex**</span></span>
  
> <span data-ttu-id="61a8c-112">Die aktuelle Position in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="61a8c-112">The current position in progress.</span></span>
    
 <span data-ttu-id="61a8c-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="61a8c-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="61a8c-114">Der Index, der Fortschritt der Fertigstellung angibt.</span><span class="sxs-lookup"><span data-stu-id="61a8c-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="61a8c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61a8c-115">Return value</span></span>

<span data-ttu-id="61a8c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="61a8c-116">S_OK</span></span> 
  
> <span data-ttu-id="61a8c-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="61a8c-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61a8c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61a8c-118">See also</span></span>



[<span data-ttu-id="61a8c-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61a8c-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

