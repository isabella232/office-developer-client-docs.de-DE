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
ms.openlocfilehash: e5adc7d0c317d8b803645d78227777998d7d241f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347838"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="85b8a-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="85b8a-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="85b8a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85b8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85b8a-105">Ruft den Wert einer einzelnen Eigenschaft von einer Eigenschaften Schnittstelle ab, also einer von [IMAPIProp](imapipropiunknown.md)abgeleiteten Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="85b8a-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85b8a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="85b8a-106">Header file:</span></span>  <br/> |<span data-ttu-id="85b8a-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="85b8a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="85b8a-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="85b8a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="85b8a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="85b8a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="85b8a-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="85b8a-110">Called by:</span></span>  <br/> |<span data-ttu-id="85b8a-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="85b8a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="85b8a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="85b8a-112">Parameters</span></span>

 <span data-ttu-id="85b8a-113">_PMP_</span><span class="sxs-lookup"><span data-stu-id="85b8a-113">_pmp_</span></span>
  
> <span data-ttu-id="85b8a-114">in Zeiger auf die [IMAPIProp](imapipropiunknown.md) -Schnittstelle, von der der Eigenschaftswert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="85b8a-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="85b8a-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="85b8a-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="85b8a-116">in Property-Tag der Eigenschaft, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="85b8a-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="85b8a-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="85b8a-117">_ppprop_</span></span>
  
> <span data-ttu-id="85b8a-118">Out Zeiger auf einen Zeiger auf die zurückgegebene [SPropValue](spropvalue.md) -Struktur, die den abgerufenen Eigenschaftswert definiert.</span><span class="sxs-lookup"><span data-stu-id="85b8a-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85b8a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85b8a-119">Return value</span></span>

<span data-ttu-id="85b8a-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="85b8a-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="85b8a-121">Die angeforderte Eigenschaft ist nicht über die angegebene Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="85b8a-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85b8a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85b8a-122">Remarks</span></span>

<span data-ttu-id="85b8a-123">Im Gegensatz zur [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode gibt die **HrGetOneProp** -Funktion nie eine Warnung zurück.</span><span class="sxs-lookup"><span data-stu-id="85b8a-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="85b8a-124">Da nur eine Eigenschaft abgerufen wird, ist Sie entweder erfolgreich oder schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="85b8a-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="85b8a-125">Zum Abrufen mehrerer Eigenschaften ist getProps schneller. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="85b8a-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="85b8a-126">Sie können eine einzelne Eigenschaft mit der [HrSetOneProp](hrsetoneprop.md) -Funktion festlegen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="85b8a-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="85b8a-127">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="85b8a-127">MFCMAPI reference</span></span>

<span data-ttu-id="85b8a-128">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="85b8a-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="85b8a-129">**Datei**</span><span class="sxs-lookup"><span data-stu-id="85b8a-129">**File**</span></span>|<span data-ttu-id="85b8a-130">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="85b8a-130">**Function**</span></span>|<span data-ttu-id="85b8a-131">**Comment**</span><span class="sxs-lookup"><span data-stu-id="85b8a-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="85b8a-132">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="85b8a-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="85b8a-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="85b8a-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="85b8a-134">MFCMAPI verwendet die **HrGetOneProp** -Methode, um den Typ eines Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="85b8a-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85b8a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85b8a-135">See also</span></span>



[<span data-ttu-id="85b8a-136">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="85b8a-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

