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
ms.openlocfilehash: 8af0d5c6eaff0c1e01e01c24c46f299e0c637f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791943"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="69c1b-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="69c1b-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="69c1b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69c1b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69c1b-105">Legt fest oder ändert den Wert einer einzelnen Eigenschaft für eine Eigenschaft Schnittstelle, d. h., eine Schnittstelle [IMAPIProp](imapipropiunknown.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="69c1b-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69c1b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="69c1b-106">Header file:</span></span>  <br/> |<span data-ttu-id="69c1b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="69c1b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="69c1b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="69c1b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="69c1b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="69c1b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="69c1b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="69c1b-110">Called by:</span></span>  <br/> |<span data-ttu-id="69c1b-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="69c1b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="69c1b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="69c1b-112">Parameters</span></span>

 <span data-ttu-id="69c1b-113">_PMP_</span><span class="sxs-lookup"><span data-stu-id="69c1b-113">_pmp_</span></span>
  
> <span data-ttu-id="69c1b-114">[in] Zeiger auf eine [IMAPIProp](imapipropiunknown.md) -Schnittstelle, die auf der Wert der Eigenschaft ist festgelegt oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="69c1b-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="69c1b-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="69c1b-115">_pprop_</span></span>
  
> <span data-ttu-id="69c1b-116">[in] Zeiger auf die [SPropValue](spropvalue.md) -Struktur definiert, des Werts der _Pmp_ -Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="69c1b-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="69c1b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69c1b-117">Return value</span></span>

<span data-ttu-id="69c1b-118">None.</span><span class="sxs-lookup"><span data-stu-id="69c1b-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69c1b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69c1b-119">Remarks</span></span>

<span data-ttu-id="69c1b-120">Im Gegensatz zu der [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode gibt die **HrSetOneProp** Funktion nie alle Warnungen.</span><span class="sxs-lookup"><span data-stu-id="69c1b-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="69c1b-121">Da nur eine Eigenschaft festgelegt, es einfach entweder Erfolg oder Fehler.</span><span class="sxs-lookup"><span data-stu-id="69c1b-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="69c1b-122">Für die Einstellung oder mehrere Eigenschaften ändern ist **SetProps** schneller.</span><span class="sxs-lookup"><span data-stu-id="69c1b-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="69c1b-123">Sie können eine einzelne Eigenschaft mit der Funktion [HrGetOneProp](hrgetoneprop.md) abrufen.</span><span class="sxs-lookup"><span data-stu-id="69c1b-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

