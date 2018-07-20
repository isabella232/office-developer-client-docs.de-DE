---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 12b1655b1e6786d2ebc985e834b635679e59f7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795789"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="49ac1-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="49ac1-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="49ac1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49ac1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49ac1-105">Ruft eine interne Funktion, um zu überprüfen, dass die Parameter-Clientanwendungen zu Dienstanbietern und MAPI-vergangen sind.</span><span class="sxs-lookup"><span data-stu-id="49ac1-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49ac1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="49ac1-106">Header file:</span></span>  <br/> |<span data-ttu-id="49ac1-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="49ac1-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="49ac1-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="49ac1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="49ac1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="49ac1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="49ac1-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="49ac1-110">Called by:</span></span>  <br/> |<span data-ttu-id="49ac1-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="49ac1-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="49ac1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="49ac1-112">Parameters</span></span>

 <span data-ttu-id="49ac1-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="49ac1-113">_eMethod_</span></span>
  
> <span data-ttu-id="49ac1-114">[in] Gibt den-Enumeration zurück, die-Methode, um zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="49ac1-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="49ac1-115">_Erster_</span><span class="sxs-lookup"><span data-stu-id="49ac1-115">_First_</span></span>
  
> <span data-ttu-id="49ac1-116">[in] Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="49ac1-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="49ac1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49ac1-117">Return value</span></span>

<span data-ttu-id="49ac1-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="49ac1-118">S_OK</span></span> 
  
> <span data-ttu-id="49ac1-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="49ac1-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="49ac1-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="49ac1-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="49ac1-121">Ein Fehler verhindert den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="49ac1-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49ac1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49ac1-122">Remarks</span></span>

<span data-ttu-id="49ac1-123">Übergeben Sie Parameter zwischen MAPI- und Service Provider wird angenommen, dass korrekt und unterzogen werden nur Debug Validierung mit dem Makro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="49ac1-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="49ac1-124">Anbieter sollten alle von Clientanwendungen übergebenen Parameter überprüfen, aber Clients sollten davon ausgehen, dass MAPI und Anbieter Parameter richtig sind.</span><span class="sxs-lookup"><span data-stu-id="49ac1-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="49ac1-125">Verwenden Sie das Makro **HR_FAILED** , um Rückgabewerte testen.</span><span class="sxs-lookup"><span data-stu-id="49ac1-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="49ac1-126">Das Makro **UlValidateParms** wird je nachdem, ob der aufrufende Code C oder C++ ist anders aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="49ac1-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="49ac1-127">Dieses Makro wird verwendet, um die Parameter für die einige **IUnknown** und MAPI-Methoden, die ULONG anstelle von HRESULT-Werte zurückgeben. das Makro [ValidateParms](validateparms.md) funktioniert für alle anderen.</span><span class="sxs-lookup"><span data-stu-id="49ac1-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

