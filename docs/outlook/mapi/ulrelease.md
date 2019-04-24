---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315295"
---
# <a name="ulrelease"></a><span data-ttu-id="3801b-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="3801b-103">UlRelease</span></span>

  
  
<span data-ttu-id="3801b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3801b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3801b-105">Bietet eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="3801b-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3801b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3801b-106">Header file:</span></span>  <br/> |<span data-ttu-id="3801b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3801b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3801b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="3801b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3801b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3801b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3801b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="3801b-110">Called by:</span></span>  <br/> |<span data-ttu-id="3801b-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="3801b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="3801b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3801b-112">Parameters</span></span>

 <span data-ttu-id="3801b-113">_Punk_</span><span class="sxs-lookup"><span data-stu-id="3801b-113">_punk_</span></span>
  
> <span data-ttu-id="3801b-114">in Zeiger auf eine von der **IUnknown** -Schnittstelle abgeleitete Schnittstelle, also jede MAPI-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3801b-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3801b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3801b-115">Return value</span></span>

<span data-ttu-id="3801b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3801b-116">S_OK</span></span> 
  
> <span data-ttu-id="3801b-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="3801b-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="3801b-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="3801b-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="3801b-119">Der Vorgang konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="3801b-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3801b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3801b-120">Remarks</span></span>

<span data-ttu-id="3801b-121">Der Verweiszähler ist die Anzahl der vorhandenen Zeiger auf das Objekt, das freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3801b-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="3801b-122">Wenn der _Punk_ -Parameter NULL ist, wird die Funktion sofort zurückgegeben, ohne **IUnknown:: Release** zu aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3801b-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="3801b-123">**UlRelease** gibt den von der **IUnknown:: Release** -Methode zurückgegebenen Wert zurück, der mit dem Verweiszähler für das freizugebende Objekt übereinstimmen kann.</span><span class="sxs-lookup"><span data-stu-id="3801b-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="3801b-124">Weitere Informationen zu **IUnknown:: Release**finden Sie unter [Implementieren der IUnknown-Schnittstelle](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3801b-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

