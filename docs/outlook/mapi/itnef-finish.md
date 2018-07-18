---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2b95e0dd62d83dd83a064ee4627811fcb24af921
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792867"
---
# <a name="itneffinish"></a><span data-ttu-id="3ae27-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="3ae27-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="3ae27-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ae27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ae27-105">Beendet Verarbeitung für alle Transport-Neutral Encapsulation Format (TNEF) Vorgänge, die sich in der Warteschlange und wartet.</span><span class="sxs-lookup"><span data-stu-id="3ae27-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="3ae27-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ae27-106">Parameters</span></span>

 <span data-ttu-id="3ae27-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ae27-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3ae27-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="3ae27-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3ae27-109">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="3ae27-109">_lpKey_</span></span>
  
> <span data-ttu-id="3ae27-110">[out] Ein Zeiger auf die wichtigste **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage.</span><span class="sxs-lookup"><span data-stu-id="3ae27-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="3ae27-111">Das TNEF-Kapselung-Objekt verwendet diesen Schlüssel mit dem entsprechenden Anlage Platzierung Tag in einer Nachricht eine Anlage übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="3ae27-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="3ae27-112">Dieser Schlüssel sollte für jede Anlage eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="3ae27-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="3ae27-113">_lpProblem_</span><span class="sxs-lookup"><span data-stu-id="3ae27-113">_lpProblem_</span></span>
  
> <span data-ttu-id="3ae27-114">[out] Ein Zeiger auf einen Zeiger auf eine zurückgegebenen [STnefProblemArray](stnefproblemarray.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3ae27-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="3ae27-115">Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3ae27-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="3ae27-116">Wenn NULL in der _LpProblem_ -Parameter übergeben wird, wird kein Problem Array-Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3ae27-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3ae27-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3ae27-117">Return value</span></span>

<span data-ttu-id="3ae27-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ae27-118">S_OK</span></span> 
  
> <span data-ttu-id="3ae27-119">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3ae27-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ae27-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ae27-120">Remarks</span></span>

<span data-ttu-id="3ae27-121">Transport-Provider, Anbieter Nachricht und Gateways Aufruf die **ITnef::Finish** -Methode zum Ausführen der Codierung aller Eigenschaften für die Codierung Aufrufe der Methoden [ITnef::AddProps](itnef-addprops.md) und [ITnef::SetProps](itnef-setprops.md) angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="3ae27-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="3ae27-122">Wenn das TNEF-Objekt mit dem TNEF_ENCODE-Flag für die [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion geöffnet wurde, codiert die Methode **Fertig stellen** die angeforderten Eigenschaften in der an dieses Objekt übergebene Encapsulation Stream.</span><span class="sxs-lookup"><span data-stu-id="3ae27-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="3ae27-123">Wenn das TNEF-Objekt mit dem TNEF_DECODE-Flag geöffnet wurde, wird die Methode **Fertig stellen** decodiert die Eigenschaften aus dem TNEF-Stream und schreibt sie zurück in die Nachricht, der sie angehören.</span><span class="sxs-lookup"><span data-stu-id="3ae27-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="3ae27-124">Nach dem Aufruf von **Fertig stellen** der Zeiger in den Stream Kapselung bis zum Ende der TNEF Daten zeigt.</span><span class="sxs-lookup"><span data-stu-id="3ae27-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="3ae27-125">Wenn der Anbieter oder Gateway muss die TNEF-Stream-Daten verwenden Sie nach dem Aufrufen der **Fertig stellen** , muss es den Zeiger Stream an den Anfang der Streamdaten TNEF zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="3ae27-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="3ae27-126">Die TNEF-Implementierung meldet TNEF Stream Codierung Probleme ohne Anhalten des Prozesses **Fertig stellen** .</span><span class="sxs-lookup"><span data-stu-id="3ae27-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="3ae27-127">Die [STnefProblemArray](stnefproblemarray.md) -Struktur zurückgegeben, die in der _LpProblem_ -Parameter gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="3ae27-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="3ae27-128">Der im **Scode** -Member, eine der in **STnefProblemArray** enthaltenen **STnefProblem** Strukturen zurückgegebene Wert gibt an, das Problem.</span><span class="sxs-lookup"><span data-stu-id="3ae27-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="3ae27-129">Der Anbieter oder Gateway kann auf der Annahme arbeiten, dass alle Eigenschaften oder Attribute für die **Fertig stellen** kein Problemberichts zurückgibt erfolgreich verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="3ae27-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="3ae27-130">Wenn Sie einen Anbieter oder ein Gateway mit Problem Arrays nicht funktionsfähig ist, können sie NULL _LpProblem_übergeben; In diesem Fall wird kein Problem Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3ae27-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="3ae27-131">Der in _LpProblem_ zurückgegebene Wert ist nur gültig, wenn der Aufruf gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="3ae27-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="3ae27-132">Wenn S_OK zurückgegeben wird, sollte der Anbieter oder ein Gateway in der Struktur **STnefProblemArray** zurückgegebenen Werte überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3ae27-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="3ae27-133">Bei einem beim Aufruf Fehler die **STnefProblemArray** -Struktur ist nicht ausgefüllt und die aufrufende Anbieter oder das Gateway nicht verwenden oder die Struktur frei.</span><span class="sxs-lookup"><span data-stu-id="3ae27-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="3ae27-134">Wenn dem Gespräch tritt kein Fehler auf, muss die aufrufende Anbieter oder Gateway den Speicher freizugeben für die **STnefProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3ae27-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3ae27-135">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="3ae27-135">MFCMAPI reference</span></span>

<span data-ttu-id="3ae27-136">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3ae27-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3ae27-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="3ae27-137">**File**</span></span>|<span data-ttu-id="3ae27-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="3ae27-138">**Function**</span></span>|<span data-ttu-id="3ae27-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="3ae27-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3ae27-140">File.cpp</span><span class="sxs-lookup"><span data-stu-id="3ae27-140">File.cpp</span></span>  <br/> |<span data-ttu-id="3ae27-141">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="3ae27-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="3ae27-142">MFCMAPI (engl.) verwendet die **ITnef::Finish** -Methode des neuen TNEF-Streams abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3ae27-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ae27-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ae27-143">See also</span></span>



[<span data-ttu-id="3ae27-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="3ae27-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="3ae27-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3ae27-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3ae27-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="3ae27-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="3ae27-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="3ae27-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="3ae27-148">PidTagAttachNumber (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3ae27-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="3ae27-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="3ae27-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="3ae27-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ae27-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="3ae27-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="3ae27-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

