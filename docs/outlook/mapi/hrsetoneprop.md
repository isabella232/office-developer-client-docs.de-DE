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
# <a name="hrsetoneprop"></a><span data-ttu-id="19ad5-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="19ad5-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="19ad5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19ad5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19ad5-105">Legt den Wert einer einzelnen Eigenschaft für eine Eigenschaften Schnittstelle fest oder ändert Sie, also eine von [IMAPIProp](imapipropiunknown.md)abgeleitete Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="19ad5-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19ad5-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="19ad5-106">Header file:</span></span>  <br/> |<span data-ttu-id="19ad5-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="19ad5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="19ad5-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="19ad5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="19ad5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="19ad5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="19ad5-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="19ad5-110">Called by:</span></span>  <br/> |<span data-ttu-id="19ad5-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="19ad5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="19ad5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="19ad5-112">Parameters</span></span>

 <span data-ttu-id="19ad5-113">_PMP_</span><span class="sxs-lookup"><span data-stu-id="19ad5-113">_pmp_</span></span>
  
> <span data-ttu-id="19ad5-114">in Zeiger auf eine [IMAPIProp](imapipropiunknown.md) -Schnittstelle, auf der der Eigenschaftswert festgelegt oder geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="19ad5-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="19ad5-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="19ad5-115">_pprop_</span></span>
  
> <span data-ttu-id="19ad5-116">in Zeiger auf die [SPropValue](spropvalue.md) -Struktur, die den Wert definiert, der für die _PMP_ -Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="19ad5-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="19ad5-117">Return value</span><span class="sxs-lookup"><span data-stu-id="19ad5-117">Return value</span></span>

<span data-ttu-id="19ad5-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="19ad5-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19ad5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19ad5-119">Remarks</span></span>

<span data-ttu-id="19ad5-120">Im Gegensatz zur [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode gibt die **HrSetOneProp** -Funktion nie Warnungen zurück.</span><span class="sxs-lookup"><span data-stu-id="19ad5-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="19ad5-121">Da nur eine Eigenschaft festgelegt wird, wird Sie entweder erfolgreich ausgeführt oder schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="19ad5-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="19ad5-122">Zum Festlegen oder ändern mehrerer Eigenschaften ist \*\*\*\* SetProps schneller.</span><span class="sxs-lookup"><span data-stu-id="19ad5-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="19ad5-123">Sie können eine einzelne Eigenschaft mit der [HrGetOneProp](hrgetoneprop.md) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="19ad5-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

