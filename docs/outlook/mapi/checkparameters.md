---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a693c06d933c7e93d384aac8da8d5311eaf1d9da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791438"
---
# <a name="checkparameters"></a><span data-ttu-id="5168b-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="5168b-103">CheckParameters</span></span>

  
  
<span data-ttu-id="5168b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5168b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5168b-105">Ruft eine interne Funktion zum debugging Parameter für Webdienstmethoden aufgerufen von MAPI-Anbieter zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5168b-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5168b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5168b-106">Header file:</span></span>  <br/> |<span data-ttu-id="5168b-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="5168b-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="5168b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5168b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5168b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5168b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5168b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5168b-110">Called by:</span></span>  <br/> |<span data-ttu-id="5168b-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5168b-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="5168b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5168b-112">Parameters</span></span>

 <span data-ttu-id="5168b-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="5168b-113">_eMethod_</span></span>
  
> <span data-ttu-id="5168b-114">[in] Gibt den-Enumeration zurück, die-Methode, um zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5168b-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="5168b-115">_Erster_</span><span class="sxs-lookup"><span data-stu-id="5168b-115">_First_</span></span>
  
> <span data-ttu-id="5168b-116">[in] Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="5168b-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5168b-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5168b-117">Return value</span></span>

<span data-ttu-id="5168b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="5168b-118">S_OK</span></span> 
  
> <span data-ttu-id="5168b-119">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5168b-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5168b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5168b-120">Remarks</span></span>

<span data-ttu-id="5168b-121">Das Makro **CheckParameters** wurde durch das Makro [CheckParms](checkparms.md) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="5168b-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="5168b-122">**CheckParms** wird auf allen Plattformen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5168b-122">**CheckParms** is recommended on all platforms.</span></span> 
  

