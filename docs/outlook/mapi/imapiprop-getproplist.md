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
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414788"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="ac02e-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="ac02e-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="ac02e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac02e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac02e-105">Gibt Eigenschaftstags für alle Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="ac02e-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="ac02e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac02e-106">Parameters</span></span>

 <span data-ttu-id="ac02e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac02e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ac02e-108">[in] Eine Bitmaske mit Flags, die das Format für die Zeichenfolgen in den zurückgegebenen Eigenschaftstags steuert.</span><span class="sxs-lookup"><span data-stu-id="ac02e-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="ac02e-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ac02e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="ac02e-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ac02e-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ac02e-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="ac02e-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="ac02e-112">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="ac02e-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ac02e-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="ac02e-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="ac02e-114">[out] Ein Zeiger auf einen Zeiger auf das Eigenschaftentagarray, das Tags für alle Eigenschaften des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="ac02e-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac02e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac02e-115">Return value</span></span>

<span data-ttu-id="ac02e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac02e-116">S_OK</span></span> 
  
> <span data-ttu-id="ac02e-117">Alle Eigenschaftstags wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ac02e-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="ac02e-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ac02e-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ac02e-119">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="ac02e-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac02e-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ac02e-120">Remarks</span></span>

<span data-ttu-id="ac02e-121">Die **IMAPIProp::GetPropList-Methode** ruft das Eigenschaftstag für jede Eigenschaft ab, die derzeit von einem Objekt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ac02e-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="ac02e-122">Wenn das Objekt derzeit keine Eigenschaften unterstützt, gibt **GetPropList** ein Eigenschaftstagarray zurück, bei dem **das Element cValues** auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ac02e-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="ac02e-123">Der Umfang der von **GetPropList** zurückgegebenen Eigenschaften variiert von Anbieter zu Anbieter.</span><span class="sxs-lookup"><span data-stu-id="ac02e-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="ac02e-124">Einige Dienstanbieter schließen die Eigenschaften aus, auf die der Anrufer keinen Zugriff hat.</span><span class="sxs-lookup"><span data-stu-id="ac02e-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="ac02e-125">Alle Anbieter geben Eigenschaften vom Typ **PT_OBJECT**.</span><span class="sxs-lookup"><span data-stu-id="ac02e-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="ac02e-126">Wenn das Objekt Unicode nicht unterstützt, gibt **GetPropList** MAPI_E_BAD_CHARWIDTH zurück, auch wenn keine Zeichenfolgeneigenschaften für das Objekt definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ac02e-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ac02e-127">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="ac02e-127">Notes to implementers</span></span>

<span data-ttu-id="ac02e-128">Remote-Transport-Anbieter implementieren **GetPropList** genau wie hier angegeben.</span><span class="sxs-lookup"><span data-stu-id="ac02e-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="ac02e-129">Es gibt keine besonderen Bedenken.</span><span class="sxs-lookup"><span data-stu-id="ac02e-129">There are no special concerns.</span></span> <span data-ttu-id="ac02e-130">Ihre Implementierung sollte natürlich dieselbe Liste von Eigenschaften zurückgeben, die von der [IMAPIProp::GetProps-Methode unterstützt](imapiprop-getprops.md) wird.</span><span class="sxs-lookup"><span data-stu-id="ac02e-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac02e-131">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ac02e-131">Notes to callers</span></span>

<span data-ttu-id="ac02e-132">Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um das Eigenschaftentagarray frei zu machen, auf das _von lppPropTagArray verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="ac02e-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ac02e-133">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="ac02e-133">MFCMAPI reference</span></span>

<span data-ttu-id="ac02e-134">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ac02e-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ac02e-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ac02e-135">**File**</span></span>|<span data-ttu-id="ac02e-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ac02e-136">**Function**</span></span>|<span data-ttu-id="ac02e-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ac02e-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac02e-138">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ac02e-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ac02e-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="ac02e-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="ac02e-140">MFCMAPI verwendet die **IMAPIProp::GetPropList-Methode,** um eine Eigenschaftsliste zu erhalten, die an **GetProps übergeben werden soll.**</span><span class="sxs-lookup"><span data-stu-id="ac02e-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac02e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac02e-141">See also</span></span>



[<span data-ttu-id="ac02e-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="ac02e-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="ac02e-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ac02e-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ac02e-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac02e-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="ac02e-145">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ac02e-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

