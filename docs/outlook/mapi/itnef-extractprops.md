---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 26949f10e22c4d2ea49594ee3365ae7d3bb3662d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792870"
---
# <a name="itnefextractprops"></a><span data-ttu-id="ae1d6-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="ae1d6-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="ae1d6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ae1d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ae1d6-105">Extrahiert die Eigenschaften von TNEF-Kapselung.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="ae1d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae1d6-106">Parameters</span></span>

 <span data-ttu-id="ae1d6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ae1d6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ae1d6-108">[in] Eine Bitmaske aus Flags, die steuert, wie Eigenschaften decodiert werden.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="ae1d6-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ae1d6-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ae1d6-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="ae1d6-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="ae1d6-111">Decodiert alle Eigenschaften in der _LpPropList_ -Parameter nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="ae1d6-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="ae1d6-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="ae1d6-113">Decodiert alle Eigenschaften in _LpPropList_angegeben.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="ae1d6-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="ae1d6-114">_lpPropList_</span></span>
  
> <span data-ttu-id="ae1d6-115">[in] Ein Zeiger auf die Liste der Eigenschaften ein-oder Ausschließen von der Decodierung Operation.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="ae1d6-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="ae1d6-116">_lpProblems_</span></span>
  
> <span data-ttu-id="ae1d6-117">[out] Ein Zeiger auf einen Zeiger auf eine zurückgegebenen [STnefProblemArray](stnefproblemarray.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="ae1d6-118">Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="ae1d6-119">Wenn NULL in der _LpProblems_ -Parameter übergeben wird, wird kein Problem Array-Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ae1d6-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae1d6-120">Return value</span></span>

<span data-ttu-id="ae1d6-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae1d6-121">S_OK</span></span> 
  
> <span data-ttu-id="ae1d6-122">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="ae1d6-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="ae1d6-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="ae1d6-124">In einem Stream decodierte Daten ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae1d6-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae1d6-125">Remarks</span></span>

<span data-ttu-id="ae1d6-126">Transport-Provider, Anbieter Nachricht und Gateways rufen die **ITnef::ExtractProps** -Methode zum Extrahieren von (das Decodieren ist,) Eigenschaften aus der Kapselung einer Nachricht oder einer Anlage, die an die Funktion [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="ae1d6-127">Die aufrufende Anbieter oder Gateway kann eine Liste der Eigenschaften zum Decodieren angeben.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="ae1d6-128">Anbieter und Gateways können **ExtractProps** auch Informationen zur keine besondere Behandlung für Anlagen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="ae1d6-129">**ExtractProps** füllt die ursprüngliche Nachricht in **OpenTNEFStream nicht ausgeführt werden** mit den Eigenschaften decodierten übergeben.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="ae1d6-130">Nachfolgende **ExtractProps** Aufrufe zurück an die Nachricht, und extrahieren Sie die neue Liste der Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="ae1d6-131">Im Gegensatz zu der [ITnef::AddProps](itnef-addprops.md) -Methode, die Warteschlangen Aktionen angefordert, bis die **ITnef::Finish** -Methode aufgerufen wird, decodiert die **ExtractProps** -Methode die gekapselten Eigenschaften sofort, wenn sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="ae1d6-132">Aus diesem Grund sollten die Zielnachricht für die Decodierung Encapsulation relativ leer sein.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="ae1d6-133">Vorhandene Eigenschaften in der Zielnachricht werden von gekapselte Eigenschaften überschrieben.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="ae1d6-134">**ExtractProps** wird nur für Objekte unterstützt, die mit dem TNEF_DECODE-Flag für die Funktion **OpenTNEFStream nicht ausgeführt werden** oder [OpenTnefStreamEx](opentnefstreamex.md) geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="ae1d6-135">Die TNEF-Implementierung Berichte TNEF-Stream Probleme ohne Anhalten des Prozesses **ExtractProps** -Codierung.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="ae1d6-136">Die [STnefProblemArray](stnefproblemarray.md) -Struktur, die in _LpProblems_ zurückgegeben gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="ae1d6-137">Der im **Scode** -Member, eine der in **STnefProblemArray** enthaltenen **STnefProblem** Strukturen zurückgegebene Wert gibt an, das Problem.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="ae1d6-138">Der Anbieter oder Gateway kann auf der Annahme arbeiten, dass alle Eigenschaften oder Attribute, die für die **ExtractProps** kein Problemberichts zurückgibt erfolgreich verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ae1d6-139">Wenn eine Eigenschaft im MAPI-Kapselung Block kann nicht verarbeitet werden und den Stream während der Decodierung eines Streams TNEF unzuverlässig lässt, Decodieren des Blocks Encapsulation wurde beendet und ein Problem gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="ae1d6-140">Das Problem Array für diese Art von Problem enthält 0L für den **UlPropTag** -Member, `attMAPIProps` oder `attAttachment` für **UlAttribute** Member und MAPI_E_UNABLE_TO_COMPLETE für den **Scode** -Member.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="ae1d6-141">Beachten Sie, dass die Decodierung des Datenstroms nicht angehalten, nur die Decodierung des MAPI-Kapselung Blocks.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="ae1d6-142">Der Datenstrom Decodierung wird mit dem nächsten Attributblock fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="ae1d6-143">Wenn Sie einen Anbieter oder ein Gateway mit Problem Arrays nicht funktionsfähig ist, können sie NULL _LppProblems_übergeben; In diesem Fall wird kein Problem Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="ae1d6-144">Der in _LpProblems_ zurückgegebene Wert ist nur gültig, wenn der Aufruf gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="ae1d6-145">Wenn S_OK zurückgegeben wird, sollte der Anbieter oder ein Gateway in der Struktur **STnefProblemArray** zurückgegebenen Werte überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="ae1d6-146">Bei einem beim Aufruf Fehler die **STnefProblemArray** -Struktur ist nicht ausgefüllt und die aufrufende Anbieter oder das Gateway nicht verwenden oder die Struktur frei.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="ae1d6-147">Wenn dem Gespräch tritt kein Fehler auf, muss die aufrufende Anbieter oder Gateway des Speichers für die Struktur **STnefProblemArray** durch Aufrufen der Funktion [MAPIFreeBuffer](mapifreebuffer.md) freigeben.</span><span class="sxs-lookup"><span data-stu-id="ae1d6-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae1d6-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae1d6-148">See also</span></span>



[<span data-ttu-id="ae1d6-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="ae1d6-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="ae1d6-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="ae1d6-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="ae1d6-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="ae1d6-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="ae1d6-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ae1d6-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ae1d6-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="ae1d6-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="ae1d6-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="ae1d6-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="ae1d6-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="ae1d6-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="ae1d6-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae1d6-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

