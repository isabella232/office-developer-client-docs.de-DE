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
ms.openlocfilehash: b71d1f477435b4a9327b4156560d1aa2e6079536
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578703"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="e3057-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="e3057-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="e3057-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3057-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3057-105">Ruft eine interne Funktion, um zu überprüfen, dass die Parameter-Clientanwendungen zu Dienstanbietern und MAPI-vergangen sind.</span><span class="sxs-lookup"><span data-stu-id="e3057-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3057-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e3057-106">Header file:</span></span>  <br/> |<span data-ttu-id="e3057-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="e3057-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="e3057-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e3057-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e3057-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e3057-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e3057-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e3057-110">Called by:</span></span>  <br/> |<span data-ttu-id="e3057-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="e3057-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="e3057-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3057-112">Parameters</span></span>

 <span data-ttu-id="e3057-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="e3057-113">_eMethod_</span></span>
  
> <span data-ttu-id="e3057-114">[in] Gibt den-Enumeration zurück, die-Methode, um zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e3057-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="e3057-115">_Erster_</span><span class="sxs-lookup"><span data-stu-id="e3057-115">_First_</span></span>
  
> <span data-ttu-id="e3057-116">[in] Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="e3057-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e3057-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e3057-117">Return value</span></span>

<span data-ttu-id="e3057-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3057-118">S_OK</span></span> 
  
> <span data-ttu-id="e3057-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="e3057-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e3057-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e3057-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="e3057-121">Ein Fehler verhindert den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e3057-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3057-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3057-122">Remarks</span></span>

<span data-ttu-id="e3057-123">Übergeben Sie Parameter zwischen MAPI- und Service Provider wird angenommen, dass korrekt und unterzogen werden nur Debug Validierung mit dem Makro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="e3057-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="e3057-124">Anbieter sollten alle von Clientanwendungen übergebenen Parameter überprüfen, aber Clients sollten davon ausgehen, dass MAPI und Anbieter Parameter richtig sind.</span><span class="sxs-lookup"><span data-stu-id="e3057-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="e3057-125">Verwenden Sie das Makro **HR_FAILED** , um Rückgabewerte testen.</span><span class="sxs-lookup"><span data-stu-id="e3057-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="e3057-126">Das Makro **UlValidateParms** wird je nachdem, ob der aufrufende Code C oder C++ ist anders aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e3057-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="e3057-127">Dieses Makro wird verwendet, um die Parameter für die einige **IUnknown** und MAPI-Methoden, die ULONG anstelle von HRESULT-Werte zurückgeben. das Makro [ValidateParms](validateparms.md) funktioniert für alle anderen.</span><span class="sxs-lookup"><span data-stu-id="e3057-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

