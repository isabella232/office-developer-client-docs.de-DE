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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360494"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="7c8c3-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="7c8c3-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="7c8c3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c8c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c8c3-105">Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die von Clientanwendungen an Dienstanbieter und MAPI übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c8c3-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="7c8c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="7c8c3-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="7c8c3-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="7c8c3-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7c8c3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7c8c3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7c8c3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7c8c3-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7c8c3-110">Called by:</span></span>  <br/> |<span data-ttu-id="7c8c3-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7c8c3-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="7c8c3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c8c3-112">Parameters</span></span>

 <span data-ttu-id="7c8c3-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="7c8c3-113">_eMethod_</span></span>
  
> <span data-ttu-id="7c8c3-114">in Gibt die zu überprüfende Methode an.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="7c8c3-115">_First_</span><span class="sxs-lookup"><span data-stu-id="7c8c3-115">_First_</span></span>
  
> <span data-ttu-id="7c8c3-116">in Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c8c3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c8c3-117">Return value</span></span>

<span data-ttu-id="7c8c3-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c8c3-118">S_OK</span></span> 
  
> <span data-ttu-id="7c8c3-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="7c8c3-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="7c8c3-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="7c8c3-121">Fehler beim Abschließen des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c8c3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c8c3-122">Remarks</span></span>

<span data-ttu-id="7c8c3-123">Parameter, die zwischen MAPI-und Dienstanbietern übergeben werden, werden als richtig angenommen und werden nur mit dem [CheckParms](checkparms.md) -Makro überprüft.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="7c8c3-124">Anbieter sollten alle Parameter überprüfen, die von Clientanwendungen übergeben wurden, aber Clients sollten davon ausgehen, dass MAPI-und Anbieter Parameter korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="7c8c3-125">Verwenden Sie das **HR_FAILED** -Makro, um Rückgabewerte zu testen.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="7c8c3-126">Das **UlValidateParms** -Makro wird anders aufgerufen, je nachdem, ob es sich bei dem aufrufenden Code um C oder C++ handelt.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="7c8c3-127">Dieses Makro wird verwendet, um Parameter für die wenigen **IUnknown** -und MAPI-Methoden zu überprüfen, die ULONG anstelle von HRESULT-Werten zurückgeben. Das [ValidateParms](validateparms.md) -Makro funktioniert für alle anderen.</span><span class="sxs-lookup"><span data-stu-id="7c8c3-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

