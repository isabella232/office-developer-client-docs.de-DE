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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8eb19f9a2d3458e153b0758b56c502ce612be0cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792290"
---
# <a name="imapipropdeleteprops"></a><span data-ttu-id="91784-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="91784-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="91784-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91784-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91784-105">Löscht eine oder mehrere Eigenschaften aus einem Objekt.</span><span class="sxs-lookup"><span data-stu-id="91784-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="91784-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="91784-106">Parameters</span></span>

 <span data-ttu-id="91784-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="91784-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="91784-108">[in] Ein Zeiger auf ein Array von Eigenschaftentags, die die zu löschenden Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="91784-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="91784-109">Das **cValues** Mitglied der [SPropTagArray](sproptagarray.md) -Struktur, die auf den _LpPropTagArray_ darf nicht NULL sein, und der _LpPropTagArray_ -Parameter selbst darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="91784-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="91784-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="91784-110">_lppProblems_</span></span>
  
> <span data-ttu-id="91784-111">[in, out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur. andernfalls NULL, was bedeutet, dass es keine Notwendigkeit Fehlerinformationen besteht.</span><span class="sxs-lookup"><span data-stu-id="91784-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="91784-112">Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **"DeleteProps"** detaillierte Informationen zu Fehlern beim Löschen einer oder mehrerer Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91784-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="91784-113">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="91784-113">Return value</span></span>

<span data-ttu-id="91784-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="91784-114">S_OK</span></span> 
  
> <span data-ttu-id="91784-115">Eigenschaften wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="91784-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="91784-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="91784-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="91784-117">Der Aufrufer verfügt nicht über ausreichende Berechtigungen zum Löschen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91784-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91784-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91784-118">Remarks</span></span>

<span data-ttu-id="91784-119">Die **IMAPIProp::DeleteProps** -Methode entfernt eine oder mehrere Eigenschaften aus dem aktuellen Objekt.</span><span class="sxs-lookup"><span data-stu-id="91784-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="91784-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="91784-120">Notes to implementers</span></span>

<span data-ttu-id="91784-121">Sie müssen keinen Eigenschaften aller Objekte gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="91784-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="91784-122">Wenn das Objekt nicht geändert werden kann, geben Sie MAPI_E_NO_ACCESS von der **"DeleteProps"** -Methode.</span><span class="sxs-lookup"><span data-stu-id="91784-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="91784-123">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="91784-123">Notes to callers</span></span>

<span data-ttu-id="91784-124">Sie müssen keinen den Eigenschaftstyp für jede Eigenschaftentag in der Tag-Array-Eigenschaft auf das durch den Parameter _LpPropTagArray_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="91784-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="91784-125">Eigenschaftentypen werden ignoriert. Es werden nur die Eigenschaftenbezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="91784-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="91784-126">Beachten Sie, dass einige Objekte keine Änderung zulassen und diese Objekte MAPI_E_NO_ACCESS von der Methode **"DeleteProps"** zurück.</span><span class="sxs-lookup"><span data-stu-id="91784-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="91784-127">Andere Objekte können einige Eigenschaften gelöscht werden soll, jedoch nicht für andere Benutzer.</span><span class="sxs-lookup"><span data-stu-id="91784-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="91784-128">Wenn ein Problem löschen nur einige der Eigenschaften vorhanden ist, wird **"DeleteProps"** S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="91784-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="91784-129">Wenn Sie einen gültigen Zeiger im _LppProblems_ -Parameter übergeben haben, wird **"DeleteProps"** den Zeiger auf eine Struktur **SPropProblemArray** festlegen, detaillierte Informationen zu den Problemen, wobei jede Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="91784-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="91784-130">Beispielsweise wird Wenn Sie alle Eigenschaften einer Nachricht löschen, und es ein Problem mit einem oder mehreren der zugehörigen Anlagen ist, die **SPropProblemArray** -Struktur einen Eintrag enthalten für die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="91784-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="91784-131">Die Struktur, die auf den _LppProblems_ ist nur gültig, wenn **"DeleteProps"** gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="91784-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="91784-132">Wenn **"DeleteProps"** einen Fehler zurückgibt, versuchen Sie nicht die Struktur **SPropProblemArray** verwenden.</span><span class="sxs-lookup"><span data-stu-id="91784-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="91784-133">Rufen Sie stattdessen das Objekt [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode, um weitere Informationen zu dem Fehler zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="91784-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="91784-134">Frei die zurückgegebene Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="91784-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="91784-135">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="91784-135">MFCMAPI reference</span></span>

<span data-ttu-id="91784-136">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="91784-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="91784-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="91784-137">**File**</span></span>|<span data-ttu-id="91784-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="91784-138">**Function**</span></span>|<span data-ttu-id="91784-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="91784-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="91784-140">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="91784-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="91784-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="91784-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="91784-142">MFCMAPI (engl.) verwendet die **IMAPIProp::DeleteProps** -Methode, um eine Eigenschaft aus einem Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="91784-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91784-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91784-143">See also</span></span>



[<span data-ttu-id="91784-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="91784-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="91784-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="91784-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="91784-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="91784-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="91784-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="91784-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="91784-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="91784-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="91784-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="91784-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="91784-150">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="91784-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="91784-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="91784-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

