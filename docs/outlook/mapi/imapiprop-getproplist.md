---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5417853dbb1fa87d2beead2f73ca57329e17b044
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571122"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="7871a-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="7871a-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="7871a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7871a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7871a-105">Eigenschaftentags für alle Eigenschaften zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7871a-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="7871a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7871a-106">Parameters</span></span>

 <span data-ttu-id="7871a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7871a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7871a-108">[in] Eine Bitmaske aus Flags, die das Format für die Zeichenfolgen in der zurückgegebenen Eigenschaftentags steuert.</span><span class="sxs-lookup"><span data-stu-id="7871a-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="7871a-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7871a-109">The following flag can be set:</span></span>
    
<span data-ttu-id="7871a-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7871a-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7871a-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="7871a-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="7871a-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="7871a-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7871a-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="7871a-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="7871a-114">[out] Ein Zeiger auf einen Zeiger auf die Eigenschaft Tag-Array, das für alle Eigenschaften des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="7871a-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7871a-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7871a-115">Return value</span></span>

<span data-ttu-id="7871a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7871a-116">S_OK</span></span> 
  
> <span data-ttu-id="7871a-117">Alle Eigenschaftentags wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7871a-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="7871a-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7871a-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7871a-119">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="7871a-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7871a-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7871a-120">Remarks</span></span>

<span data-ttu-id="7871a-121">Die **IMAPIProp::GetPropList** -Methode ruft das Eigenschafts-Tag für jede Eigenschaft, die derzeit von einem Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7871a-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="7871a-122">Wenn das Objekt keine Eigenschaften derzeit nicht unterstützt, gibt **GetPropList** ein Array Tag-Eigenschaft mit dem **cValues** -Element auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7871a-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="7871a-123">Der Umfang der Eigenschaften von **GetPropList** zurückgegebene variiert von Anbieter zu Anbieter.</span><span class="sxs-lookup"><span data-stu-id="7871a-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="7871a-124">Einige Dienstanbieter ausschließen diese Eigenschaften für die der Anrufer nicht zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="7871a-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="7871a-125">Alle Anbieter geben Eigenschaften vom Typ **PT_OBJECT**zurück.</span><span class="sxs-lookup"><span data-stu-id="7871a-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="7871a-126">Wenn das Objekt Unicode nicht unterstützt, gibt **GetPropList** MAPI_E_BAD_CHARWIDTH, auch wenn es keine Zeichenfolgeneigenschaften für das Objekt definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7871a-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7871a-127">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="7871a-127">Notes to implementers</span></span>

<span data-ttu-id="7871a-128">Remote-Transport-Anbieter implementieren **GetPropList** hier genau wie angegeben.</span><span class="sxs-lookup"><span data-stu-id="7871a-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="7871a-129">Es sind keine besonderen Bedenken.</span><span class="sxs-lookup"><span data-stu-id="7871a-129">There are no special concerns.</span></span> <span data-ttu-id="7871a-130">Die Implementierung sollte, natürlich, Eigenschaften, die von der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode unterstützt die gleiche Liste zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7871a-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7871a-131">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7871a-131">Notes to callers</span></span>

<span data-ttu-id="7871a-132">Rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um die Array-Tag-Eigenschaft auf den _LppPropTagArray_frei.</span><span class="sxs-lookup"><span data-stu-id="7871a-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7871a-133">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="7871a-133">MFCMAPI reference</span></span>

<span data-ttu-id="7871a-134">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7871a-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7871a-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="7871a-135">**File**</span></span>|<span data-ttu-id="7871a-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="7871a-136">**Function**</span></span>|<span data-ttu-id="7871a-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7871a-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7871a-138">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="7871a-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="7871a-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="7871a-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="7871a-140">MFCMAPI (engl.) verwendet die **IMAPIProp::GetPropList** -Methode, um eine Eigenschaftenliste zum Übergeben an **GetProps**abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7871a-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7871a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7871a-141">See also</span></span>



[<span data-ttu-id="7871a-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="7871a-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="7871a-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7871a-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7871a-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7871a-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="7871a-145">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="7871a-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

