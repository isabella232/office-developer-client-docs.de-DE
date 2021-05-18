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
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412618"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="8f0b4-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="8f0b4-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="8f0b4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f0b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f0b4-105">Aktualisiert eine oder mehrere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="8f0b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f0b4-106">Parameters</span></span>

 <span data-ttu-id="8f0b4-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="8f0b4-107">_cValues_</span></span>
  
> <span data-ttu-id="8f0b4-108">[in] Die Anzahl der Eigenschaftswerte, auf die der  _lpPropArray-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="8f0b4-109">Der  _cValues-Parameter_ darf nicht 0 sein.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="8f0b4-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="8f0b4-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="8f0b4-111">[in] Ein Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die Eigenschaftswerte enthalten, die aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="8f0b4-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="8f0b4-112">_lppProblems_</span></span>
  
> <span data-ttu-id="8f0b4-113">[in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls NULL, was angibt, dass keine Fehlerinformationen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="8f0b4-114">Wenn  _lppProblems ein_ gültiger Zeiger auf Eingaben ist, gibt **SetProps** detaillierte Informationen zu Fehlern beim Aktualisieren einer oder mehreren Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8f0b4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f0b4-115">Return value</span></span>

<span data-ttu-id="8f0b4-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8f0b4-116">S_OK</span></span> 
  
> <span data-ttu-id="8f0b4-117">Die Eigenschaften wurden erfolgreich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="8f0b4-118">Die folgenden Werte können in der **SPropProblemArray-Struktur** zurückgegeben werden, jedoch nicht als Rückgabewerte für **SetProps:**</span><span class="sxs-lookup"><span data-stu-id="8f0b4-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="8f0b4-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8f0b4-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="8f0b4-120">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="8f0b4-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="8f0b4-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="8f0b4-122">Die Eigenschaft kann nicht aktualisiert werden, da sie schreibgeschützt ist und vom Dienstanbieter berechnet wird, der für das Objekt zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="8f0b4-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="8f0b4-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="8f0b4-124">Der Eigenschaftentyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-124">The property type is invalid.</span></span>
    
<span data-ttu-id="8f0b4-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8f0b4-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8f0b4-126">Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zu zugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="8f0b4-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="8f0b4-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="8f0b4-128">Die Eigenschaft kann nicht aktualisiert werden, da sie größer als die Größe des RPC-Puffers (Remote Procedure Call) ist.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="8f0b4-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="8f0b4-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="8f0b4-130">Der Eigenschaftstyp ist nicht der Typ, der von der aufrufenden Implementierung erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="8f0b4-131">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="8f0b4-131">Notes to implementers</span></span>

<span data-ttu-id="8f0b4-132">Ignorieren Sie **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md))-Eigenschaftstag und alle Eigenschaften mit dem Typ **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="8f0b4-133">Nehmen Sie keine Änderungen vor oder melden Sie keine Probleme in der **SPropProblemArray-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="8f0b4-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="8f0b4-134">Gibt MAPI_E_INVALID_PARAMETER zurück, wenn eine Eigenschaft vom Typ **PT_OBJECT** im Eigenschaftenwertarray enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="8f0b4-135">Geben Sie diesen Fehler auch zurück, wenn eine Eigenschaft mit mehreren Wert im Array enthalten ist und der **cValues-Member** auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="8f0b4-136">Wenn der Aufruf insgesamt erfolgreich ist, es jedoch Probleme beim Festlegen einiger Eigenschaften gibt, geben Sie S_OK zurück, und geben Sie Informationen zu den Problemen in den entsprechenden Eintrag der **SPropProblemArray-Struktur** ein, auf die der  _lppProblems-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8f0b4-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8f0b4-137">Notes to callers</span></span>

<span data-ttu-id="8f0b4-138">Je nach Dienstanbieter können Sie den Eigenschaftentyp auch ändern, indem Sie ein Eigenschaftentag übergeben, das einen anderen Typ enthält als zuvor mit einer bestimmten Eigenschafts-ID verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="8f0b4-139">Wenn Sie ein Eigenschaftstag für eine Eigenschaft hinzufügen, die vom Objekt nicht unterstützt wird und die Implementierung von **SetProps** die Erstellung neuer Eigenschaften ermöglicht, wird die Eigenschaft dem Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="8f0b4-140">Alle vorherigen Werte, die mit dem Eigenschaftenbezeichner gespeichert wurden, der für die neue Eigenschaft verwendet wurde, werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="8f0b4-141">Beachten Sie, dass S_OK Rückgabewert nicht garantiert, dass alle Eigenschaften erfolgreich aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="8f0b4-142">Einige Anbieter **zwischenspeichern SetProps-Anrufe,** bis sie einen Anruf erhalten, für den ein Anbietereingriff erforderlich ist, z. B. [IMAPIProp::SaveChanges](imapiprop-savechanges.md) oder [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="8f0b4-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="8f0b4-143">Daher können Fehlerwerte empfangen werden, die sich auf den **SetProps-Aufruf** mit den späteren Aufrufen beziehen.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="8f0b4-144">Wenn **SetProps** S_OK, überprüfen Sie die **SPropProblemArray-Struktur,** auf die von  _lppProblems_ verwiesen wird, auf Probleme beim Aktualisieren einzelner Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="8f0b4-145">Wenn **SetProps** einen Fehler zurückgibt, überprüfen Sie das Eigenschaftenproblemarray nicht.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="8f0b4-146">Rufen Sie stattdessen die [IMAPIProp::GetLastError-Methode des Objekts](imapiprop-getlasterror.md) auf.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="8f0b4-147">Beim Aktualisieren großer Eigenschaften **kann SetProps** fehler- und MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="8f0b4-148">Es gibt keine maximale Größe für Eigenschaften, und unterschiedliche Objekte können unterschiedliche Grenzwerte haben.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="8f0b4-149">Wenn Sie mit potenziell großen Eigenschaften zu tun haben, können Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) mit IID_IStream als Schnittstellenbezeichner aufrufen, wenn **SetProps** diesen Fehlerwert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="8f0b4-150">Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um die **SPropProblemArray-Struktur frei** zu geben.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8f0b4-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="8f0b4-151">MFCMAPI reference</span></span>

<span data-ttu-id="8f0b4-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8f0b4-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8f0b4-153">**File**</span></span>|<span data-ttu-id="8f0b4-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8f0b4-154">**Function**</span></span>|<span data-ttu-id="8f0b4-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8f0b4-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8f0b4-156">PropertyEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="8f0b4-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="8f0b4-157">CPropertyEditor::WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="8f0b4-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="8f0b4-158">MFCMAPI verwendet die **IMAPIProp::SetProps-Methode,** um eine Eigenschaft zurück in ein Objekt zu schreiben, nachdem die Eigenschaft bearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="8f0b4-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8f0b4-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f0b4-159">See also</span></span>



[<span data-ttu-id="8f0b4-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8f0b4-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="8f0b4-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="8f0b4-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="8f0b4-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="8f0b4-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="8f0b4-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8f0b4-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="8f0b4-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8f0b4-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8f0b4-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="8f0b4-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="8f0b4-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8f0b4-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="8f0b4-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f0b4-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

