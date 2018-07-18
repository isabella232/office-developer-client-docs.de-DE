---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7008549111f1b914cf2025c8d61ebc07196706fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792858"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="2b5c5-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="2b5c5-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="2b5c5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2b5c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2b5c5-105">Verarbeitet aus einer Nachricht an eine einzelne Komponenten zu einem Zeitpunkt in einem Stream Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="2b5c5-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="2b5c5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b5c5-106">Parameters</span></span>

 <span data-ttu-id="2b5c5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2b5c5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2b5c5-108">[in] Eine Bitmaske aus Flags, die steuert, welche Komponente abgeschlossen sein wird.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="2b5c5-109">Mindestens eine der anderen der folgenden Werte muss festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="2b5c5-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="2b5c5-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="2b5c5-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="2b5c5-111">Für ein Attachment-Objekt wird die Verarbeitung abgeschlossen werden; der Parameter _UlComponentID_ enthält die **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="2b5c5-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="2b5c5-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="2b5c5-113">Wird die Verarbeitung für ein Meldungsobjekt abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="2b5c5-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="2b5c5-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="2b5c5-115">[in] 0 bis zur Verarbeitung für eine Nachricht oder die **PR_ATTACH_NUM** -Eigenschaft einer Anlage zu verarbeitenden anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="2b5c5-116">Wenn das Flag TNEF_COMPONENT_MESSAGE im _UlFlags_ -Parameter festgelegt ist, muss _UlComponentID_ 0 sein.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="2b5c5-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="2b5c5-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="2b5c5-118">[in] Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die Eigenschaftentags enthält, mit denen die Eigenschaften im _LpCustomProps_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="2b5c5-119">Es muss eine 1: 1-Beziehung zwischen den einzelnen Eigenschaftswert in _LpCustomProps_ und ein Tag-Eigenschaft im _LpCustomPropList_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="2b5c5-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="2b5c5-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="2b5c5-121">[in] Ein Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die Eigenschaftswerte für die Eigenschaften, die zu codierende enthält.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="2b5c5-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="2b5c5-122">_lpPropList_</span></span>
  
> <span data-ttu-id="2b5c5-123">[in] Ein Zeiger auf eine **SPropTagArray** -Struktur, die für die Eigenschaften, die zu codierende Eigenschaftentags enthält.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="2b5c5-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="2b5c5-124">_lppProblems_</span></span>
  
> <span data-ttu-id="2b5c5-125">[out] Ein Zeiger auf einen Zeiger auf eine zurückgegebenen [STnefProblemArray](stnefproblemarray.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="2b5c5-126">Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="2b5c5-127">Wenn NULL in der _LppProblems_ -Parameter übergeben wird, wird kein Problem Array-Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2b5c5-128">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="2b5c5-128">Return value</span></span>

<span data-ttu-id="2b5c5-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b5c5-129">S_OK</span></span> 
  
> <span data-ttu-id="2b5c5-130">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2b5c5-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b5c5-131">Remarks</span></span>

<span data-ttu-id="2b5c5-132">Transport-Anbieter, Nachricht-Anbieter und Gateways Aufruf der **ITnef::FinishComponent** -Methode von TNEF für eine Komponente, die eine Nachricht oder eine Anlage Verarbeitung ausführen, wie das Flag festlegen in der _UlFlags_ -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="2b5c5-133">Für die Verarbeitung der Komponente aktiviert werden soll, übergeben die aufrufende Anbieter oder Gateway Sie die Kennzeichen TNEF_COMPONENT_ENCODING _UlFlags_ für die [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion, die das Objekt, um die Codierung wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="2b5c5-134">Übergeben von Werten in den _LpCustomPropList_ und _LpCustomProps_ führt Komponente Codierung entspricht, die die [ITnef::SetProps](itnef-setprops.md) -Methode ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="2b5c5-135">Ein Wert in der _LpPropList_ -Parameter übergeben, führt Komponente Codierung entspricht, die von der [ITnef::AddProps](itnef-addprops.md) -Methode mit dem TNEF_PROP_INCLUDE-Flag festlegen in _UlFlags_erfolgen.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="2b5c5-136">Übergeben diese Werte können Sie mit einem einzigen Aufruf anstatt mehrere Aufrufe Codierungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="2b5c5-137">Die TNEF-Implementierung Berichte TNEF-Stream Probleme ohne Anhalten des Prozesses **FinishComponent** -Codierung.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="2b5c5-138">Die **STnefProblemArray** -Struktur, die in _LppProblems_ zurückgegeben gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="2b5c5-139">Der im **Scode** -Member, eine der in **STnefProblemArray** enthaltenen **STnefProblem** Strukturen zurückgegebene Wert gibt an, das Problem.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="2b5c5-140">Der Anbieter oder Gateway kann auf der Annahme arbeiten, dass alle Eigenschaften oder Attribute, die für die **FinishComponent** kein Problemberichts zurückgibt erfolgreich verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="2b5c5-141">Wenn Sie einen Anbieter oder ein Gateway mit Problem Arrays nicht funktionsfähig ist, können sie NULL _LppProblems_übergeben; In diesem Fall wird kein Problem Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="2b5c5-142">Der in _LppProblems_ zurückgegebene Wert ist nur gültig, wenn der Aufruf gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="2b5c5-143">Wenn S_OK zurückgegeben wird, sollte der Anbieter oder ein Gateway in der Struktur [STnefProblemArray](stnefproblemarray.md) zurückgegebenen Werte überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="2b5c5-144">Bei einem beim Aufruf Fehler die **STnefProblemArray** -Struktur ist nicht ausgefüllt, und die aufrufende Anbieter oder das Gateway nicht verwenden oder die Struktur frei.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="2b5c5-145">Wenn dem Gespräch tritt kein Fehler auf, muss die aufrufende Anbieter oder Gateway den Speicher freizugeben für die **STnefProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2b5c5-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b5c5-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b5c5-146">See also</span></span>



[<span data-ttu-id="2b5c5-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="2b5c5-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="2b5c5-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="2b5c5-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="2b5c5-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2b5c5-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2b5c5-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="2b5c5-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="2b5c5-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="2b5c5-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="2b5c5-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="2b5c5-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="2b5c5-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="2b5c5-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="2b5c5-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2b5c5-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

