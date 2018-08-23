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
ms.openlocfilehash: 0985ed0c5d4482bb22f46bdc9198afc343c61e5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565536"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="a8433-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="a8433-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="a8433-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8433-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8433-105">Vergleicht zwei Eigenschaftswerte, um festzustellen, ob diese gleich sind.</span><span class="sxs-lookup"><span data-stu-id="a8433-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8433-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a8433-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8433-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a8433-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a8433-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a8433-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8433-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a8433-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a8433-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a8433-110">Called by:</span></span>  <br/> |<span data-ttu-id="a8433-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a8433-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="a8433-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8433-112">Parameters</span></span>

 <span data-ttu-id="a8433-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="a8433-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="a8433-114">[in] Zeiger auf eine [SPropValue](spropvalue.md) -Struktur definieren den ersten Eigenschaftswert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8433-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="a8433-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="a8433-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="a8433-116">[in] Zeiger auf eine **SPropValue** -Struktur definieren den zweiten Eigenschaftswert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8433-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a8433-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a8433-117">Return value</span></span>

 <span data-ttu-id="a8433-118">**LPropCompareProp** gibt einen der folgenden Werte für die meisten Eigenschaftentypen zurück:</span><span class="sxs-lookup"><span data-stu-id="a8433-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="a8433-119">Kleiner als 0 (null) ist der Parameter _LpSPropValueA_ , wenn der Wert von angegebenen kleiner ist als der durch den Parameter _LpSPropValueB_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="a8433-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="a8433-120">Größer als 0 (null), wenn der Wert von _LpSPropValueA_ angegebene ist größer als der mit _LpSPropValueB_angegeben.</span><span class="sxs-lookup"><span data-stu-id="a8433-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="a8433-121">0 (null), wenn der Wert von _LpSPropValueA_ angegebene gleich den durch _LpSPropValueB_angegebenen Wert ist.</span><span class="sxs-lookup"><span data-stu-id="a8433-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="a8433-122">Für Eigenschaftentypen, die keine systeminterne Sortierung, wie etwa boolescher Wert haben oder Fehlertypen, gibt die **LPropCompareProp** -Funktion einen nicht definierten Wert zurück, wenn die zwei Werte nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="a8433-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="a8433-123">Dieser Wert nicht definierte sind ungleich NULL und konsistent Anrufe.</span><span class="sxs-lookup"><span data-stu-id="a8433-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a8433-124">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a8433-124">Remarks</span></span>

<span data-ttu-id="a8433-125">Verwenden Sie die **LPropCompareProp** -Funktion nur, wenn die Typen der beiden Eigenschaften, die verglichen werden identisch sind.</span><span class="sxs-lookup"><span data-stu-id="a8433-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="a8433-126">Vor dem Aufruf von **LPropCompareProp**, muss eine Clientanwendung oder Dienstanbieter zunächst die Eigenschaften für den Vergleich mit einem Aufruf der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="a8433-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="a8433-127">Der Vergleich von Eigenschaftswerten ist gültig, wenn ein Client oder Anbieter Anrufe **LPropCompareProp**, die Funktion zuerst die Eigenschaftentags, um sicherzustellen, dass untersucht.</span><span class="sxs-lookup"><span data-stu-id="a8433-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="a8433-128">Die Funktion vergleicht dann die Eigenschaftswerte, die einen entsprechenden Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a8433-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="a8433-129">Wenn die Werte ungleich sind, bestimmt **LPropCompareProp** an, welche größer ist.</span><span class="sxs-lookup"><span data-stu-id="a8433-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="a8433-130">Die Eigenschaften, die **LPropCompareProp** vergleicht müssen nicht auf das gleiche Objekt gehören.</span><span class="sxs-lookup"><span data-stu-id="a8433-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

