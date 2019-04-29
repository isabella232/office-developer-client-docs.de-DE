---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432835"
---
# <a name="uladdref"></a><span data-ttu-id="5fd39-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="5fd39-103">UlAddRef</span></span>

  
  
<span data-ttu-id="5fd39-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fd39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fd39-105">Stellt eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown:: AddRef**.</span><span class="sxs-lookup"><span data-stu-id="5fd39-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fd39-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5fd39-106">Header file:</span></span>  <br/> |<span data-ttu-id="5fd39-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5fd39-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5fd39-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5fd39-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5fd39-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5fd39-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5fd39-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5fd39-110">Called by:</span></span>  <br/> |<span data-ttu-id="5fd39-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5fd39-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="5fd39-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fd39-112">Parameters</span></span>

 <span data-ttu-id="5fd39-113">_Punk_</span><span class="sxs-lookup"><span data-stu-id="5fd39-113">_punk_</span></span>
  
> <span data-ttu-id="5fd39-114">in Zeiger auf eine von der **IUnknown** -Schnittstelle abgeleitete Schnittstelle, also jede MAPI-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5fd39-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5fd39-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5fd39-115">Return value</span></span>

<span data-ttu-id="5fd39-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5fd39-116">S_OK</span></span> 
  
> <span data-ttu-id="5fd39-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="5fd39-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="5fd39-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="5fd39-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="5fd39-119">Der Vorgang konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="5fd39-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5fd39-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fd39-120">Remarks</span></span>

 <span data-ttu-id="5fd39-121">**UlAddRef** gibt den von der **IUnknown:: AddRef** -Methode zurückgegebenen Wert zurück, bei dem es sich um den neuen Wert des Verweiszählers für die Schnittstelle handelt.</span><span class="sxs-lookup"><span data-stu-id="5fd39-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="5fd39-122">Der Wert ist ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="5fd39-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="5fd39-123">Weitere Informationen zu **IUnknown:: AddRef**finden Sie unter [Implementieren der IUnknown-Schnittstelle](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="5fd39-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

