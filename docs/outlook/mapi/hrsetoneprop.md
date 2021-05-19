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
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417658"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="f3ef7-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="f3ef7-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="f3ef7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3ef7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3ef7-105">Legt fest oder ändert den Wert einer einzelnen Eigenschaft auf einer Eigenschaftenschnittstelle, d. h. einer Schnittstelle, die von [IMAPIProp abgeleitet ist.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="f3ef7-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3ef7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f3ef7-106">Header file:</span></span>  <br/> |<span data-ttu-id="f3ef7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f3ef7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f3ef7-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f3ef7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f3ef7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f3ef7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f3ef7-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f3ef7-110">Called by:</span></span>  <br/> |<span data-ttu-id="f3ef7-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f3ef7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="f3ef7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3ef7-112">Parameters</span></span>

 <span data-ttu-id="f3ef7-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="f3ef7-113">_pmp_</span></span>
  
> <span data-ttu-id="f3ef7-114">[in] Zeiger auf eine [IMAPIProp-Schnittstelle,](imapipropiunknown.md) auf der der Eigenschaftswert festgelegt oder geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3ef7-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="f3ef7-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="f3ef7-115">_pprop_</span></span>
  
> <span data-ttu-id="f3ef7-116">[in] Zeiger auf die [SPropValue-Struktur,](spropvalue.md) die den wert definiert, der für die  _pmp-Eigenschaft festgelegt werden_ soll.</span><span class="sxs-lookup"><span data-stu-id="f3ef7-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f3ef7-117">Return value</span><span class="sxs-lookup"><span data-stu-id="f3ef7-117">Return value</span></span>

<span data-ttu-id="f3ef7-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="f3ef7-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f3ef7-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f3ef7-119">Remarks</span></span>

<span data-ttu-id="f3ef7-120">Im Gegensatz zur [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) gibt die **HrSetOneProp-Funktion** keine Warnungen zurück.</span><span class="sxs-lookup"><span data-stu-id="f3ef7-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="f3ef7-121">Da nur eine Eigenschaft definiert wird, ist sie einfach erfolgreich oder schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="f3ef7-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="f3ef7-122">Zum Festlegen oder Ändern mehrerer Eigenschaften ist **SetProps** schneller.</span><span class="sxs-lookup"><span data-stu-id="f3ef7-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="f3ef7-123">Sie können eine einzelne Eigenschaft mit der [HrGetOneProp-Funktion](hrgetoneprop.md) abrufen.</span><span class="sxs-lookup"><span data-stu-id="f3ef7-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

