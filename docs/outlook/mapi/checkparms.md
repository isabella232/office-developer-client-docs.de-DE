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
ms.openlocfilehash: 5732dd3c1587c127cf153ebcadd9b791e6abb9ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582035"
---
# <a name="checkparms"></a><span data-ttu-id="8ea22-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="8ea22-103">CheckParms</span></span>

  
  
<span data-ttu-id="8ea22-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ea22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ea22-105">Ruft eine interne Funktion zum debugging Parameter für Webdienstmethoden aufgerufen von MAPI-Anbieter zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8ea22-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ea22-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8ea22-106">Header file:</span></span>  <br/> |<span data-ttu-id="8ea22-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="8ea22-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="8ea22-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8ea22-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8ea22-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8ea22-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8ea22-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8ea22-110">Called by:</span></span>  <br/> |<span data-ttu-id="8ea22-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="8ea22-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="8ea22-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ea22-112">Parameters</span></span>

 <span data-ttu-id="8ea22-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="8ea22-113">_eMethod_</span></span>
  
> <span data-ttu-id="8ea22-114">[in] Gibt den-Enumeration zurück, die-Methode, um zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8ea22-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="8ea22-115">_Erster_</span><span class="sxs-lookup"><span data-stu-id="8ea22-115">_First_</span></span>
  
> <span data-ttu-id="8ea22-116">[in] Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="8ea22-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8ea22-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8ea22-117">Return value</span></span>

<span data-ttu-id="8ea22-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ea22-118">S_OK</span></span> 
  
> <span data-ttu-id="8ea22-119">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8ea22-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8ea22-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ea22-120">Remarks</span></span>

<span data-ttu-id="8ea22-121">Im Gegensatz zu den [ValidateParms](validateparms.md) und [UlValidateParms](ulvalidateparms.md) Makros führt das Makro **CheckParms** keine vollständige Parameter Überprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="8ea22-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="8ea22-122">Übergeben Sie Parameter zwischen MAPI- und Service Provider wird angenommen, dass richtig sein, damit **CheckParms** nur eine Debug-Überprüfung durchführt.</span><span class="sxs-lookup"><span data-stu-id="8ea22-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

