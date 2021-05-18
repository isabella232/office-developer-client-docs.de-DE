---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ffa1b596b2f60bce35f24df8a20326502be8165a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422278"
---
# <a name="checkparms"></a><span data-ttu-id="309c2-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="309c2-103">CheckParms</span></span>

  
  
<span data-ttu-id="309c2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="309c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="309c2-105">Ruft eine interne Funktion auf, um Debugparameter für von MAPI aufgerufene Dienstanbietermethoden zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="309c2-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="309c2-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="309c2-106">Header file:</span></span>  <br/> |<span data-ttu-id="309c2-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="309c2-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="309c2-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="309c2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="309c2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="309c2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="309c2-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="309c2-110">Called by:</span></span>  <br/> |<span data-ttu-id="309c2-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="309c2-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="309c2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="309c2-112">Parameters</span></span>

 <span data-ttu-id="309c2-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="309c2-113">_eMethod_</span></span>
  
> <span data-ttu-id="309c2-114">[in] Gibt die zu überprüfende Methode per Enumeration an.</span><span class="sxs-lookup"><span data-stu-id="309c2-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="309c2-115">_First_</span><span class="sxs-lookup"><span data-stu-id="309c2-115">_First_</span></span>
  
> <span data-ttu-id="309c2-116">[in] Zeiger auf das erste Argument auf dem Stapel.</span><span class="sxs-lookup"><span data-stu-id="309c2-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="309c2-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="309c2-117">Return value</span></span>

<span data-ttu-id="309c2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="309c2-118">S_OK</span></span> 
  
> <span data-ttu-id="309c2-119">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="309c2-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="309c2-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="309c2-120">Remarks</span></span>

<span data-ttu-id="309c2-121">Im Gegensatz zu den [Makros ValidateParms](validateparms.md) und [UlValidateParms](ulvalidateparms.md) führt das **Makro CheckParms** keine vollständige Parameterüberprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="309c2-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="309c2-122">Parameter, die zwischen MAPI und Dienstanbietern übergeben werden, werden als richtig angenommen, daher führt **CheckParms** nur eine Debugüberprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="309c2-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

