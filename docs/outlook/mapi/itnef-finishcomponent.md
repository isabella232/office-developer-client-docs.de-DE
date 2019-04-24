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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278886"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="f6557-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="f6557-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="f6557-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6557-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6557-105">Verarbeitet einzelne Komponenten aus einer Nachricht nacheinander in einen TNEF-Stream (Transport Neutral Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="f6557-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="f6557-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6557-106">Parameters</span></span>

 <span data-ttu-id="f6557-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f6557-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f6557-108">in Eine Bitmaske von Flags, die steuert, welche Komponente beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6557-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="f6557-109">Eine der folgenden Flags muss festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f6557-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="f6557-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="f6557-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="f6557-111">Die Verarbeitung wird für ein Attachment-Objekt beendet; der Parameter _ulComponentID_ enthält die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage.</span><span class="sxs-lookup"><span data-stu-id="f6557-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="f6557-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="f6557-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="f6557-113">Die Verarbeitung wird für ein Message-Objekt abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f6557-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="f6557-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="f6557-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="f6557-115">[in] 0, um die Verarbeitung für eine Nachricht anzugeben, oder die **PR_ATTACH_NUM** -Eigenschaft einer Anlage, die verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6557-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="f6557-116">Wenn das TNEF_COMPONENT_MESSAGE-Flag im _ulFlags_ -Parameter festgelegt ist, muss _ulComponentID_ 0 sein.</span><span class="sxs-lookup"><span data-stu-id="f6557-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="f6557-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="f6557-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="f6557-118">in Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die Eigenschaftstags enthält, die die im _lpCustomProps_ -Parameter übergebenen Eigenschaften identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f6557-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="f6557-119">Es muss eine 1:1-Entsprechung zwischen jedem Eigenschaftswert in _lpCustomProps_ und einem Property-Tag im _LpCustomPropList_ -Parameter vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f6557-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="f6557-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="f6557-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="f6557-121">in Ein Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die Eigenschaftswerte für die zu codierenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="f6557-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="f6557-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="f6557-122">_lpPropList_</span></span>
  
> <span data-ttu-id="f6557-123">in Ein Zeiger auf eine **SPropTagArray** -Struktur, die Eigenschaftentags für die zu codierenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="f6557-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="f6557-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="f6557-124">_lppProblems_</span></span>
  
> <span data-ttu-id="f6557-125">Out Ein Zeiger auf einen Zeiger auf eine zurückgegebene [STnefProblemArray](stnefproblemarray.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f6557-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="f6557-126">Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f6557-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="f6557-127">Wenn NULL im _lppProblems_ -Parameter übergeben wird, wird kein Property-Problem-Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f6557-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f6557-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6557-128">Return value</span></span>

<span data-ttu-id="f6557-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6557-129">S_OK</span></span> 
  
> <span data-ttu-id="f6557-130">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f6557-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6557-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6557-131">Remarks</span></span>

<span data-ttu-id="f6557-132">Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef:: FinishComponent** -Methode auf, um die TNEF-Verarbeitung für eine Komponente, entweder eine Nachricht oder eine Anlage auszuführen, wie durch das im _ulFlags_ -Parameter festgelegte Flag angegeben.</span><span class="sxs-lookup"><span data-stu-id="f6557-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="f6557-133">Zur Aktivierung der Komponentenverarbeitung übergibt der aufrufende Anbieter oder das Gateway das TNEF_COMPONENT_ENCODING-Flag in _ulFlags_ für die [OpenTnefStream](opentnefstream.md) -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion, die das Objekt zum Empfangen der Codierung geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="f6557-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="f6557-134">Das übergeben von Werten in den Parametern _lpCustomPropList_ und _lpCustomProps_ führt eine Komponenten Codierung aus, die der [ITnef::](itnef-setprops.md) SetProps-Methode entspricht.</span><span class="sxs-lookup"><span data-stu-id="f6557-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="f6557-135">Durch das Übergeben eines Werts im _lpPropList_ -Parameter wird die Komponenten Codierung ausgeführt, die der [ITnef::](itnef-addprops.md) AddProps-Methode mit dem in _ULFLAGS_festgelegten TNEF_PROP_INCLUDE-Flag entspricht.</span><span class="sxs-lookup"><span data-stu-id="f6557-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="f6557-136">Durch das Übergeben dieser Werte können Sie Codierungen mit einem einzelnen Aufruf anstelle mehrerer Aufrufe durchführen.</span><span class="sxs-lookup"><span data-stu-id="f6557-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="f6557-137">Die TNEF-Implementierung meldet TNEF-Datenstrom Codierungsprobleme, ohne den **FinishComponent** -Prozess zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f6557-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="f6557-138">Die in _lppProblems_ zurückgeGebene **STnefProblemArray** -Struktur gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnten.</span><span class="sxs-lookup"><span data-stu-id="f6557-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="f6557-139">Der Wert, der im **SCODE** -Element einer der in **STnefProblemArray** enthaltenen **STnefProblem** -Strukturen zurückgegeben wird, gibt das spezifische Problem an.</span><span class="sxs-lookup"><span data-stu-id="f6557-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="f6557-140">Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **FinishComponent** keinen Problembericht zurückgibt, erfolgreich verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="f6557-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="f6557-141">Wenn ein Anbieter oder Gateway nicht mit Problem Arrays funktioniert, kann er in _lppProblems_den Wert NULL überschreiten; in diesem Fall wird kein Problem Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f6557-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="f6557-142">Der in _lppProblems_ zurückgegebene Wert ist nur gültig, wenn der Aufruf S_OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f6557-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="f6557-143">Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die in der [STnefProblemArray](stnefproblemarray.md) -Struktur zurückgegebenen Werte überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f6557-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="f6557-144">Wenn für den Anruf ein Fehler auftritt, wird die **STnefProblemArray** -Struktur nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder freigeben.</span><span class="sxs-lookup"><span data-stu-id="f6557-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="f6557-145">Wenn beim Aufruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Speicher für das **STnefProblemArray** freigeben, indem er die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="f6557-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6557-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6557-146">See also</span></span>



[<span data-ttu-id="f6557-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="f6557-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="f6557-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="f6557-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="f6557-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f6557-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f6557-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="f6557-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="f6557-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="f6557-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="f6557-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="f6557-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="f6557-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="f6557-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="f6557-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6557-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

