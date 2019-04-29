---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416902"
---
# <a name="ulpropsize"></a><span data-ttu-id="4b711-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="4b711-103">UlPropSize</span></span>

  
  
<span data-ttu-id="4b711-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b711-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b711-105">Gibt die Größe eines einzelnen Eigenschaftswerts zurück.</span><span class="sxs-lookup"><span data-stu-id="4b711-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b711-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4b711-106">Header file:</span></span>  <br/> |<span data-ttu-id="4b711-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4b711-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4b711-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="4b711-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4b711-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4b711-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4b711-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="4b711-110">Called by:</span></span>  <br/> |<span data-ttu-id="4b711-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="4b711-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="4b711-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b711-112">Parameters</span></span>

 <span data-ttu-id="4b711-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="4b711-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="4b711-114">in Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die die zu messende Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="4b711-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4b711-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b711-115">Return value</span></span>

<span data-ttu-id="4b711-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b711-116">S_OK</span></span> 
  
> <span data-ttu-id="4b711-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="4b711-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="4b711-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="4b711-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="4b711-119">Der Vorgang konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="4b711-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b711-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b711-120">Remarks</span></span>

<span data-ttu-id="4b711-121">Die **UlPropSize** -Funktion gibt die Größe des Eigenschaftswerts für die angegebene Eigenschaft in Byte zurück.</span><span class="sxs-lookup"><span data-stu-id="4b711-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="4b711-122">Die Größe des Rests der **SPropValue** -Struktur wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4b711-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

