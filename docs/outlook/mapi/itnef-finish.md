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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435677"
---
# <a name="itneffinish"></a><span data-ttu-id="8d397-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="8d397-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="8d397-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d397-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d397-105">Beendet die Verarbeitung aller TNEF-Vorgänge (Transport Neutral Encapsulation Format), die in der Warteschlange gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="8d397-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="8d397-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d397-106">Parameters</span></span>

 <span data-ttu-id="8d397-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d397-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8d397-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="8d397-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8d397-109">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="8d397-109">_lpKey_</span></span>
  
> <span data-ttu-id="8d397-110">Out Ein Zeiger auf die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Schlüsseleigenschaft einer Anlage.</span><span class="sxs-lookup"><span data-stu-id="8d397-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="8d397-111">Das TNEF-Kapselungs Objekt verwendet diesen Schlüssel, um eine Anlage mit dem Attachment-Platzierungs-Tag in einer Nachricht abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="8d397-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="8d397-112">Dieser Schlüssel sollte für jede Anlage eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="8d397-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="8d397-113">_lpProblem_</span><span class="sxs-lookup"><span data-stu-id="8d397-113">_lpProblem_</span></span>
  
> <span data-ttu-id="8d397-114">Out Ein Zeiger auf einen Zeiger auf eine zurückgegebene [STnefProblemArray](stnefproblemarray.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8d397-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="8d397-115">Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="8d397-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="8d397-116">Wenn NULL im _lpProblem_ -Parameter übergeben wird, wird kein Property-Problem-Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d397-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8d397-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d397-117">Return value</span></span>

<span data-ttu-id="8d397-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d397-118">S_OK</span></span> 
  
> <span data-ttu-id="8d397-119">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d397-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d397-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d397-120">Remarks</span></span>

<span data-ttu-id="8d397-121">Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef:: Finish** -Methode auf, um die Codierung aller Eigenschaften auszuführen, für die die Codierung in Aufrufen der [ITnef::](itnef-addprops.md) AddProps-und [ITnef:](itnef-setprops.md) : SetProps-Methoden angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="8d397-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="8d397-122">Wenn das TNEF-Objekt mit dem TNEF_ENCODE-Flag für die [OpenTnefStream](opentnefstream.md) -oder die [OpenTnefStreamEx](opentnefstreamex.md) -Funktion geöffnet wurde, codiert die **Finish** -Methode die angeforderten Eigenschaften in den an dieses Objekt übergebenen Kapselungs Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="8d397-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="8d397-123">Wenn das TNEF-Objekt mit dem TNEF_DECODE-Flag geöffnet wurde, dekodiert die **Finish** -Methode die Eigenschaften aus dem TNEF-Stream und schreibt Sie zurück in die Nachricht, zu der Sie gehören.</span><span class="sxs-lookup"><span data-stu-id="8d397-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="8d397-124">Nach dem **Finish** -Aufruf zeigt der Zeiger auf den Encapsulation-Stream auf das Ende der TNEF-Daten.</span><span class="sxs-lookup"><span data-stu-id="8d397-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="8d397-125">Wenn der Anbieter oder das Gateway die TNEF-Streamdaten nach dem **Beendigungs** Aufruf verwenden muss, muss er den Stream-Zeiger auf den Anfang der TNEF-Datenstrom zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="8d397-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="8d397-126">Die TNEF-Implementierung meldet TNEF-Datenstrom Codierungsprobleme, ohne den **Abschluss** Prozess zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8d397-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="8d397-127">Die im Parameter _lpProblem_ zurückgeGebene [STnefProblemArray](stnefproblemarray.md) -Struktur gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnten.</span><span class="sxs-lookup"><span data-stu-id="8d397-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="8d397-128">Der Wert, der im **SCODE** -Element einer der in **STnefProblemArray** enthaltenen **STnefProblem** -Strukturen zurückgegeben wird, gibt das spezifische Problem an.</span><span class="sxs-lookup"><span data-stu-id="8d397-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="8d397-129">Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **Finish** keinen Problembericht zurückgibt, erfolgreich verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="8d397-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="8d397-130">Wenn ein Anbieter oder Gateway nicht mit Problem Arrays funktioniert, kann er in _lpProblem_den Wert NULL überschreiten; in diesem Fall wird kein Problem Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d397-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="8d397-131">Der in _lpProblem_ zurückgegebene Wert ist nur gültig, wenn der Aufruf S_OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8d397-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="8d397-132">Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die in der **STnefProblemArray** -Struktur zurückgegebenen Werte überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8d397-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="8d397-133">Wenn für den Anruf ein Fehler auftritt, wird die **STnefProblemArray** -Struktur nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder freigeben.</span><span class="sxs-lookup"><span data-stu-id="8d397-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="8d397-134">Wenn beim Aufruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Speicher für das **STnefProblemArray** freigeben, indem er die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="8d397-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8d397-135">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="8d397-135">MFCMAPI reference</span></span>

<span data-ttu-id="8d397-136">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8d397-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8d397-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8d397-137">**File**</span></span>|<span data-ttu-id="8d397-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8d397-138">**Function**</span></span>|<span data-ttu-id="8d397-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8d397-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d397-140">Datei. cpp</span><span class="sxs-lookup"><span data-stu-id="8d397-140">File.cpp</span></span>  <br/> |<span data-ttu-id="8d397-141">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="8d397-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="8d397-142">MFCMAPI verwendet die **ITnef:: Finish** -Methode, um die Verarbeitung des neuen TNEF-Streams abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="8d397-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d397-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d397-143">See also</span></span>



[<span data-ttu-id="8d397-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="8d397-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="8d397-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8d397-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8d397-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="8d397-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="8d397-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="8d397-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="8d397-148">Kanonische Pidtagattachnumber (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8d397-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="8d397-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="8d397-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="8d397-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d397-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="8d397-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8d397-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

