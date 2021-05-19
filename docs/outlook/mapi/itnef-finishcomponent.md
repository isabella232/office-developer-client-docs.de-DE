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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416440"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="2c1a7-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="2c1a7-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="2c1a7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c1a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c1a7-105">Verarbeitet einzelne Komponenten aus einer Nachricht einzeln in einen Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="2c1a7-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2c1a7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c1a7-106">Parameters</span></span>

 <span data-ttu-id="2c1a7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2c1a7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2c1a7-108">[in] Eine Bitmaske mit Flags, die steuert, welche Komponente fertig gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="2c1a7-109">Das eine oder andere der folgenden Kennzeichen muss festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="2c1a7-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="2c1a7-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="2c1a7-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="2c1a7-111">Die Verarbeitung für ein Anlagenobjekt wird abgeschlossen. Der  _ulComponentID-Parameter_ enthält **die PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) -Eigenschaft der Anlage.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="2c1a7-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="2c1a7-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="2c1a7-113">Die Verarbeitung wird für ein Nachrichtenobjekt abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="2c1a7-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="2c1a7-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="2c1a7-115">[in] 0, um die Verarbeitung einer Nachricht oder die PR_ATTACH_NUM **einer** zu verarbeitenden Anlage anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="2c1a7-116">Wenn das TNEF_COMPONENT_MESSAGE im  _ulFlags-Parameter_ festgelegt ist,  _muss ulComponentID_ 0 sein.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="2c1a7-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="2c1a7-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="2c1a7-118">[in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die Eigenschaftstags enthält, die die im  _lpCustomProps-Parameter_ übergebenen Eigenschaften identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="2c1a7-119">Es muss eine 1:1-Entsprechung zwischen jedem Eigenschaftswert in  _lpCustomProps_ und einem Eigenschaftstag im  _lpCustomPropList-Parameter_ liegen.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="2c1a7-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="2c1a7-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="2c1a7-121">[in] Ein Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die Eigenschaftswerte für die zu codierenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="2c1a7-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="2c1a7-122">_lpPropList_</span></span>
  
> <span data-ttu-id="2c1a7-123">[in] Ein Zeiger auf eine **SPropTagArray-Struktur,** die Eigenschaftstags für die zu codenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="2c1a7-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="2c1a7-124">_lppProblems_</span></span>
  
> <span data-ttu-id="2c1a7-125">[out] Ein Zeiger auf einen Zeiger auf eine zurückgegebene [STnefProblemArray-Struktur.](stnefproblemarray.md)</span><span class="sxs-lookup"><span data-stu-id="2c1a7-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="2c1a7-126">Die **STnefProblemArray-Struktur** gibt an, welche Eigenschaften, falls welche, nicht ordnungsgemäß codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="2c1a7-127">Wenn NULL im  _lppProblems-Parameter_ übergeben wird, wird kein Array mit Eigenschaftsproblemen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2c1a7-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c1a7-128">Return value</span></span>

<span data-ttu-id="2c1a7-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="2c1a7-129">S_OK</span></span> 
  
> <span data-ttu-id="2c1a7-130">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2c1a7-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c1a7-131">Remarks</span></span>

<span data-ttu-id="2c1a7-132">Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::FinishComponent-Methode** auf, um die TNEF-Verarbeitung für eine Komponente, entweder eine Nachricht oder eine Anlage, durchzuführen, wie durch das im  _ulFlags-Parameter_ festgelegte Flag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="2c1a7-133">Damit die Komponentenverarbeitung aktiviert werden kann, übergeben der aufrufende Anbieter oder das Gateway das TNEF_COMPONENT_ENCODING-Flag in  _ulFlags_ für die [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion,](opentnefstreamex.md) die das Objekt geöffnet hat, um die Codierung zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="2c1a7-134">Bei der Übergabe von Werten in den  _Parametern lpCustomPropList_ und  _lpCustomProps_ wird eine Komponentencodierung durchgeführt, die der von der [ITnef::SetProps-Methode](itnef-setprops.md) durchgeführten Codierung entspricht.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="2c1a7-135">Das Übergeben eines Werts im  _lpPropList-Parameter_ führt eine Komponentencodierung durch, die der von der [ITnef::AddProps-Methode](itnef-addprops.md) mit dem in  _ulFlags_ festgelegten TNEF_PROP_INCLUDE entspricht.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="2c1a7-136">Wenn Sie diese Werte übergeben, können Sie Codierungen mit einem einzelnen Aufruf statt mit mehreren Aufrufen ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="2c1a7-137">Die TNEF-Implementierung meldet TNEF-Streamcodierungsprobleme, ohne den **FinishComponent-Prozess zu** beenden.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="2c1a7-138">Die in _lppProblems_ zurückgegebene **STnefProblemArray-Struktur** gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften (falls welche) nicht verarbeitet werden konnten.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="2c1a7-139">Der im **scode-Element** der in **STnefProblemArray enthaltene STnefProblemProblem-Struktur** zurückgegebene Wert gibt das spezifische Problem an. </span><span class="sxs-lookup"><span data-stu-id="2c1a7-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="2c1a7-140">Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **FinishComponent** keinen Problembericht zurück gibt, erfolgreich verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="2c1a7-141">Wenn ein Anbieter oder Gateway nicht mit Problemarrays funktioniert, kann er NULL in  _lppProblems übergeben._ In diesem Fall wird kein Problemarray zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="2c1a7-142">Der in  _lppProblems_ zurückgegebene Wert ist nur gültig, wenn der Aufruf eine S_OK.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="2c1a7-143">Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die in der [STnefProblemArray-Struktur](stnefproblemarray.md) zurückgegebenen Werte überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="2c1a7-144">Wenn beim Anruf ein Fehler auftritt, wird die **STnefProblemArray-Struktur** nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder frei geben.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="2c1a7-145">Wenn beim Anruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Arbeitsspeicher für **das STnefProblemArray** durch Aufrufen der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) frei geben.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c1a7-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c1a7-146">See also</span></span>



[<span data-ttu-id="2c1a7-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="2c1a7-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="2c1a7-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="2c1a7-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="2c1a7-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2c1a7-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2c1a7-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="2c1a7-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="2c1a7-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="2c1a7-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="2c1a7-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="2c1a7-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="2c1a7-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="2c1a7-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="2c1a7-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2c1a7-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

