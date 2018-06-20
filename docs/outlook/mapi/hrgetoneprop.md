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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4dcdce72781669988a0cb15eb9b3a7cd73494bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791938"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="2b1ab-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="2b1ab-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="2b1ab-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2b1ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2b1ab-105">Ruft den Wert einer Eigenschaft von einer Eigenschaft Oberfläche, d. h., eine Schnittstelle abgeleitet [IMAPIProp](imapipropiunknown.md)ab.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b1ab-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2b1ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="2b1ab-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2b1ab-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2b1ab-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2b1ab-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2b1ab-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2b1ab-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2b1ab-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2b1ab-110">Called by:</span></span>  <br/> |<span data-ttu-id="2b1ab-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="2b1ab-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="2b1ab-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b1ab-112">Parameters</span></span>

 <span data-ttu-id="2b1ab-113">_PMP_</span><span class="sxs-lookup"><span data-stu-id="2b1ab-113">_pmp_</span></span>
  
> <span data-ttu-id="2b1ab-114">[in] Zeiger auf die [IMAPIProp](imapipropiunknown.md) -Schnittstelle, die von der Wert der Eigenschaft ist abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="2b1ab-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="2b1ab-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="2b1ab-116">[in] Eigenschaftentag der Eigenschaft abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="2b1ab-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="2b1ab-117">_ppprop_</span></span>
  
> <span data-ttu-id="2b1ab-118">[out] Zeiger auf einen Zeiger auf die zurückgegebene [SPropValue](spropvalue.md) -Struktur, die den Wert der abgerufenen-Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2b1ab-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="2b1ab-119">Return value</span></span>

<span data-ttu-id="2b1ab-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2b1ab-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2b1ab-121">Die angeforderte-Eigenschaft ist von der angegebenen Schnittstelle nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2b1ab-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b1ab-122">Remarks</span></span>

<span data-ttu-id="2b1ab-123">Im Gegensatz zu der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode gibt die **HrGetOneProp** -Funktion nie eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="2b1ab-124">Da es nur eine Eigenschaft abruft, es einfach entweder Erfolg oder Fehler.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="2b1ab-125">Zum Abrufen von mehreren Eigenschaften, ist **GetProps** schneller.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="2b1ab-126">Sie können festlegen oder ändern eine einzelne Eigenschaft mit der [HrSetOneProp](hrsetoneprop.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2b1ab-127">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="2b1ab-127">MFCMAPI reference</span></span>

<span data-ttu-id="2b1ab-128">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2b1ab-129">**Datei**</span><span class="sxs-lookup"><span data-stu-id="2b1ab-129">**File**</span></span>|<span data-ttu-id="2b1ab-130">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="2b1ab-130">**Function**</span></span>|<span data-ttu-id="2b1ab-131">**Comment**</span><span class="sxs-lookup"><span data-stu-id="2b1ab-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2b1ab-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="2b1ab-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2b1ab-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="2b1ab-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="2b1ab-134">MFCMAPI (engl.) wird die **HrGetOneProp** -Methode verwendet, um den Typ eines Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b1ab-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b1ab-135">See also</span></span>



[<span data-ttu-id="2b1ab-136">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="2b1ab-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

