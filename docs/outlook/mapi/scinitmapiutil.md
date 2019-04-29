---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420591"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="510f4-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="510f4-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="510f4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="510f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="510f4-105">Ersetzt [MAPIInitialize](mapiinitialize.md) , wenn nur ausgewählte Dienstprogrammfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="510f4-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="510f4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="510f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="510f4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="510f4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="510f4-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="510f4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="510f4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="510f4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="510f4-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="510f4-110">Called by:</span></span>  <br/> |<span data-ttu-id="510f4-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="510f4-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="510f4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="510f4-112">Parameters</span></span>

 <span data-ttu-id="510f4-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="510f4-113">_ulFlags_</span></span>
  
> <span data-ttu-id="510f4-114">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="510f4-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="510f4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="510f4-115">Return value</span></span>

<span data-ttu-id="510f4-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="510f4-116">S_OK</span></span> 
  
> <span data-ttu-id="510f4-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="510f4-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="510f4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="510f4-118">Remarks</span></span>

<span data-ttu-id="510f4-119">Die **ScInitMapiUtil** -und die [DeinitMapiUtil](deinitmapiutil.md) -Funktion kooperieren beim Aufrufen und Freigeben von SELECT Utility-Funktionen, im Gegensatz zu [MAPIInitialize](mapiinitialize.md), das sowohl Core-als auch Utility-Funktionen aufruft.</span><span class="sxs-lookup"><span data-stu-id="510f4-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="510f4-120">Wenn **ScInitMapiUtil** Dienstfunktionen aufruft, wird auch der erforderliche Speicher initialisiert.</span><span class="sxs-lookup"><span data-stu-id="510f4-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="510f4-121">Wenn die Verwendung der von **ScInitMapiUtil** aufgerufenen Funktionen abgeschlossen ist, muss **DeinitMapiUtil** explizit aufgerufen werden, um Sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="510f4-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="510f4-122">**MAPIInitialize** ruft hingegen implizit **DeinitMapiUtil**auf.</span><span class="sxs-lookup"><span data-stu-id="510f4-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="510f4-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="510f4-123">See also</span></span>



[<span data-ttu-id="510f4-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="510f4-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

