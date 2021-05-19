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
# <a name="scinitmapiutil"></a><span data-ttu-id="e1494-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="e1494-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="e1494-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1494-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1494-105">Ersetzt [MAPIInitialize,](mapiinitialize.md) wenn nur ausgewählte Hilfsfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1494-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1494-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e1494-106">Header file:</span></span>  <br/> |<span data-ttu-id="e1494-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e1494-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e1494-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e1494-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e1494-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e1494-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e1494-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e1494-110">Called by:</span></span>  <br/> |<span data-ttu-id="e1494-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="e1494-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e1494-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1494-112">Parameters</span></span>

 <span data-ttu-id="e1494-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e1494-113">_ulFlags_</span></span>
  
> <span data-ttu-id="e1494-114">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="e1494-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e1494-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1494-115">Return value</span></span>

<span data-ttu-id="e1494-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1494-116">S_OK</span></span> 
  
> <span data-ttu-id="e1494-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="e1494-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1494-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e1494-118">Remarks</span></span>

<span data-ttu-id="e1494-119">Die **Funktionen ScInitMapiUtil** und [DeinitMapiUtil](deinitmapiutil.md) arbeiten zusammen, um ausgewählte Hilfsfunktionen auf- und frei zu geben, im Gegensatz zu [MAPIInitialize](mapiinitialize.md), das Kern- und Hilfsfunktionen aufruft.</span><span class="sxs-lookup"><span data-stu-id="e1494-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="e1494-120">Wenn **ScInitMapiUtil** Hilfsfunktionen aufruft, initialisiert es auch den erforderlichen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e1494-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="e1494-121">Wenn die Verwendung der Funktionen, die **ScInitMapiUtil** aufgerufen hat, abgeschlossen ist, **muss DeinitMapiUtil** explizit aufgerufen werden, um sie frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="e1494-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="e1494-122">Im Gegensatz dazu ruft **MAPIInitialize** implizit **DeinitMapiUtil auf.**</span><span class="sxs-lookup"><span data-stu-id="e1494-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1494-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1494-123">See also</span></span>



[<span data-ttu-id="e1494-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="e1494-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

