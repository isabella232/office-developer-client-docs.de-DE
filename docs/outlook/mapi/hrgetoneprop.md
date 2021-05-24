---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 95273bf6025d6ef995d7c21c0e44bdbbf59072f6
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589173"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="a824e-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="a824e-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="a824e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a824e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a824e-105">Ruft den Wert einer einzelnen Eigenschaft von einer Eigenschaftenschnittstelle ab, d. h. einer Schnittstelle, die von [IMAPIProp abgeleitet ist.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="a824e-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a824e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a824e-106">Header file:</span></span>  <br/> |<span data-ttu-id="a824e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a824e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a824e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a824e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a824e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a824e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a824e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a824e-110">Called by:</span></span>  <br/> |<span data-ttu-id="a824e-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a824e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="a824e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a824e-112">Parameters</span></span>

 <span data-ttu-id="a824e-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="a824e-113">_pmp_</span></span>
  
> <span data-ttu-id="a824e-114">[in] Zeiger auf die [IMAPIProp-Schnittstelle,](imapipropiunknown.md) von der der Eigenschaftswert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a824e-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="a824e-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="a824e-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="a824e-116">[in] Eigenschaftstag der abzurufende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a824e-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="a824e-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="a824e-117">_ppprop_</span></span>
  
> <span data-ttu-id="a824e-118">[out] Zeiger auf einen Zeiger auf die [zurückgegebene SPropValue-Struktur,](spropvalue.md) die den abgerufenen Eigenschaftswert definiert.</span><span class="sxs-lookup"><span data-stu-id="a824e-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a824e-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a824e-119">Return value</span></span>

<span data-ttu-id="a824e-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a824e-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a824e-121">Die angeforderte Eigenschaft ist nicht über die angegebene Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a824e-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a824e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a824e-122">Remarks</span></span>

<span data-ttu-id="a824e-123">Im Gegensatz zur [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) gibt die **HrGetOneProp-Funktion** nie eine Warnung zurück.</span><span class="sxs-lookup"><span data-stu-id="a824e-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="a824e-124">Da nur eine Eigenschaft abgerufen wird, ist sie einfach erfolgreich oder schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="a824e-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="a824e-125">Zum Abrufen mehrerer Eigenschaften ist **GetProps** schneller.</span><span class="sxs-lookup"><span data-stu-id="a824e-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="a824e-126">Sie können eine einzelne Eigenschaft mit der [HrSetOneProp-Funktion](hrsetoneprop.md) festlegen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="a824e-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a824e-127">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a824e-127">MFCMAPI reference</span></span>

<span data-ttu-id="a824e-128">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a824e-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a824e-129">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a824e-129">**File**</span></span>|<span data-ttu-id="a824e-130">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a824e-130">**Function**</span></span>|<span data-ttu-id="a824e-131">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a824e-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a824e-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a824e-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a824e-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="a824e-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="a824e-134">MFCMAPI verwendet die **HrGetOneProp-Methode,** um den Typ eines Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a824e-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a824e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a824e-135">See also</span></span>



[<span data-ttu-id="a824e-136">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a824e-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

