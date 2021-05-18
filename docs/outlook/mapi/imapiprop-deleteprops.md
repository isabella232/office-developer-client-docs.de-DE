---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5bfef87baa2dffa4605f9a7afa3833024f514430
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409237"
---
# <a name="imapipropdeleteprops"></a><span data-ttu-id="63b2e-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="63b2e-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="63b2e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63b2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63b2e-105">Löscht eine oder mehrere Eigenschaften aus einem Objekt.</span><span class="sxs-lookup"><span data-stu-id="63b2e-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="63b2e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63b2e-106">Parameters</span></span>

 <span data-ttu-id="63b2e-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="63b2e-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="63b2e-108">[in] Ein Zeiger auf ein Array von Eigenschaftstags, die die zu löschenden Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="63b2e-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="63b2e-109">Das **cValues-Element** der [SPropTagArray-Struktur,](sproptagarray.md) auf die  _von lpPropTagArray_ verwiesen wird, darf nicht Null sein, und der  _lpPropTagArray-Parameter_ selbst darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="63b2e-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="63b2e-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="63b2e-110">_lppProblems_</span></span>
  
> <span data-ttu-id="63b2e-111">[in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) Andernfalls NULL, was angibt, dass keine Fehlerinformationen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="63b2e-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="63b2e-112">Wenn  _lppProblems ein_ gültiger Zeiger auf Eingaben ist, gibt **DeleteProps** detaillierte Informationen zu Fehlern beim Löschen einer oder mehreren Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="63b2e-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="63b2e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63b2e-113">Return value</span></span>

<span data-ttu-id="63b2e-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="63b2e-114">S_OK</span></span> 
  
> <span data-ttu-id="63b2e-115">Eigenschaften wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="63b2e-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="63b2e-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="63b2e-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="63b2e-117">Der Aufrufer verfügt über unzureichende Berechtigungen zum Löschen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="63b2e-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63b2e-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63b2e-118">Remarks</span></span>

<span data-ttu-id="63b2e-119">Die **IMAPIProp::D eleteProps-Methode** entfernt eine oder mehrere Eigenschaften aus dem aktuellen Objekt.</span><span class="sxs-lookup"><span data-stu-id="63b2e-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="63b2e-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="63b2e-120">Notes to implementers</span></span>

<span data-ttu-id="63b2e-121">Sie müssen nicht zulassen, dass Eigenschaften aus allen Objekten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="63b2e-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="63b2e-122">Wenn das Objekt nicht veränderbar ist, geben Sie MAPI_E_NO_ACCESS **deleteProps-Methode** zurück.</span><span class="sxs-lookup"><span data-stu-id="63b2e-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="63b2e-123">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="63b2e-123">Notes to callers</span></span>

<span data-ttu-id="63b2e-124">Sie müssen nicht den Eigenschaftentyp für jedes Eigenschaftstag im Eigenschaftentagarray festlegen, auf das der  _lpPropTagArray-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="63b2e-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="63b2e-125">Eigenschaftstypen werden ignoriert. nur die Eigenschaftsbezeichner werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="63b2e-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="63b2e-126">Beachten Sie, dass einige Objekte keine Änderung zulassen und dass diese Objekte MAPI_E_NO_ACCESS **deleteProps-Methode** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="63b2e-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="63b2e-127">Bei anderen Objekten können einige Eigenschaften gelöscht werden, andere jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="63b2e-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="63b2e-128">Wenn ein Problem beim Löschen nur einiger Eigenschaften besteht, gibt **DeleteProps** S_OK.</span><span class="sxs-lookup"><span data-stu-id="63b2e-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="63b2e-129">Wenn Sie einen gültigen Zeiger im  _lppProblems-Parameter_ übergeben haben, legt **DeleteProps** den Zeiger auf eine **SPropProblemArray-Struktur** fest, die detaillierte Informationen zu den Problemen mit jeder Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="63b2e-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="63b2e-130">Wenn Sie beispielsweise alle Eigenschaften einer Nachricht löschen und ein Problem mit einer oder mehreren Anlagen besteht, enthält die **SPropProblemArray-Struktur** einen Eintrag für die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="63b2e-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="63b2e-131">Die Struktur, auf die  _lppProblems_ verweist, ist nur gültig, wenn **DeleteProps** S_OK.</span><span class="sxs-lookup"><span data-stu-id="63b2e-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="63b2e-132">Wenn **DeleteProps** einen Fehler zurückgibt, versuchen Sie nicht, die **SPropProblemArray-Struktur zu** verwenden.</span><span class="sxs-lookup"><span data-stu-id="63b2e-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="63b2e-133">Rufen Sie stattdessen die [IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) des Objekts auf, um weitere Informationen zum Fehler zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="63b2e-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="63b2e-134">Geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="63b2e-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="63b2e-135">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="63b2e-135">MFCMAPI reference</span></span>

<span data-ttu-id="63b2e-136">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="63b2e-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="63b2e-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="63b2e-137">**File**</span></span>|<span data-ttu-id="63b2e-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="63b2e-138">**Function**</span></span>|<span data-ttu-id="63b2e-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="63b2e-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="63b2e-140">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="63b2e-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="63b2e-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="63b2e-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="63b2e-142">MFCMAPI verwendet die **IMAPIProp::D eleteProps-Methode,** um eine Eigenschaft aus einem Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="63b2e-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63b2e-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63b2e-143">See also</span></span>



[<span data-ttu-id="63b2e-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="63b2e-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="63b2e-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="63b2e-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="63b2e-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="63b2e-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="63b2e-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="63b2e-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="63b2e-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="63b2e-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="63b2e-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="63b2e-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="63b2e-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63b2e-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="63b2e-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="63b2e-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

