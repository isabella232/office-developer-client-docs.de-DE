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
description: 'Letzte Änderung: 26. Juni 2012'
ms.openlocfilehash: 108073f5e4833d9641e67065eb642320352fffe4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426856"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="a467f-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="a467f-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="a467f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a467f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a467f-105">Initiiert eine Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="a467f-105">Initiates a synchronization.</span></span> <span data-ttu-id="a467f-106">Diese Methode wird von Microsoft Outlook 2010 und Microsoft Outlook 2013 aufgerufen und von Nachrichtenspeicheranbietern implementiert.</span><span class="sxs-lookup"><span data-stu-id="a467f-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="a467f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a467f-107">Parameters</span></span>

 <span data-ttu-id="a467f-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="a467f-108">_psibpb_</span></span>
  
> <span data-ttu-id="a467f-109">Informiert den Anbieter darüber, was synchronisiert wird, und gewährt Zugriff auf Schnittstellen, die während der Synchronisierung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a467f-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="a467f-110">Es handelt sich um eine [MAPISIB-Struktur.](mapisib.md)</span><span class="sxs-lookup"><span data-stu-id="a467f-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a467f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a467f-111">Return value</span></span>

<span data-ttu-id="a467f-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a467f-112">S_OK</span></span> 
  
> <span data-ttu-id="a467f-113">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a467f-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a467f-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a467f-114">See also</span></span>



[<span data-ttu-id="a467f-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a467f-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="a467f-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="a467f-116">MAPISIB</span></span>](mapisib.md)

