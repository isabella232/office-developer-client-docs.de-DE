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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a922b8bb21bfd534935d4d1706a6ccfd15c2da5c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433395"
---
# <a name="checkparameters"></a><span data-ttu-id="a64ed-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="a64ed-103">CheckParameters</span></span>

  
  
<span data-ttu-id="a64ed-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a64ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a64ed-105">Ruft eine interne Funktion auf, um debuggingparameter für Dienstanbieter Methoden zu überprüfen, die von MAPI aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a64ed-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a64ed-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="a64ed-106">Header file:</span></span>  <br/> |<span data-ttu-id="a64ed-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="a64ed-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="a64ed-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a64ed-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a64ed-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a64ed-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a64ed-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a64ed-110">Called by:</span></span>  <br/> |<span data-ttu-id="a64ed-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a64ed-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="a64ed-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a64ed-112">Parameters</span></span>

 <span data-ttu-id="a64ed-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="a64ed-113">_eMethod_</span></span>
  
> <span data-ttu-id="a64ed-114">in Gibt die zu überprüfende Methode an.</span><span class="sxs-lookup"><span data-stu-id="a64ed-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="a64ed-115">_First_</span><span class="sxs-lookup"><span data-stu-id="a64ed-115">_First_</span></span>
  
> <span data-ttu-id="a64ed-116">in Zeiger auf das erste Argument im Stapel.</span><span class="sxs-lookup"><span data-stu-id="a64ed-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a64ed-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a64ed-117">Return value</span></span>

<span data-ttu-id="a64ed-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a64ed-118">S_OK</span></span> 
  
> <span data-ttu-id="a64ed-119">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a64ed-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a64ed-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a64ed-120">Remarks</span></span>

<span data-ttu-id="a64ed-121">Das **CheckParameters** -Makro wurde vom [CheckParms](checkparms.md) -Makro abgelöst.</span><span class="sxs-lookup"><span data-stu-id="a64ed-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="a64ed-122">**CheckParms** wird auf allen Plattformen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="a64ed-122">**CheckParms** is recommended on all platforms.</span></span> 
  

