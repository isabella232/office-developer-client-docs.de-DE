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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341258"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="1463f-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1463f-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="1463f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1463f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1463f-105">Aktualisiert den Status im Dialogfeld senden/empfangen.</span><span class="sxs-lookup"><span data-stu-id="1463f-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="1463f-106">Der Informationsspeicher Anbieter ruft diese Funktion regelmäßig auf.</span><span class="sxs-lookup"><span data-stu-id="1463f-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="1463f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1463f-107">Parameters</span></span>

 <span data-ttu-id="1463f-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="1463f-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="1463f-109">Ein Zeiger auf eine Zeichenfolge, die den aktuellen Status Schritt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1463f-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="1463f-110">Es kann NULL sein, um den Fortschritt zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1463f-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="1463f-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="1463f-111">**ulIndex**</span></span>
  
> <span data-ttu-id="1463f-112">Aktuelle Position.</span><span class="sxs-lookup"><span data-stu-id="1463f-112">The current position in progress.</span></span>
    
 <span data-ttu-id="1463f-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="1463f-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="1463f-114">Der Index, der den vollständigen Fortschritt angibt.</span><span class="sxs-lookup"><span data-stu-id="1463f-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1463f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1463f-115">Return value</span></span>

<span data-ttu-id="1463f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1463f-116">S_OK</span></span> 
  
> <span data-ttu-id="1463f-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="1463f-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1463f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1463f-118">See also</span></span>



[<span data-ttu-id="1463f-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1463f-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

