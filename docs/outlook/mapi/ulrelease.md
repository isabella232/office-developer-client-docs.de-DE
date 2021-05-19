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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415845"
---
# <a name="ulrelease"></a><span data-ttu-id="ec0f3-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="ec0f3-103">UlRelease</span></span>

  
  
<span data-ttu-id="ec0f3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec0f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec0f3-105">Bietet eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown::Release**.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ec0f3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ec0f3-106">Header file:</span></span>  <br/> |<span data-ttu-id="ec0f3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec0f3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ec0f3-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ec0f3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ec0f3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ec0f3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ec0f3-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ec0f3-110">Called by:</span></span>  <br/> |<span data-ttu-id="ec0f3-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ec0f3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="ec0f3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec0f3-112">Parameters</span></span>

 <span data-ttu-id="ec0f3-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="ec0f3-113">_punk_</span></span>
  
> <span data-ttu-id="ec0f3-114">[in] Zeiger auf eine Schnittstelle, die von der **IUnknown-Schnittstelle** abgeleitet ist, d. h. auf eine beliebige MAPI-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ec0f3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec0f3-115">Return value</span></span>

<span data-ttu-id="ec0f3-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec0f3-116">S_OK</span></span> 
  
> <span data-ttu-id="ec0f3-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="ec0f3-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="ec0f3-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="ec0f3-119">Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec0f3-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec0f3-120">Remarks</span></span>

<span data-ttu-id="ec0f3-121">Die Referenzanzahl ist die Anzahl vorhandener Zeiger auf das zu freigegebene Objekt.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="ec0f3-122">Wenn der  _Parameter "punk"_ NULL ist, gibt die Funktion sofort ohne Aufruf von **IUnknown::Release zurück.**</span><span class="sxs-lookup"><span data-stu-id="ec0f3-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="ec0f3-123">**UlRelease** gibt den von der **IUnknown::Release-Methode** zurückgegebenen Wert zurück, der der Referenzanzahl für das losgelassene Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="ec0f3-124">Weitere Informationen zu **IUnknown::Release finden** Sie unter [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="ec0f3-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

