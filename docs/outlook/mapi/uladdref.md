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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fc6c12d914e581c3f975e94809f0bdea73020099
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795769"
---
# <a name="uladdref"></a><span data-ttu-id="6b209-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="6b209-103">UlAddRef</span></span>

  
  
<span data-ttu-id="6b209-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b209-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b209-105">Bietet eine alternative Möglichkeit, die OLE-Methode **IUnknown:: AddRef**aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b209-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b209-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6b209-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b209-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b209-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6b209-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6b209-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6b209-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6b209-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6b209-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6b209-110">Called by:</span></span>  <br/> |<span data-ttu-id="6b209-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="6b209-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="6b209-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b209-112">Parameters</span></span>

 <span data-ttu-id="6b209-113">_pUnk_</span><span class="sxs-lookup"><span data-stu-id="6b209-113">_punk_</span></span>
  
> <span data-ttu-id="6b209-114">[in] Zeiger auf eine Schnittstelle abgeleitet die **IUnknown** -Schnittstelle, mit anderen Worten alle MAPI-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6b209-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6b209-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6b209-115">Return value</span></span>

<span data-ttu-id="6b209-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b209-116">S_OK</span></span> 
  
> <span data-ttu-id="6b209-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="6b209-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="6b209-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="6b209-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="6b209-119">Ein Fehler unerwartete oder unbekannten Ursprungs verhindert den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="6b209-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b209-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6b209-120">Remarks</span></span>

 <span data-ttu-id="6b209-121">**UlAddRef** gibt den Wert von der **IUnknown:: AddRef** -Methode zurückgegeben, die der neue Wert für den Referenzzähler für die Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="6b209-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="6b209-122">Der Wert ist ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="6b209-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="6b209-123">Weitere Informationen zu **IUnknown:: AddRef**finden Sie unter [die IUnknown-Schnittstelle implementieren](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="6b209-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

