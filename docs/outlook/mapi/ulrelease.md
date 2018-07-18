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
ms.openlocfilehash: 5b34e2c21ac967b0874872986c0cf484750f4e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795791"
---
# <a name="ulrelease"></a><span data-ttu-id="cb0ee-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="cb0ee-103">UlRelease</span></span>

  
  
<span data-ttu-id="cb0ee-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb0ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb0ee-105">Bietet eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb0ee-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="cb0ee-106">Header file:</span></span>  <br/> |<span data-ttu-id="cb0ee-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb0ee-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cb0ee-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cb0ee-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cb0ee-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cb0ee-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-110">Called by:</span></span>  <br/> |<span data-ttu-id="cb0ee-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="cb0ee-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="cb0ee-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb0ee-112">Parameters</span></span>

 <span data-ttu-id="cb0ee-113">_pUnk_</span><span class="sxs-lookup"><span data-stu-id="cb0ee-113">_punk_</span></span>
  
> <span data-ttu-id="cb0ee-114">[in] Zeiger auf eine Schnittstelle abgeleitet die **IUnknown** -Schnittstelle, mit anderen Worten alle MAPI-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cb0ee-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="cb0ee-115">Return value</span></span>

<span data-ttu-id="cb0ee-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="cb0ee-116">S_OK</span></span> 
  
> <span data-ttu-id="cb0ee-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="cb0ee-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="cb0ee-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="cb0ee-119">Ein Fehler unerwartete oder unbekannten Ursprungs verhindert den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb0ee-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb0ee-120">Remarks</span></span>

<span data-ttu-id="cb0ee-121">Die Anzahl der Verweise ist die Anzahl der vorhandenen Zeiger auf das Objekt, das freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="cb0ee-122">Wenn der Parameter _Punk_ NULL ist, gibt die Funktion sofort ohne einen Aufruf **IUnknown**</span><span class="sxs-lookup"><span data-stu-id="cb0ee-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="cb0ee-123">**UlRelease** gibt den Wert zurückgegeben, die von der **IUnknown** -Methode, die den Referenzzähler für das Objekt, das freigegeben werden muss gleich sein kann.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="cb0ee-124">Weitere Informationen zu **IUnknown**finden Sie unter [die IUnknown-Schnittstelle implementieren](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="cb0ee-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

