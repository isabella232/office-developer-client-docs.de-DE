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
ms.openlocfilehash: 9b44337a4bc9615558ac6337e99ea206ba063b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429110"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="35c58-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35c58-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="35c58-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35c58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35c58-105">Aktualisiert den Status im Dialogfeld Senden/Empfangen.</span><span class="sxs-lookup"><span data-stu-id="35c58-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="35c58-106">Der Speicheranbieter ruft diese Funktion regelmäßig auf.</span><span class="sxs-lookup"><span data-stu-id="35c58-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="35c58-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="35c58-107">Parameters</span></span>

 <span data-ttu-id="35c58-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="35c58-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="35c58-109">Ein Zeiger auf eine Zeichenfolge, die den aktuellen Fortschrittsschritt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="35c58-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="35c58-110">Es kann NULL sein, um den Fortschritt zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="35c58-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="35c58-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="35c58-111">**ulIndex**</span></span>
  
> <span data-ttu-id="35c58-112">Die aktuelle position in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="35c58-112">The current position in progress.</span></span>
    
 <span data-ttu-id="35c58-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="35c58-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="35c58-114">Der Index, der den vollständigen Fortschritt angibt.</span><span class="sxs-lookup"><span data-stu-id="35c58-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35c58-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35c58-115">Return value</span></span>

<span data-ttu-id="35c58-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="35c58-116">S_OK</span></span> 
  
> <span data-ttu-id="35c58-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="35c58-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35c58-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35c58-118">See also</span></span>



[<span data-ttu-id="35c58-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35c58-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

