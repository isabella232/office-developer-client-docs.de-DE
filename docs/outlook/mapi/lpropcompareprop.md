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
ms.openlocfilehash: d214cb5d449e2f7e42e7ee72774fdc146495adb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792922"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="f7c43-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="f7c43-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="f7c43-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7c43-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7c43-105">Vergleicht zwei Eigenschaftswerte, um festzustellen, ob diese gleich sind.</span><span class="sxs-lookup"><span data-stu-id="f7c43-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7c43-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f7c43-106">Header file:</span></span>  <br/> |<span data-ttu-id="f7c43-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f7c43-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f7c43-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f7c43-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f7c43-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f7c43-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f7c43-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f7c43-110">Called by:</span></span>  <br/> |<span data-ttu-id="f7c43-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f7c43-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="f7c43-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7c43-112">Parameters</span></span>

 <span data-ttu-id="f7c43-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="f7c43-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="f7c43-114">[in] Zeiger auf eine [SPropValue](spropvalue.md) -Struktur definieren den ersten Eigenschaftswert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7c43-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="f7c43-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="f7c43-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="f7c43-116">[in] Zeiger auf eine **SPropValue** -Struktur definieren den zweiten Eigenschaftswert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7c43-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f7c43-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7c43-117">Return value</span></span>

 <span data-ttu-id="f7c43-118">**LPropCompareProp** gibt einen der folgenden Werte für die meisten Eigenschaftentypen zurück:</span><span class="sxs-lookup"><span data-stu-id="f7c43-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="f7c43-119">Kleiner als 0 (null) ist der Parameter _LpSPropValueA_ , wenn der Wert von angegebenen kleiner ist als der durch den Parameter _LpSPropValueB_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="f7c43-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="f7c43-120">Größer als 0 (null), wenn der Wert von _LpSPropValueA_ angegebene ist größer als der mit _LpSPropValueB_angegeben.</span><span class="sxs-lookup"><span data-stu-id="f7c43-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="f7c43-121">0 (null), wenn der Wert von _LpSPropValueA_ angegebene gleich den durch _LpSPropValueB_angegebenen Wert ist.</span><span class="sxs-lookup"><span data-stu-id="f7c43-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="f7c43-122">Für Eigenschaftentypen, die keine systeminterne Sortierung, wie etwa boolescher Wert haben oder Fehlertypen, gibt die **LPropCompareProp** -Funktion einen nicht definierten Wert zurück, wenn die zwei Werte nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="f7c43-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="f7c43-123">Dieser Wert nicht definierte sind ungleich NULL und konsistent Anrufe.</span><span class="sxs-lookup"><span data-stu-id="f7c43-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f7c43-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7c43-124">Remarks</span></span>

<span data-ttu-id="f7c43-125">Verwenden Sie die **LPropCompareProp** -Funktion nur, wenn die Typen der beiden Eigenschaften, die verglichen werden identisch sind.</span><span class="sxs-lookup"><span data-stu-id="f7c43-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="f7c43-126">Vor dem Aufruf von **LPropCompareProp**, muss eine Clientanwendung oder Dienstanbieter zunächst die Eigenschaften für den Vergleich mit einem Aufruf der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="f7c43-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="f7c43-127">Der Vergleich von Eigenschaftswerten ist gültig, wenn ein Client oder Anbieter Anrufe **LPropCompareProp**, die Funktion zuerst die Eigenschaftentags, um sicherzustellen, dass untersucht.</span><span class="sxs-lookup"><span data-stu-id="f7c43-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="f7c43-128">Die Funktion vergleicht dann die Eigenschaftswerte, die einen entsprechenden Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f7c43-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="f7c43-129">Wenn die Werte ungleich sind, bestimmt **LPropCompareProp** an, welche größer ist.</span><span class="sxs-lookup"><span data-stu-id="f7c43-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="f7c43-130">Die Eigenschaften, die **LPropCompareProp** vergleicht müssen nicht auf das gleiche Objekt gehören.</span><span class="sxs-lookup"><span data-stu-id="f7c43-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

