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
# <a name="imapipropdeleteprops"></a><span data-ttu-id="2ee0c-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="2ee0c-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="2ee0c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ee0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ee0c-105">Löscht eine oder mehrere Eigenschaften aus einem Objekt.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="2ee0c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ee0c-106">Parameters</span></span>

 <span data-ttu-id="2ee0c-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="2ee0c-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="2ee0c-108">in Ein Zeiger auf ein Array von Property-Tags, die die zu löschenden Eigenschaften anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="2ee0c-109">Das **cValues** -Element der [SPropTagArray](sproptagarray.md) -Struktur, auf die durch _lpPropTagArray_ verwiesen wird, darf nicht NULL sein, und der _lpPropTagArray_ -Parameter selbst darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="2ee0c-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="2ee0c-110">_lppProblems_</span></span>
  
> <span data-ttu-id="2ee0c-111">[in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur; andernfalls NULL, was bedeutet, dass keine Fehlerinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="2ee0c-112">Wenn _lppProblems_ ein gültiger Zeiger auf der Eingabe ist, gibt **DeleteProps** detaillierte Informationen zu Fehlern beim Löschen einer oder mehrerer Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2ee0c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ee0c-113">Return value</span></span>

<span data-ttu-id="2ee0c-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ee0c-114">S_OK</span></span> 
  
> <span data-ttu-id="2ee0c-115">Eigenschaften wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="2ee0c-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2ee0c-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="2ee0c-117">Der Aufrufer verfügt nicht über ausreichende Berechtigungen zum Löschen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ee0c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ee0c-118">Remarks</span></span>

<span data-ttu-id="2ee0c-119">Die **IMAPIProp::D eleteprops** -Methode entfernt eine oder mehrere Eigenschaften aus dem aktuellen Objekt.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2ee0c-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="2ee0c-120">Notes to implementers</span></span>

<span data-ttu-id="2ee0c-121">Sie müssen nicht zulassen, dass Eigenschaften aus allen Objekten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="2ee0c-122">Wenn das Objekt nicht geändert werden kann, geben Sie MAPI_E_NO_ACCESS von der **DeleteProps** -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2ee0c-123">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="2ee0c-123">Notes to callers</span></span>

<span data-ttu-id="2ee0c-124">Sie müssen den Eigenschaftentyp für jedes Property-Tag im Property Tag-Array, auf das durch den _lpPropTagArray_ -Parameter verwiesen wird, nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="2ee0c-125">Eigenschaftstypen werden ignoriert; nur die Eigenschaftenbezeichner werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="2ee0c-126">Beachten Sie, dass einige Objekte keine Änderung zulassen und diese Objekte MAPI_E_NO_ACCESS von der **DeleteProps** -Methode zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="2ee0c-127">Andere Objekte erlauben, dass einige Eigenschaften gelöscht werden, nicht aber andere.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="2ee0c-128">Wenn beim Löschen von nur einigen Eigenschaften ein Problem auftritt, gibt **DELETEPROPS** S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="2ee0c-129">Wenn Sie einen gültigen Zeiger im _lppProblems_ -Parameter übergeben haben, legt **DeleteProps** den Zeiger auf eine **SPropProblemArray** -Struktur fest, die detaillierte Informationen zu den Problemen mit den einzelnen Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="2ee0c-130">Wenn Sie beispielsweise alle Eigenschaften einer Nachricht löschen und ein Problem mit einer oder mehreren ihrer Anlagen vorliegt, enthält die **SPropProblemArray** -Struktur einen Eintrag für die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments ( ](pidtagmessageattachments-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="2ee0c-131">Die Struktur, auf die durch _lppProblems_ verwiesen wird, ist nur gültig, wenn **DeleteProps** S_OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="2ee0c-132">Wenn **DeleteProps** einen Fehler zurückgibt, versuchen Sie nicht, die **SPropProblemArray** -Struktur zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="2ee0c-133">Rufen Sie stattdessen die [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) -Methode des Objekts auf, um weitere Informationen zum Fehler abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="2ee0c-134">Freigeben Sie die zurückgegebene **SPropProblemArray** -Struktur durch Aufrufen der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2ee0c-135">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="2ee0c-135">MFCMAPI reference</span></span>

<span data-ttu-id="2ee0c-136">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2ee0c-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="2ee0c-137">**File**</span></span>|<span data-ttu-id="2ee0c-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="2ee0c-138">**Function**</span></span>|<span data-ttu-id="2ee0c-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="2ee0c-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2ee0c-140">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="2ee0c-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2ee0c-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="2ee0c-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="2ee0c-142">MFCMAPI verwendet die **IMAPIProp::D eleteprops** -Methode, um eine Eigenschaft aus einem Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="2ee0c-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ee0c-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ee0c-143">See also</span></span>



[<span data-ttu-id="2ee0c-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2ee0c-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="2ee0c-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="2ee0c-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="2ee0c-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="2ee0c-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="2ee0c-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2ee0c-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2ee0c-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="2ee0c-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="2ee0c-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="2ee0c-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="2ee0c-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ee0c-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="2ee0c-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="2ee0c-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

