---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 93bfcce9c45a4c6fd4d57be8c1222be286e0a945
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592031"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="eadaa-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="eadaa-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="eadaa-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eadaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eadaa-105">Aktualisiert eine oder mehrere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eadaa-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="eadaa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eadaa-106">Parameters</span></span>

 <span data-ttu-id="eadaa-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="eadaa-107">_cValues_</span></span>
  
> <span data-ttu-id="eadaa-108">[in] Die Anzahl der Eigenschaftswerte, die auf den durch den Parameter _LpPropArray_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="eadaa-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="eadaa-109">Der Parameter _cValues_ darf nicht 0 sein.</span><span class="sxs-lookup"><span data-stu-id="eadaa-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="eadaa-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="eadaa-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="eadaa-111">[in] Ein Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die enthalten Eigenschaftswerte aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="eadaa-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="eadaa-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="eadaa-112">_lppProblems_</span></span>
  
> <span data-ttu-id="eadaa-113">[in, out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur. andernfalls NULL zurück, der keine Notwendigkeit zur Fehlerinformationen angibt.</span><span class="sxs-lookup"><span data-stu-id="eadaa-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="eadaa-114">Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **SetProps** detaillierte Informationen zu Fehlern beim Aktualisieren einer oder mehrerer Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="eadaa-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eadaa-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="eadaa-115">Return value</span></span>

<span data-ttu-id="eadaa-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="eadaa-116">S_OK</span></span> 
  
> <span data-ttu-id="eadaa-117">Die Eigenschaften wurden erfolgreich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="eadaa-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="eadaa-118">Die folgenden Werte können in der Struktur **SPropProblemArray** , aber nicht als Rückgabewerte für **SetProps**zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="eadaa-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="eadaa-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="eadaa-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="eadaa-120">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="eadaa-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="eadaa-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="eadaa-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="eadaa-122">Die Eigenschaft kann nicht aktualisiert werden, da es schreibgeschützt ist berechnet, indem der Dienstanbieter, der für das Objekt zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="eadaa-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="eadaa-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="eadaa-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="eadaa-124">Der Eigenschaftstyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="eadaa-124">The property type is invalid.</span></span>
    
<span data-ttu-id="eadaa-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="eadaa-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="eadaa-126">Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="eadaa-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="eadaa-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="eadaa-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="eadaa-128">Die Eigenschaft kann nicht aktualisiert werden, da es größer als die Größe des Puffers Remoteprozeduraufruf Remoteprozeduraufruf (RPC) ist.</span><span class="sxs-lookup"><span data-stu-id="eadaa-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="eadaa-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="eadaa-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="eadaa-130">Der Eigenschaftentyp ist nicht von der aufrufenden Implementierung erwartet.</span><span class="sxs-lookup"><span data-stu-id="eadaa-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="eadaa-131">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="eadaa-131">Notes to implementers</span></span>

<span data-ttu-id="eadaa-132">Ignorieren Sie das Eigenschafts-Tag **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) und alle Eigenschaften mit einem **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="eadaa-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="eadaa-133">Stellen Sie in der Struktur **SPropProblemArray** nicht geändert oder Probleme melden.</span><span class="sxs-lookup"><span data-stu-id="eadaa-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="eadaa-134">MAPI_E_INVALID_PARAMETER zurück, wenn eine Eigenschaft vom Typ **PT_OBJECT** im Array-Wert Eigenschaft enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="eadaa-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="eadaa-135">Auch zurückgeben Sie, dass dieser Fehler, wenn eine mehrwertige Eigenschaft in das Array und seine Member **cValues** einbezogen wird auf 0 gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="eadaa-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="eadaa-136">Wenn der Aufruf erfolgreich insgesamt ist, aber es Probleme treten mit dem einige der Eigenschaften festlegen, wird zurückgegeben Sie S_OK, und platzieren Sie Informationen zu den Problemen in den entsprechenden Eintrag der **SPropProblemArray** -Struktur, der auf der _LppProblems_ -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="eadaa-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eadaa-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="eadaa-137">Notes to callers</span></span>

<span data-ttu-id="eadaa-138">Je nach den Dienstanbieter können Sie auch möglicherweise so ändern Sie den Eigenschaftentyp, indem Sie eine Eigenschaftentag, das einen anderen Typ enthält, als vorher mit einem bestimmten Eigenschaftenbezeichner verwendet wurde übergeben.</span><span class="sxs-lookup"><span data-stu-id="eadaa-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="eadaa-139">Wenn Sie eine Eigenschaftentag für eine Eigenschaft, die durch das Objekt nicht unterstützt wird und die Implementierung der **SetProps** die Erstellung von neuen Eigenschaften ermöglicht, ist die Eigenschaft auf das Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="eadaa-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="eadaa-140">Alle vorherigen Werte gespeichert, mit der Bezeichner, der für die neue Eigenschaft verwendet wurde, wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="eadaa-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="eadaa-141">Beachten Sie, dass der Rückgabewert S_OK nicht garantiert, dass alle Eigenschaften erfolgreich aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="eadaa-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="eadaa-142">Einige Anbieter cache **SetProps** Anrufe, bis sie einen Anruf entgegen, der vom Anbieter Eingriff, beispielsweise [IMAPIProp::SaveChanges](imapiprop-savechanges.md) oder [IMAPIProp::GetProps](imapiprop-getprops.md)erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="eadaa-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="eadaa-143">Aus diesem Grund ist es möglich, Fehlerwerte erhalten, die für den Aufruf der **SetProps** mit spätere Aufrufe beziehen.</span><span class="sxs-lookup"><span data-stu-id="eadaa-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="eadaa-144">Wenn **SetProps** S_OK zurückgegeben wird, überprüfen Sie die **SPropProblemArray** -Struktur, die auf den _LppProblems_ für Probleme bei der Aktualisierung der einzelner Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eadaa-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="eadaa-145">Wenn **SetProps** einen Fehler zurückgegeben wird, überprüfen Sie das Problem Array-Eigenschaft nicht.</span><span class="sxs-lookup"><span data-stu-id="eadaa-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="eadaa-146">Rufen Sie stattdessen das Objekt [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="eadaa-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="eadaa-147">Beim Aktualisieren großer Eigenschaften können **SetProps** fehl und MAPI_E_NOT_ENOUGH_MEMORY zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="eadaa-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="eadaa-148">Es wurde keine maximale Größe für Eigenschaften, und verschiedene Objekte können unterschiedliche Grenzwerte haben.</span><span class="sxs-lookup"><span data-stu-id="eadaa-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="eadaa-149">Wenn Sie mit potenziell großen-Eigenschaften arbeiten, bereiten Sie die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode mit IID_IStream als Schnittstellenbezeichner aufrufen, **SetProps** dieser Fehlerwert zurück.</span><span class="sxs-lookup"><span data-stu-id="eadaa-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="eadaa-150">Rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um die Struktur **SPropProblemArray** frei.</span><span class="sxs-lookup"><span data-stu-id="eadaa-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eadaa-151">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="eadaa-151">MFCMAPI reference</span></span>

<span data-ttu-id="eadaa-152">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="eadaa-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eadaa-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="eadaa-153">**File**</span></span>|<span data-ttu-id="eadaa-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="eadaa-154">**Function**</span></span>|<span data-ttu-id="eadaa-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="eadaa-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eadaa-156">PropertyEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="eadaa-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="eadaa-157">CPropertyEditor::WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="eadaa-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="eadaa-158">MFCMAPI (engl.) verwendet die **IMAPIProp::SetProps** -Methode zum Zurückschreiben einer Eigenschaft zu einem Objekt nach die Eigenschaft bearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="eadaa-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eadaa-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eadaa-159">See also</span></span>



[<span data-ttu-id="eadaa-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="eadaa-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="eadaa-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="eadaa-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="eadaa-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="eadaa-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="eadaa-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="eadaa-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="eadaa-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="eadaa-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="eadaa-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="eadaa-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="eadaa-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="eadaa-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="eadaa-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eadaa-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

