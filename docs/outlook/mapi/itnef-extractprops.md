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
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348650"
---
# <a name="itnefextractprops"></a><span data-ttu-id="4018f-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="4018f-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="4018f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4018f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4018f-105">Extrahiert die Eigenschaften aus einer TNEF-Kapselung.</span><span class="sxs-lookup"><span data-stu-id="4018f-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="4018f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4018f-106">Parameters</span></span>

 <span data-ttu-id="4018f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4018f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4018f-108">in Eine Bitmaske von Flags, die Steuern, wie Eigenschaften decodiert werden.</span><span class="sxs-lookup"><span data-stu-id="4018f-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="4018f-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4018f-109">The following flags can be set:</span></span>
    
<span data-ttu-id="4018f-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="4018f-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="4018f-111">Decodiert alle Eigenschaften, die nicht im _lpPropList_ -Parameter angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="4018f-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="4018f-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="4018f-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="4018f-113">Decodiert alle in _lpPropList_angegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4018f-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="4018f-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="4018f-114">_lpPropList_</span></span>
  
> <span data-ttu-id="4018f-115">in Ein Zeiger auf die Liste der Eigenschaften, die in den Decodierungsvorgang eingeschlossen oder daraus ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4018f-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="4018f-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="4018f-116">_lpProblems_</span></span>
  
> <span data-ttu-id="4018f-117">Out Ein Zeiger auf einen Zeiger auf eine zurückgegebene [STnefProblemArray](stnefproblemarray.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4018f-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="4018f-118">Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="4018f-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="4018f-119">Wenn NULL im _lpProblems_ -Parameter übergeben wird, wird kein Property-Problem-Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4018f-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4018f-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4018f-120">Return value</span></span>

<span data-ttu-id="4018f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="4018f-121">S_OK</span></span> 
  
> <span data-ttu-id="4018f-122">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4018f-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="4018f-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="4018f-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="4018f-124">Daten, die in einem Stream decodiert werden, sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="4018f-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4018f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4018f-125">Remarks</span></span>

<span data-ttu-id="4018f-126">Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef:: ExtractProps** -Methode auf, um Eigenschaften aus der Kapselung einer Nachricht oder einer Anlage, die an die [OpenTnefStream](opentnefstream.md) -Funktion übergeben wurde, zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="4018f-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="4018f-127">Der aufrufende Anbieter oder das Gateway kann eine Liste der zu decodierenden Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="4018f-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="4018f-128">Anbieter und Gateways können auch **ExtractProps** verwenden, um Informationen zur Sonderbehandlung für Anlagen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4018f-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="4018f-129">**ExtractProps** füllt die ursprüngliche Nachricht, die an **OpenTnefStream** übergeben wurde, mit den decodierten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4018f-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="4018f-130">Nachfolgende **ExtractProps** -Aufrufe gehen zurück auf die Nachricht und extrahieren die neue Liste mit Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4018f-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="4018f-131">Im Gegensatz zur [ITnef::](itnef-addprops.md) AddProps-Methode, die die angeforderten Aktionen in die Warteschlange stellt, bis die **ITnef:: Finish** -Methode aufgerufen wird, dekodiert die **ExtractProps** -Methode die gekapselt Eigenschaften sofort, wenn Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4018f-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="4018f-132">Aus diesem Grund sollte die Zielnachricht für die Kapselungs Decodierung relativ leer sein.</span><span class="sxs-lookup"><span data-stu-id="4018f-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="4018f-133">Vorhandene Eigenschaften in der Zielnachricht werden durch gekapselte Eigenschaften überschrieben.</span><span class="sxs-lookup"><span data-stu-id="4018f-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="4018f-134">**ExtractProps** wird nur für Objekte unterstützt, die mit dem TNEF_DECODE-Flag für die **OpenTnefStream** -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="4018f-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="4018f-135">Die TNEF-Implementierung meldet TNEF-Datenstrom Codierungsprobleme, ohne den **ExtractProps** -Prozess zu beenden.</span><span class="sxs-lookup"><span data-stu-id="4018f-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="4018f-136">Die in _lpProblems_ zurückgeGebene [STnefProblemArray](stnefproblemarray.md) -Struktur gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnten.</span><span class="sxs-lookup"><span data-stu-id="4018f-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="4018f-137">Der Wert, der im **SCODE** -Element einer der in **STnefProblemArray** enthaltenen **STnefProblem** -Strukturen zurückgegeben wird, gibt das spezifische Problem an.</span><span class="sxs-lookup"><span data-stu-id="4018f-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="4018f-138">Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **ExtractProps** keinen Problembericht zurückgibt, erfolgreich verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="4018f-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4018f-139">Wenn eine Eigenschaft im MAPI-Kapselungs Block nicht verarbeitet werden kann und der Datenstrom während der Decodierung eines TNEF-Streams unzuverlässig bleibt, wird die Decodierung des Kapselungs Blocks beendet und ein Problem gemeldet.</span><span class="sxs-lookup"><span data-stu-id="4018f-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="4018f-140">Das Problem Array für diesen Problemtyp enthält 0L für das **ulPropTag** `attMAPIProps` -Element `attAttachment` oder für das **ulAttribute** -Element und MAPI_E_UNABLE_TO_COMPLETE für das **SCODE** -Element.</span><span class="sxs-lookup"><span data-stu-id="4018f-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="4018f-141">Beachten Sie, dass die Decodierung des Streams nicht angehalten wird, sondern nur die Decodierung des MAPI-Kapselungs Blocks.</span><span class="sxs-lookup"><span data-stu-id="4018f-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="4018f-142">Die Datenstrom Decodierung wird mit dem nächsten Attributblock fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4018f-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="4018f-143">Wenn ein Anbieter oder Gateway nicht mit Problem Arrays funktioniert, kann er in _lppProblems_den Wert NULL überschreiten; in diesem Fall wird kein Problem Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4018f-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="4018f-144">Der in _lpProblems_ zurückgegebene Wert ist nur gültig, wenn der Aufruf S_OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4018f-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="4018f-145">Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die in der **STnefProblemArray** -Struktur zurückgegebenen Werte überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4018f-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="4018f-146">Wenn für den Anruf ein Fehler auftritt, wird die **STnefProblemArray** -Struktur nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder freigeben.</span><span class="sxs-lookup"><span data-stu-id="4018f-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="4018f-147">Wenn beim Aufruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Speicher für die **STnefProblemArray** -Struktur freigeben, indem er die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="4018f-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4018f-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4018f-148">See also</span></span>



[<span data-ttu-id="4018f-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="4018f-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="4018f-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="4018f-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="4018f-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="4018f-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="4018f-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4018f-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4018f-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="4018f-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="4018f-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="4018f-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="4018f-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="4018f-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="4018f-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4018f-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

