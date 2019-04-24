---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329568"
---
# <a name="validateparameters"></a><span data-ttu-id="6b047-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="6b047-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="6b047-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b047-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b047-105">Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die Clientanwendungen an Dienstanbieter übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="6b047-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b047-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="6b047-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b047-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="6b047-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="6b047-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6b047-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6b047-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6b047-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6b047-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6b047-110">Called by:</span></span>  <br/> |<span data-ttu-id="6b047-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="6b047-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="6b047-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b047-112">Parameters</span></span>

 <span data-ttu-id="6b047-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="6b047-113">_eMethod_</span></span>
  
> <span data-ttu-id="6b047-114">in Gibt die zu überprüfende Methode an.</span><span class="sxs-lookup"><span data-stu-id="6b047-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="6b047-115">_First_</span><span class="sxs-lookup"><span data-stu-id="6b047-115">_First_</span></span>
  
> <span data-ttu-id="6b047-116">in Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="6b047-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b047-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b047-117">Return value</span></span>

<span data-ttu-id="6b047-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b047-118">S_OK</span></span> 
  
> <span data-ttu-id="6b047-119">Alle Parameter sind gültig.</span><span class="sxs-lookup"><span data-stu-id="6b047-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="6b047-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="6b047-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="6b047-121">Mindestens einer der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6b047-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b047-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b047-122">Remarks</span></span>

<span data-ttu-id="6b047-123">Das **ValidateParameters** -Makro wurde vom [ValidateParms](validateparms.md) -Makro abgelöst.</span><span class="sxs-lookup"><span data-stu-id="6b047-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="6b047-124">**ValidateParameters** funktioniert auf RISC-Plattformen nicht ordnungsgemäß und kann nun nicht mehr kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="6b047-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="6b047-125">Es wird weiterhin auf Intel-Plattformen kompiliert und funktioniert, aber **ValidateParms** wird auf allen Plattformen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="6b047-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

