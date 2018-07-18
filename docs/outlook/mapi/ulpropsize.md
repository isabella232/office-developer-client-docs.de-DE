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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bc00270b167c9f7317fa466d790d5020d961676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795774"
---
# <a name="ulpropsize"></a><span data-ttu-id="4803e-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="4803e-103">UlPropSize</span></span>

  
  
<span data-ttu-id="4803e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4803e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4803e-105">Gibt die Größe des einen einzelnen Eigenschaftswert zurück.</span><span class="sxs-lookup"><span data-stu-id="4803e-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4803e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4803e-106">Header file:</span></span>  <br/> |<span data-ttu-id="4803e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4803e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4803e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="4803e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4803e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4803e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4803e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="4803e-110">Called by:</span></span>  <br/> |<span data-ttu-id="4803e-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="4803e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="4803e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4803e-112">Parameters</span></span>

 <span data-ttu-id="4803e-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="4803e-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="4803e-114">[in] Zeiger auf eine [SPropValue](spropvalue.md) -Struktur definieren die Eigenschaft gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4803e-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4803e-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="4803e-115">Return value</span></span>

<span data-ttu-id="4803e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4803e-116">S_OK</span></span> 
  
> <span data-ttu-id="4803e-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="4803e-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="4803e-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="4803e-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="4803e-119">Ein Fehler unerwartete oder unbekannten Ursprungs verhindert den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="4803e-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4803e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4803e-120">Remarks</span></span>

<span data-ttu-id="4803e-121">Die **UlPropSize** -Funktion gibt die Größe der Wert der Eigenschaft um für die angegebene Eigenschaft in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="4803e-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="4803e-122">Es ignoriert die Größe des den Rest der **SPropValue** Struktur.</span><span class="sxs-lookup"><span data-stu-id="4803e-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

