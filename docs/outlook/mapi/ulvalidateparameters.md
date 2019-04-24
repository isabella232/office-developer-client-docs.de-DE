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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315288"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="f4061-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="f4061-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="f4061-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4061-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4061-105">Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die von Clientanwendungen an Dienstanbieter und MAPI übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="f4061-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4061-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="f4061-106">Header file:</span></span>  <br/> |<span data-ttu-id="f4061-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f4061-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f4061-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f4061-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f4061-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f4061-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f4061-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f4061-110">Called by:</span></span>  <br/> |<span data-ttu-id="f4061-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f4061-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="f4061-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4061-112">Parameters</span></span>

 <span data-ttu-id="f4061-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="f4061-113">_eMethod_</span></span>
  
> <span data-ttu-id="f4061-114">in Gibt die zu überprüfende Methode an.</span><span class="sxs-lookup"><span data-stu-id="f4061-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="f4061-115">_First_</span><span class="sxs-lookup"><span data-stu-id="f4061-115">_First_</span></span>
  
> <span data-ttu-id="f4061-116">in Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="f4061-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f4061-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4061-117">Return value</span></span>

<span data-ttu-id="f4061-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4061-118">S_OK</span></span> 
  
> <span data-ttu-id="f4061-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f4061-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="f4061-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="f4061-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="f4061-121">Der Vorgang konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="f4061-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4061-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4061-122">Remarks</span></span>

<span data-ttu-id="f4061-123">Das **UlValidateParameters** -Makro wurde vom [UlValidateParms](ulvalidateparms.md) -Makro abgelöst.</span><span class="sxs-lookup"><span data-stu-id="f4061-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="f4061-124">**UlValidateParameters** funktioniert auf RISC-Plattformen nicht ordnungsgemäß und kann nun nicht mehr kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="f4061-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="f4061-125">Es wird weiterhin auf Intel-Plattformen kompiliert und funktioniert, aber **UlValidateParms** wird auf allen Plattformen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="f4061-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

