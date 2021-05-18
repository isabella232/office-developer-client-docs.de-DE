---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412457"
---
# <a name="imapipropgetprops"></a><span data-ttu-id="db89f-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="db89f-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="db89f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db89f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db89f-105">Ruft den Eigenschaftswert einer oder mehrere Eigenschaften eines Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="db89f-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="db89f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="db89f-106">Parameters</span></span>

 <span data-ttu-id="db89f-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="db89f-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="db89f-108">[in] Ein Zeiger auf ein Array von Eigenschaftstags, die die Eigenschaften identifizieren, deren Werte abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="db89f-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="db89f-109">Der  _lpPropTagArray-Parameter_ muss entweder NULL sein, der angibt, dass Werte für alle Eigenschaften des Objekts zurückgegeben werden sollen, oder auf eine [SPropTagArray-Struktur](sproptagarray.md) verweisen, die ein oder mehrere Eigenschaftstags enthält.</span><span class="sxs-lookup"><span data-stu-id="db89f-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="db89f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="db89f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="db89f-111">[in] Eine Bitmaske mit Flags, die das Format für Eigenschaften angibt, deren Typ PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="db89f-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="db89f-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="db89f-112">The following flag can be set:</span></span>
    
<span data-ttu-id="db89f-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="db89f-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="db89f-114">Die Zeichenfolgenwerte für diese Eigenschaften sollten im Unicode-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="db89f-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="db89f-115">Wenn das MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgenwerte im ANSI-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="db89f-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="db89f-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="db89f-116">_lpcValues_</span></span>
  
> <span data-ttu-id="db89f-117">[out] Ein Zeiger auf eine Anzahl von Eigenschaftswerten, auf die der  _lppPropArray-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="db89f-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="db89f-118">Wenn  _lppPropArray_ NULL ist, ist der Inhalt des  _lpcValues-Parameters_ null.</span><span class="sxs-lookup"><span data-stu-id="db89f-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="db89f-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="db89f-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="db89f-120">[out] Ein Zeiger auf einen Zeiger auf die abgerufenen Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="db89f-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="db89f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db89f-121">Return value</span></span>

<span data-ttu-id="db89f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="db89f-122">S_OK</span></span> 
  
> <span data-ttu-id="db89f-123">Die Eigenschaftswerte wurden erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="db89f-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="db89f-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="db89f-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="db89f-125">Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="db89f-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="db89f-126">Das **aulPropTag-Element** des Eigenschaftswerts für jede nicht verfügbare Eigenschaft hat den Eigenschaftstyp PT_ERROR und den Bezeichner Null.</span><span class="sxs-lookup"><span data-stu-id="db89f-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="db89f-127">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="db89f-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="db89f-128">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="db89f-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="db89f-129">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="db89f-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="db89f-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="db89f-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="db89f-131">Null wurde im **cValues-Element** der **SPropTagArray-Struktur** übergeben, auf das _lpPropTagArray verweist._</span><span class="sxs-lookup"><span data-stu-id="db89f-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="db89f-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="db89f-132">Remarks</span></span>

<span data-ttu-id="db89f-133">Die **IMAPIProp::GetProps-Methode** ruft die Eigenschaftswerte einer oder mehreren Eigenschaften eines Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="db89f-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="db89f-134">Die Eigenschaftswerte werden in der reihenfolge zurückgegeben, in der sie angefordert wurden (d. h. die Reihenfolge der Eigenschaften im Eigenschaftentagarray, auf die  _von lpPropTagArray_ verwiesen wird, entspricht der Reihenfolge im Array der Eigenschaftenwertstrukturen, auf die von  _lppPropArray_ verwiesen wird).</span><span class="sxs-lookup"><span data-stu-id="db89f-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="db89f-135">Die in den **aulPropTag-Membern** des Eigenschaftstagarrays angegebenen Eigenschaftstypen geben den Werttyp an, der im **Value-Element** jeder Eigenschaftswertstruktur zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="db89f-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="db89f-136">Wenn der Aufrufer jedoch den Typ einer Eigenschaft nicht kennt, kann der Typ im **aulPropTag-Element** stattdessen auf PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="db89f-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="db89f-137">Beim Abrufen des **Werts legt GetProps** den richtigen Typ im **aulPropTag-Element** der Eigenschaftswertstruktur für die Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="db89f-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="db89f-138">Wenn Eigenschaftstypen im **SPropTagArray** in _lpPropTagArray_ angegeben werden, verfügen die Eigenschaftswerte in der in _lppPropArray_ zurückgegebenen **SPropValue-Eigenschaft** über Typen, die exakt mit den angeforderten Typen übereinstimmen, es sei denn, stattdessen wird ein Fehlerwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db89f-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="db89f-139">Zeichenfolgeneigenschaften können einen von zwei Eigenschaftstypen aufweisen: PT_UNICODE, um das Unicode-Format und PT_STRING8 an das ANSI-Format zu stellen.</span><span class="sxs-lookup"><span data-stu-id="db89f-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="db89f-140">Wenn das MAPI_UNICODE im  _ulFlags-Parameter_ festgelegt ist, gibt GetProps immer dann seinen Wert im Unicode-Format zurück, wenn **GetProps** das entsprechende Format für eine Zeichenfolgeneigenschaft nicht bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="db89f-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="db89f-141">**GetProps kann** in den folgenden Situationen keinen genauen Zeichenfolgeneigenschaftentyp bestimmen:</span><span class="sxs-lookup"><span data-stu-id="db89f-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="db89f-142">Der  _lpPropTagArray-Parameter_ ist auf NULL festgelegt, um alle Eigenschaften an fordern.</span><span class="sxs-lookup"><span data-stu-id="db89f-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="db89f-143">Das **Element aulPropTag** enthält den Wert PT_UNSPECIFIED eigenschaftstyp im Eigenschaftentagarray.</span><span class="sxs-lookup"><span data-stu-id="db89f-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="db89f-144">Wenn der  _lpPropTagArray-Parameter_ auf NULL festgelegt ist, um alle Eigenschaften des Objekts abzurufen und keine Eigenschaften vorhanden sind, führt **GetProps** die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="db89f-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="db89f-145">Gibt S_OK.</span><span class="sxs-lookup"><span data-stu-id="db89f-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="db89f-146">Legt den Count-Wert im **cValues-Element** der Eigenschaftswertstruktur auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="db89f-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="db89f-147">Legt den Inhalt von  _lpcValues auf_ 0 fest.</span><span class="sxs-lookup"><span data-stu-id="db89f-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="db89f-148">Legt  _lppPropArray auf_ NULL fest.</span><span class="sxs-lookup"><span data-stu-id="db89f-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="db89f-149">**GetProps** darf keine Mehrwerteigenschaften zurückgeben, **wenn cValues** auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="db89f-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="db89f-150">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="db89f-150">Notes to implementers</span></span>

<span data-ttu-id="db89f-151">Rufen Sie die [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) auf, um zunächst Arbeitsspeicher für die [SPropValue-Struktur](spropvalue.md) zu reservieren, auf die  _von lpPropTagArray verwiesen wird._ rufen [Sie MAPIAllocateMore auf,](mapiallocatemore.md) um zusätzlichen Arbeitsspeicher zuzuordnen, der für die Mitglieder der Struktur erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="db89f-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="db89f-152">Geben MAPI_W_ERRORS_RETURNED zurück, wenn Sie den Wert für eine oder mehrere der angeforderten Eigenschaften nicht abrufen können.</span><span class="sxs-lookup"><span data-stu-id="db89f-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="db89f-153">Legen Sie in der Eigenschaftswertstruktur den Typ im **Element aulPropTag** auf PT_ERROR und value auf einen Statuscode fest, der den Fehler beschreibt. </span><span class="sxs-lookup"><span data-stu-id="db89f-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="db89f-154">Wenn Sie beispielsweise eine Zeichenfolge in Unicode konvertieren müssen und Unicode nicht unterstützen, legen Sie das **Value-Element** auf MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="db89f-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="db89f-155">Wenn die Eigenschaft zu groß ist, legen Sie sie auf MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="db89f-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="db89f-156">Wenn das Objekt die Eigenschaft nicht unterstützt, legen Sie sie auf MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="db89f-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="db89f-157">Die Implementierung der **GetProps-Methode** durch einen Remotetransportanbieter muss die Eigenschaftswerte des Ordners für vom Aufrufer angeforderte Eigenschaften zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="db89f-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="db89f-158">Ihre Implementierung muss die folgenden Schritte unternehmen:</span><span class="sxs-lookup"><span data-stu-id="db89f-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="db89f-159">Weisen Sie ein Eigenschaftenwertarray zu, um an den Aufrufer zurückzukehren und dessen Adresse im Eigenschaftswertzeigerparameter zu speichern, der zu diesem Zweck übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="db89f-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="db89f-160">Kopieren Sie die Eigenschaftstags aus den Eigenschaften des Ordners in die Eigenschaftstags im Eigenschaftswertarray entsprechend dem Array der Eigenschaftstags, die an **GetProps übergeben werden.**</span><span class="sxs-lookup"><span data-stu-id="db89f-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="db89f-161">Stellen Sie sicher, dass der Eigenschaftentyp für alle Eigenschaftstags festgelegt ist, die an **GetProps übergeben werden.**</span><span class="sxs-lookup"><span data-stu-id="db89f-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="db89f-162">Der Aufrufer kann einen Eigenschaftentyp von PT_UNSPECIFIED übergeben, in diesem Fall **muss GetProps** den richtigen Eigenschaftentyp für dieses Eigenschaftstag festlegen.</span><span class="sxs-lookup"><span data-stu-id="db89f-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="db89f-163">Legen Sie den Wert der einzelnen Eigenschaften im Eigenschaftswertarray entsprechend ihrem Tag.</span><span class="sxs-lookup"><span data-stu-id="db89f-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="db89f-164">Wenn das vom Aufrufer angeforderte Eigenschaftstag beispielsweise PR_OBJECT_TYPE **(** [PidTagObjectType](pidtagobjecttype-canonical-property.md)) ist, kann **GetProps** den Wert auf MAPI_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="db89f-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="db89f-165">Wenn der Aufrufer eigenschaftstags übergibt, die ihre Implementierung nicht verarbeiten kann, können Sie das Eigenschaftstag auf PT_ERROR für diese Eigenschaften festlegen und den Eigenschaftswert auf MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="db89f-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="db89f-166">Geben S_OK zurück, wenn keine Fehler aufgetreten sind, oder MAPI_W_ERRORS_RETURNED, wenn Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="db89f-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="db89f-167">Die Implementierung der **GetProps-Methode** eines Remotetransportanbieters muss mindestens die folgenden Eigenschaften unterstützen:</span><span class="sxs-lookup"><span data-stu-id="db89f-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="db89f-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="db89f-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="db89f-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="db89f-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="db89f-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="db89f-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="db89f-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="db89f-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="db89f-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="db89f-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="db89f-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="db89f-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="db89f-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="db89f-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="db89f-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="db89f-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="db89f-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="db89f-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="db89f-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="db89f-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="db89f-178">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="db89f-178">Notes to callers</span></span>

<span data-ttu-id="db89f-179">Rufen Sie für Eigenschaften vom Typ PT_OBJECT [die IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) anstelle von **GetProps auf.**</span><span class="sxs-lookup"><span data-stu-id="db89f-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="db89f-180">Für sichere Eigenschaften sollten Sie sie nicht abrufen, indem Sie **GetProps** aufrufen, wenn der  _lppPropTagArray-Parameter_ auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="db89f-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="db89f-181">Sie müssen den Bezeichner einer sicheren Eigenschaft explizit im **aulPropTag-Element** des Eigenschaftentagarrays festlegen, wenn Sie **GetProps aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="db89f-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="db89f-182">Wann und wie eine sichere Eigenschaft verfügbar ist, liegt beim Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="db89f-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="db89f-183">Geben Sie die **zurückgegebene SPropValue-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) nur aufrufen, wenn **GetProps** S_OK oder MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="db89f-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="db89f-184">Wenn **GetProps** MAPI_W_ERRORS_RETURNED, da er nicht auf eine oder mehrere Eigenschaften zugreifen konnte, überprüfen Sie die Eigenschaftstags der zurückgegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="db89f-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="db89f-185">Für die fehlgeschlagenen Eigenschaften werden die folgenden Werte in ihrer Eigenschaftswertstruktur festgelegt:</span><span class="sxs-lookup"><span data-stu-id="db89f-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="db89f-186">Der Eigenschaftstyp im **Element aulPropTag,** das auf PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="db89f-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="db89f-187">Der Eigenschaftswert im **Value-Element** wird auf einen Statuscode für den Fehler festgelegt, z. B. MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="db89f-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="db89f-188">Eigenschaften, die fehlschlagen, weil sie zu groß sind, um bequem in der Eigenschaftswertstruktur zurückgegeben zu werden, haben ihren **Value-Member** auf MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="db89f-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="db89f-189">In der Regel tritt dies bei Zeichenfolgen- oder binären Eigenschaften des Typs PT_STRING8, PT_UNICODE oder PT_BINARY auf, wenn der Wert der Eigenschaft 4 KB oder größer ist.</span><span class="sxs-lookup"><span data-stu-id="db89f-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="db89f-190">Rufen **Sie IMAPIProp::OpenProperty auf,** um große Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="db89f-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="db89f-191">Nicht alle Implementierungen von **GetProps** unterstützen sowohl die Unicode- als auch die ANSI-Formate für Zeichenzeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="db89f-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="db89f-192">Wenn eine bestimmte Eigenschaft eine Zeichenfolgenformatkonvertierung erfordert und **GetProps** sie nicht unterstützt, wird das **Value-Element** für die Eigenschaft auf MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="db89f-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="db89f-193">Um zu überprüfen, ob es sich bei einer PST SharePoint pst handelt, stellen Sie die PST mithilfe von [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)ein, und rufen Sie **dann GetProps** für das Nachrichtenspeicherobjekt auf, das diese Eigenschaft anfordert.</span><span class="sxs-lookup"><span data-stu-id="db89f-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="db89f-194">Wenn sie vorhanden ist, können Sie davon ausgehen, dass die #A0 für die SharePoint. Andern falls nicht, wurde das PST nicht als SharePoint konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="db89f-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="db89f-195">Weitere Informationen zur Verwendung von **GetProps** für den Zugriff auf Eigenschaften finden Sie unter [Abrufen von MAPI-Eigenschaften](retrieving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="db89f-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="db89f-196">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="db89f-196">MFCMAPI reference</span></span>

<span data-ttu-id="db89f-197">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="db89f-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="db89f-198">**Datei**</span><span class="sxs-lookup"><span data-stu-id="db89f-198">**File**</span></span>|<span data-ttu-id="db89f-199">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="db89f-199">**Function**</span></span>|<span data-ttu-id="db89f-200">**Comment**</span><span class="sxs-lookup"><span data-stu-id="db89f-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="db89f-201">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="db89f-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="db89f-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="db89f-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="db89f-203">MFCMAPI verwendet die **IMAPIProp::GetProps-Methode,** um alle Eigenschaften für ein Objekt zu erhalten, indem null oder das array übergeben wird, das von der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) im  _lpPropTagArray-Parameter_ zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="db89f-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db89f-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db89f-204">See also</span></span>



[<span data-ttu-id="db89f-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="db89f-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="db89f-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="db89f-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="db89f-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="db89f-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="db89f-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="db89f-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="db89f-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="db89f-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="db89f-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="db89f-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="db89f-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="db89f-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="db89f-212">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="db89f-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="db89f-213">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="db89f-213">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="db89f-214">Abrufen von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="db89f-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="db89f-215">Verwenden von Makros für die Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="db89f-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

