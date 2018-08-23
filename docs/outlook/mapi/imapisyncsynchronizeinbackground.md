---
title: IMAPISync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: 'Zuletzt geändert: 26 Juni 2012'
ms.openlocfilehash: ee6fe07df894213331ab51f9abaa4008247dac07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568777"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="94211-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="94211-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="94211-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94211-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="94211-105">Initiiert eine Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="94211-105">Initiates a synchronization.</span></span> <span data-ttu-id="94211-106">Diese Methode wird von Microsoft Outlook 2010 und Microsoft Outlook 2013 aufgerufen und Zeichenfolgeneigenschaften Nachricht implementiert.</span><span class="sxs-lookup"><span data-stu-id="94211-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="94211-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="94211-107">Parameters</span></span>

 <span data-ttu-id="94211-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="94211-108">_psibpb_</span></span>
  
> <span data-ttu-id="94211-109">Informiert den Anbieter von Was synchronisiert werden soll, und ermöglicht den Zugriff auf Schnittstellen, die während der Synchronisierung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="94211-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="94211-110">Es ist eine [MAPISIB](mapisib.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="94211-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="94211-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="94211-111">Return value</span></span>

<span data-ttu-id="94211-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="94211-112">S_OK</span></span> 
  
> <span data-ttu-id="94211-113">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="94211-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94211-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94211-114">See also</span></span>



[<span data-ttu-id="94211-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94211-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="94211-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="94211-116">MAPISIB</span></span>](mapisib.md)

