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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341013"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="c3154-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="c3154-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="c3154-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3154-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3154-105">Aktualisiert eine oder mehrere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3154-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="c3154-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3154-106">Parameters</span></span>

 <span data-ttu-id="c3154-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="c3154-107">_cValues_</span></span>
  
> <span data-ttu-id="c3154-108">in Die Anzahl der Eigenschaftswerte, auf die durch den _lpPropArray_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c3154-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="c3154-109">Der _cValues_ -Parameter darf nicht 0 sein.</span><span class="sxs-lookup"><span data-stu-id="c3154-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="c3154-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="c3154-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="c3154-111">in Ein Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die Eigenschaftswerte enthalten, die aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3154-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="c3154-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="c3154-112">_lppProblems_</span></span>
  
> <span data-ttu-id="c3154-113">[in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur; andernfalls NULL, was bedeutet, dass keine Fehlerinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c3154-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="c3154-114">Wenn _lppProblems_ ein gültiger Zeiger auf der Eingabe ist \*\*\*\* , gibt SetProps detaillierte Informationen zu Fehlern beim Aktualisieren einer oder mehrerer Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="c3154-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c3154-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3154-115">Return value</span></span>

<span data-ttu-id="c3154-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3154-116">S_OK</span></span> 
  
> <span data-ttu-id="c3154-117">Die Eigenschaften wurden erfolgreich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c3154-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="c3154-118">Die folgenden Werte können in der **SPropProblemArray** -Struktur zurückgegeben werden, jedoch nicht als Rückgabewerte für SetProps: \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c3154-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="c3154-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c3154-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c3154-120">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="c3154-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="c3154-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="c3154-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="c3154-122">Die Eigenschaft kann nicht aktualisiert werden, da sie schreibgeschützt ist und vom Dienstanbieter berechnet wird, der für das Objekt verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="c3154-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="c3154-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3154-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="c3154-124">Der Eigenschaftentyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c3154-124">The property type is invalid.</span></span>
    
<span data-ttu-id="c3154-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c3154-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c3154-126">Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="c3154-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="c3154-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="c3154-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="c3154-128">Die Eigenschaft kann nicht aktualisiert werden, da Sie größer als die RPC-Puffergröße (Remote Procedure Call) ist.</span><span class="sxs-lookup"><span data-stu-id="c3154-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="c3154-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3154-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="c3154-130">Der Eigenschaftentyp ist nicht der Typ, der von der aufrufenden Implementierung erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="c3154-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="c3154-131">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c3154-131">Notes to implementers</span></span>

<span data-ttu-id="c3154-132">Ignorieren Sie das **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md))-Eigenschaftentag und alle Eigenschaften mit einem Typ von **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="c3154-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="c3154-133">Nehmen Sie keine Änderungen vor, oder melden Sie Probleme in der **SPropProblemArray** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3154-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="c3154-134">Geben Sie MAPI_E_INVALID_PARAMETER zurück, wenn eine Eigenschaft vom Typ **PT_OBJECT** im Eigenschaftswert Array enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c3154-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="c3154-135">Geben Sie auch diesen Fehler zurück, wenn eine mehrwertige Eigenschaft im Array enthalten ist und dessen **cValues** -Element auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3154-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="c3154-136">Wenn der Aufruf insgesamt erfolgreich ist, aber Probleme beim Festlegen einiger Eigenschaften auftreten, geben Sie S_OK zurück, und setzen Sie Informationen zu den Problemen in den entsprechenden Eintrag der **SPropProblemArray** -Struktur, auf die der _lppProblems_ -Parameter zeigt.</span><span class="sxs-lookup"><span data-stu-id="c3154-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c3154-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c3154-137">Notes to callers</span></span>

<span data-ttu-id="c3154-138">Je nach Dienstanbieter können Sie möglicherweise auch den Eigenschaftentyp ändern, indem Sie ein Property-Tag übergeben, das einen anderen Typ als der zuvor mit einem angegebenen Eigenschaftenbezeichner verwendete ist.</span><span class="sxs-lookup"><span data-stu-id="c3154-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="c3154-139">Wenn Sie ein Property-Tag für eine Eigenschaft einfügen, die vom Objekt nicht unterstützt wird und die Implementierung \*\*\*\* von SetProps die Erstellung neuer Eigenschaften zulässt, wird die Eigenschaft dem Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c3154-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="c3154-140">Jeder vorherige Wert, der mit dem Eigenschaftenbezeichner gespeichert wurde, der für die neue Eigenschaft verwendet wurde, wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="c3154-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="c3154-141">Beachten Sie, dass der S_OK-Rückgabewert nicht garantiert, dass alle Eigenschaften erfolgreich aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c3154-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="c3154-142">Einige Anbieter speichern \*\*\*\* SetProps-Aufrufe, bis Sie einen Aufruf erhalten, der eine Anbieter Intervention erfordert, wie [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) oder [IMAPIProp::](imapiprop-getprops.md)GetProps.</span><span class="sxs-lookup"><span data-stu-id="c3154-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="c3154-143">Daher ist es möglich, Fehlerwerte zu erhalten, die sich auf \*\*\*\* den SetProps-Aufruf mit den späteren Aufrufen beziehen.</span><span class="sxs-lookup"><span data-stu-id="c3154-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="c3154-144">Wenn \*\*\*\* SetProps S_OK zurückgibt, überprüfen Sie die **SPropProblemArray** -Struktur, auf die durch _lppProblems_ für Probleme beim Aktualisieren einzelner Eigenschaften verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c3154-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="c3154-145">Wenn \*\*\*\* SetProps einen Fehler zurückgibt, überprüfen Sie nicht das Problem Array der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c3154-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="c3154-146">Rufen Sie stattdessen die [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) -Methode des Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="c3154-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="c3154-147">Beim Aktualisieren von umfangreichen \*\*\*\* Eigenschaften können SetProps fehlschlagen und MAPI_E_NOT_ENOUGH_MEMORY zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c3154-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="c3154-148">Es gibt keine maximale Größe für Eigenschaften, und verschiedene Objekte können unterschiedliche Begrenzungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c3154-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="c3154-149">Wenn Sie potenziell große Eigenschaften behandeln, müssen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode mit IID_IStream als Schnittstellenbezeichner aufrufen, wenn SetProps diesen Fehlerwert zurückgibt. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c3154-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="c3154-150">Rufen Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um die **SPropProblemArray** -Struktur freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c3154-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c3154-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="c3154-151">MFCMAPI reference</span></span>

<span data-ttu-id="c3154-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c3154-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c3154-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c3154-153">**File**</span></span>|<span data-ttu-id="c3154-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c3154-154">**Function**</span></span>|<span data-ttu-id="c3154-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c3154-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c3154-156">Eingeschaften. cpp</span><span class="sxs-lookup"><span data-stu-id="c3154-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="c3154-157">CPropertyEditor:: WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="c3154-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="c3154-158">MFCMAPI verwendet die **IMAPIProp::** SetProps-Methode, um eine Eigenschaft zurück in ein Objekt zu schreiben, nachdem die Eigenschaft bearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="c3154-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3154-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3154-159">See also</span></span>



[<span data-ttu-id="c3154-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c3154-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="c3154-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c3154-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="c3154-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="c3154-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="c3154-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c3154-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c3154-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c3154-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c3154-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c3154-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="c3154-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c3154-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="c3154-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c3154-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

