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
ms.openlocfilehash: 5803441486f01883d08cd99048d8eae133cd3f14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592129"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="4fe03-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4fe03-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="4fe03-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fe03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fe03-105">Aktualisiert den Status im Dialogfeld senden/empfangen.</span><span class="sxs-lookup"><span data-stu-id="4fe03-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="4fe03-106">Diese Funktion wird in regelmäßigen Abständen Speicheranbieter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4fe03-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="4fe03-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fe03-107">Parameters</span></span>

 <span data-ttu-id="4fe03-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="4fe03-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="4fe03-109">Ein Zeiger auf eine Zeichenfolge, die den aktuellen Status Schritt wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4fe03-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="4fe03-110">Zum Aktualisieren des Fortschritts NULL kann sein.</span><span class="sxs-lookup"><span data-stu-id="4fe03-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="4fe03-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="4fe03-111">**ulIndex**</span></span>
  
> <span data-ttu-id="4fe03-112">Die aktuelle Position in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="4fe03-112">The current position in progress.</span></span>
    
 <span data-ttu-id="4fe03-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="4fe03-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="4fe03-114">Der Index, der Fortschritt der Fertigstellung angibt.</span><span class="sxs-lookup"><span data-stu-id="4fe03-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4fe03-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="4fe03-115">Return value</span></span>

<span data-ttu-id="4fe03-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4fe03-116">S_OK</span></span> 
  
> <span data-ttu-id="4fe03-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="4fe03-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4fe03-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fe03-118">See also</span></span>



[<span data-ttu-id="4fe03-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4fe03-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

