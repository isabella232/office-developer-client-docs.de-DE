---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 31d2be027ef3b58fdd44e71c922677164d352feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569127"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="815d3-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="815d3-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="815d3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="815d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="815d3-105">Legt fest oder ändert den Wert einer einzelnen Eigenschaft für eine Eigenschaft Schnittstelle, d. h., eine Schnittstelle [IMAPIProp](imapipropiunknown.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="815d3-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="815d3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="815d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="815d3-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="815d3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="815d3-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="815d3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="815d3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="815d3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="815d3-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="815d3-110">Called by:</span></span>  <br/> |<span data-ttu-id="815d3-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="815d3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="815d3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="815d3-112">Parameters</span></span>

 <span data-ttu-id="815d3-113">_PMP_</span><span class="sxs-lookup"><span data-stu-id="815d3-113">_pmp_</span></span>
  
> <span data-ttu-id="815d3-114">[in] Zeiger auf eine [IMAPIProp](imapipropiunknown.md) -Schnittstelle, die auf der Wert der Eigenschaft ist festgelegt oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="815d3-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="815d3-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="815d3-115">_pprop_</span></span>
  
> <span data-ttu-id="815d3-116">[in] Zeiger auf die [SPropValue](spropvalue.md) -Struktur definiert, des Werts der _Pmp_ -Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="815d3-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="815d3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="815d3-117">Return value</span></span>

<span data-ttu-id="815d3-118">None.</span><span class="sxs-lookup"><span data-stu-id="815d3-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="815d3-119">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="815d3-119">Remarks</span></span>

<span data-ttu-id="815d3-120">Im Gegensatz zu der [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode gibt die **HrSetOneProp** Funktion nie alle Warnungen.</span><span class="sxs-lookup"><span data-stu-id="815d3-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="815d3-121">Da nur eine Eigenschaft festgelegt, es einfach entweder Erfolg oder Fehler.</span><span class="sxs-lookup"><span data-stu-id="815d3-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="815d3-122">Für die Einstellung oder mehrere Eigenschaften ändern ist **SetProps** schneller.</span><span class="sxs-lookup"><span data-stu-id="815d3-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="815d3-123">Sie können eine einzelne Eigenschaft mit der Funktion [HrGetOneProp](hrgetoneprop.md) abrufen.</span><span class="sxs-lookup"><span data-stu-id="815d3-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

