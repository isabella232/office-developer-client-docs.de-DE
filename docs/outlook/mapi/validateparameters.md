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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 662330a7b8c665471e9bbe6af27dff84ee68c8cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586067"
---
# <a name="validateparameters"></a><span data-ttu-id="dbed4-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="dbed4-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="dbed4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbed4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbed4-105">Ruft eine interne Funktion, um zu überprüfen, dass die Parameter-Clientanwendungen Dienstanbietern vergangen sind.</span><span class="sxs-lookup"><span data-stu-id="dbed4-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbed4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="dbed4-106">Header file:</span></span>  <br/> |<span data-ttu-id="dbed4-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="dbed4-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="dbed4-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="dbed4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dbed4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dbed4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dbed4-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="dbed4-110">Called by:</span></span>  <br/> |<span data-ttu-id="dbed4-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="dbed4-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="dbed4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbed4-112">Parameters</span></span>

 <span data-ttu-id="dbed4-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="dbed4-113">_eMethod_</span></span>
  
> <span data-ttu-id="dbed4-114">[in] Gibt den-Enumeration zurück, die-Methode, um zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="dbed4-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="dbed4-115">_Erster_</span><span class="sxs-lookup"><span data-stu-id="dbed4-115">_First_</span></span>
  
> <span data-ttu-id="dbed4-116">[in] Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="dbed4-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dbed4-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="dbed4-117">Return value</span></span>

<span data-ttu-id="dbed4-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="dbed4-118">S_OK</span></span> 
  
> <span data-ttu-id="dbed4-119">Alle Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dbed4-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="dbed4-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="dbed4-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="dbed4-121">Eine oder mehrere der Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dbed4-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dbed4-122">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="dbed4-122">Remarks</span></span>

<span data-ttu-id="dbed4-123">Das Makro **ValidateParameters** wurde durch das Makro [ValidateParms](validateparms.md) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="dbed4-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="dbed4-124">**ValidateParameters** funktioniert nicht ordnungsgemäß auf RISC-Plattformen und wird nun auf diese zu kompilieren verhindert.</span><span class="sxs-lookup"><span data-stu-id="dbed4-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="dbed4-125">Immer noch kompiliert und auf Intel-Plattformen ordnungsgemäß funktioniert, aber **ValidateParms** wird auf allen Plattformen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="dbed4-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

