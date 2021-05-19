---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414613"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="ee9b8-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="ee9b8-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="ee9b8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee9b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee9b8-105">Vergleicht zwei Eigenschaftswerte, um zu bestimmen, ob sie gleich sind.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee9b8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ee9b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="ee9b8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ee9b8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ee9b8-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ee9b8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ee9b8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ee9b8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ee9b8-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ee9b8-110">Called by:</span></span>  <br/> |<span data-ttu-id="ee9b8-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ee9b8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="ee9b8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee9b8-112">Parameters</span></span>

 <span data-ttu-id="ee9b8-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="ee9b8-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="ee9b8-114">[in] Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die den ersten zu vergleichenden Eigenschaftswert definiert.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="ee9b8-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="ee9b8-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="ee9b8-116">[in] Zeiger auf eine **SPropValue-Struktur,** die den zweiten zu vergleichenden Eigenschaftswert definiert.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ee9b8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee9b8-117">Return value</span></span>

 <span data-ttu-id="ee9b8-118">**LPropCompareProp** gibt einen der folgenden Werte für die meisten Eigenschaftstypen zurück:</span><span class="sxs-lookup"><span data-stu-id="ee9b8-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="ee9b8-119">Kleiner als Null, wenn der vom  _lpSPropValueA-Parameter_ angegebene Wert kleiner als der wert ist, der durch den  _lpSPropValueB-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="ee9b8-120">Größer als Null, wenn der von  _lpSPropValueA_ angegebene Wert größer als der von  _lpSPropValueB_ angegebene Wert ist.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="ee9b8-121">Null, wenn der von _lpSPropValueA_ angegebene Wert dem von _lpSPropValueB angegebenen Wert entspricht._</span><span class="sxs-lookup"><span data-stu-id="ee9b8-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="ee9b8-122">Bei Eigenschaftstypen ohne systeminterne Sortierung, z. B. Boolean- oder Fehlertypen, gibt die **LPropCompareProp-Funktion** einen nicht definierten Wert zurück, wenn die beiden Eigenschaftswerte nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="ee9b8-123">Dieser undefined-Wert ist ungleich Null und für alle Aufrufe konsistent.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ee9b8-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee9b8-124">Remarks</span></span>

<span data-ttu-id="ee9b8-125">Verwenden Sie **die LPropCompareProp-Funktion** nur, wenn die Typen der beiden zu vergleichenden Eigenschaften identisch sind.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="ee9b8-126">Vor dem Aufrufen **von LPropCompareProp** muss eine Clientanwendung oder ein Dienstanbieter zuerst die Eigenschaften für den Vergleich mit einem Aufruf der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) abrufen.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="ee9b8-127">Wenn ein Client oder Anbieter **LPropCompareProp** aufruft, untersucht die Funktion zunächst die Eigenschaftstags, um sicherzustellen, dass der Vergleich der Eigenschaftswerte gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="ee9b8-128">Die Funktion vergleicht dann die Eigenschaftswerte und gibt einen entsprechenden Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="ee9b8-129">Wenn die Eigenschaftswerte ungleichmäßig sind, **bestimmt LPropCompareProp,** welcher der größere ist.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="ee9b8-130">Die Eigenschaften, **die LPropCompareProp** vergleicht, müssen nicht zum gleichen Objekt gehören.</span><span class="sxs-lookup"><span data-stu-id="ee9b8-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

