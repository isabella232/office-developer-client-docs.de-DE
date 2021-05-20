---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431274"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="1db8b-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="1db8b-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="1db8b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1db8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1db8b-105">Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die Clientanwendungen an Dienstanbieter und MAPI übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="1db8b-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1db8b-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="1db8b-106">Header file:</span></span>  <br/> |<span data-ttu-id="1db8b-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="1db8b-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="1db8b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1db8b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1db8b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1db8b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1db8b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1db8b-110">Called by:</span></span>  <br/> |<span data-ttu-id="1db8b-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1db8b-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="1db8b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1db8b-112">Parameters</span></span>

 <span data-ttu-id="1db8b-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="1db8b-113">_eMethod_</span></span>
  
> <span data-ttu-id="1db8b-114">[in] Gibt die zu überprüfende Methode per Enumeration an.</span><span class="sxs-lookup"><span data-stu-id="1db8b-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="1db8b-115">_First_</span><span class="sxs-lookup"><span data-stu-id="1db8b-115">_First_</span></span>
  
> <span data-ttu-id="1db8b-116">[in] Zeiger auf das erste Argument auf dem Stapel.</span><span class="sxs-lookup"><span data-stu-id="1db8b-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1db8b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1db8b-117">Return value</span></span>

<span data-ttu-id="1db8b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1db8b-118">S_OK</span></span> 
  
> <span data-ttu-id="1db8b-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="1db8b-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="1db8b-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="1db8b-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="1db8b-121">Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1db8b-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1db8b-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1db8b-122">Remarks</span></span>

<span data-ttu-id="1db8b-123">Das **UlValidateParameters-Makro** wurde durch das [UlValidateParms-Makro ersetzt.](ulvalidateparms.md)</span><span class="sxs-lookup"><span data-stu-id="1db8b-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="1db8b-124">**UlValidateParameters** funktioniert nicht ordnungsgemäß auf RISC-Plattformen und kann jetzt nicht mehr für sie kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="1db8b-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="1db8b-125">Sie wird weiterhin auf Intel-Plattformen kompiliert und funktioniert ordnungsgemäß, **UlValidateParms** wird jedoch auf allen Plattformen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="1db8b-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

