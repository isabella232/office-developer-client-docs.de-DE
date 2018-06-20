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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 771b466e58bf57a7eb4285c6f6ce94c815ec7288
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795447"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="06480-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="06480-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="06480-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06480-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06480-105">["MAPIInitialize"](mapiinitialize.md) ersetzt, wenn nur select Hilfsfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06480-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06480-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="06480-106">Header file:</span></span>  <br/> |<span data-ttu-id="06480-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="06480-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="06480-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="06480-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="06480-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="06480-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="06480-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="06480-110">Called by:</span></span>  <br/> |<span data-ttu-id="06480-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="06480-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="06480-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="06480-112">Parameters</span></span>

 <span data-ttu-id="06480-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="06480-113">_ulFlags_</span></span>
  
> <span data-ttu-id="06480-114">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="06480-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="06480-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="06480-115">Return value</span></span>

<span data-ttu-id="06480-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="06480-116">S_OK</span></span> 
  
> <span data-ttu-id="06480-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="06480-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="06480-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="06480-118">Remarks</span></span>

<span data-ttu-id="06480-119">Die Funktionen **ScInitMapiUtil** und [DeinitMapiUtil](deinitmapiutil.md) zusammenarbeiten, um aufrufen und Freigeben von select Hilfsfunktionen für Funktionen, im Gegensatz zu ["MAPIInitialize"](mapiinitialize.md), die Core sowie Dienstprogramm aufruft.</span><span class="sxs-lookup"><span data-stu-id="06480-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="06480-120">Wenn **ScInitMapiUtil** Hilfsfunktionen anruft, wird auch den erforderlichen Arbeitsspeicher initialisiert.</span><span class="sxs-lookup"><span data-stu-id="06480-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="06480-121">Nach Abschluss der Verwendung der Funktionen, die **ScInitMapiUtil** aufgerufen hat muss **DeinitMapiUtil** explizit aufgerufen werden, um diese freigeben.</span><span class="sxs-lookup"><span data-stu-id="06480-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="06480-122">Im Gegensatz dazu ruft **"MAPIInitialize"** implizit **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="06480-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06480-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06480-123">See also</span></span>



[<span data-ttu-id="06480-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="06480-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

