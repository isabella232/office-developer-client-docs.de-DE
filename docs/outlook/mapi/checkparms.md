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
# <a name="checkparms"></a><span data-ttu-id="f3a18-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="f3a18-103">CheckParms</span></span>

  
  
<span data-ttu-id="f3a18-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3a18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3a18-105">Ruft eine interne Funktion auf, um debuggingparameter für Dienstanbieter Methoden zu überprüfen, die von MAPI aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f3a18-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3a18-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="f3a18-106">Header file:</span></span>  <br/> |<span data-ttu-id="f3a18-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f3a18-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f3a18-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f3a18-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f3a18-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f3a18-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f3a18-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f3a18-110">Called by:</span></span>  <br/> |<span data-ttu-id="f3a18-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f3a18-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="f3a18-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3a18-112">Parameters</span></span>

 <span data-ttu-id="f3a18-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="f3a18-113">_eMethod_</span></span>
  
> <span data-ttu-id="f3a18-114">in Gibt die zu überprüfende Methode an.</span><span class="sxs-lookup"><span data-stu-id="f3a18-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="f3a18-115">_First_</span><span class="sxs-lookup"><span data-stu-id="f3a18-115">_First_</span></span>
  
> <span data-ttu-id="f3a18-116">in Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="f3a18-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f3a18-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3a18-117">Return value</span></span>

<span data-ttu-id="f3a18-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3a18-118">S_OK</span></span> 
  
> <span data-ttu-id="f3a18-119">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3a18-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3a18-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3a18-120">Remarks</span></span>

<span data-ttu-id="f3a18-121">Im Gegensatz zu den Makros [ValidateParms](validateparms.md) und [UlValidateParms](ulvalidateparms.md) führt das **CheckParms** -Makro keine vollständige Parameterüberprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="f3a18-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="f3a18-122">Parameter, die zwischen MAPI-und Dienstanbietern übergeben werden, werden als richtig angenommen, daher führt **CheckParms** nur eine Debug-Validierung aus.</span><span class="sxs-lookup"><span data-stu-id="f3a18-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

