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
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419611"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="35a08-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="35a08-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="35a08-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35a08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35a08-105">Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die Clientanwendungen an Dienstanbieter und MAPI übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="35a08-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35a08-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="35a08-106">Header file:</span></span>  <br/> |<span data-ttu-id="35a08-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="35a08-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="35a08-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="35a08-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="35a08-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="35a08-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="35a08-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="35a08-110">Called by:</span></span>  <br/> |<span data-ttu-id="35a08-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="35a08-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="35a08-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="35a08-112">Parameters</span></span>

 <span data-ttu-id="35a08-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="35a08-113">_eMethod_</span></span>
  
> <span data-ttu-id="35a08-114">[in] Gibt die zu überprüfende Methode per Enumeration an.</span><span class="sxs-lookup"><span data-stu-id="35a08-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="35a08-115">_First_</span><span class="sxs-lookup"><span data-stu-id="35a08-115">_First_</span></span>
  
> <span data-ttu-id="35a08-116">[in] Zeiger auf das erste Argument auf dem Stapel.</span><span class="sxs-lookup"><span data-stu-id="35a08-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35a08-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35a08-117">Return value</span></span>

<span data-ttu-id="35a08-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="35a08-118">S_OK</span></span> 
  
> <span data-ttu-id="35a08-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="35a08-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="35a08-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="35a08-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="35a08-121">Ein Fehler verhinderte, dass der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="35a08-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35a08-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35a08-122">Remarks</span></span>

<span data-ttu-id="35a08-123">Parameter, die zwischen MAPI und Dienstanbietern übergeben werden, werden als richtig angenommen und werden nur mit dem [CheckParms-Makro](checkparms.md) einer Debugüberprüfung unterzogen.</span><span class="sxs-lookup"><span data-stu-id="35a08-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="35a08-124">Anbieter sollten alle von Clientanwendungen übergebenen Parameter überprüfen, Clients sollten jedoch davon ausgehen, dass MAPI- und Anbieterparameter korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="35a08-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="35a08-125">Verwenden Sie das **HR_FAILED,** um Rückgabewerte zu testen.</span><span class="sxs-lookup"><span data-stu-id="35a08-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="35a08-126">Das **UlValidateParms-Makro** wird unterschiedlich aufgerufen, je nachdem, ob der aufrufende Code C oder C++ ist.</span><span class="sxs-lookup"><span data-stu-id="35a08-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="35a08-127">Dieses Makro wird verwendet, um Parameter für die wenigen **IUnknown-** und #A0 zu überprüfen, die ULONG anstelle von HRESULT-Werten zurückgeben. Das [ValidateParms-Makro](validateparms.md) funktioniert für alle anderen.</span><span class="sxs-lookup"><span data-stu-id="35a08-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

