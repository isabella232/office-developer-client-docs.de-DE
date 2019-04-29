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
# <a name="imapipropgetprops"></a><span data-ttu-id="232b3-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="232b3-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="232b3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="232b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="232b3-105">Ruft den Eigenschaftswert einer oder mehrerer Eigenschaften eines Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="232b3-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="232b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="232b3-106">Parameters</span></span>

 <span data-ttu-id="232b3-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="232b3-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="232b3-108">in Ein Zeiger auf ein Array von Property-Tags, die die Eigenschaften identifizieren, deren Werte abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="232b3-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="232b3-109">Der _lpPropTagArray_ -Parameter muss entweder NULL sein, wodurch angegeben wird, dass Werte für alle Eigenschaften des Objekts zurückgegeben werden sollen, oder auf eine [SPropTagArray](sproptagarray.md) -Struktur verweisen, die mindestens ein Property-Tag enthält.</span><span class="sxs-lookup"><span data-stu-id="232b3-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="232b3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="232b3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="232b3-111">in Eine Bitmaske von Flags, die das Format für Eigenschaften mit dem Typ PT_UNSPECIFIED angibt.</span><span class="sxs-lookup"><span data-stu-id="232b3-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="232b3-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="232b3-112">The following flag can be set:</span></span>
    
<span data-ttu-id="232b3-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="232b3-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="232b3-114">Die Zeichenfolgenwerte für diese Eigenschaften sollten im Unicode-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="232b3-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="232b3-115">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sollten die Zeichenfolgenwerte im ANSI-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="232b3-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="232b3-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="232b3-116">_lpcValues_</span></span>
  
> <span data-ttu-id="232b3-117">Out Ein Zeiger auf die Anzahl von Eigenschaftswerten, auf die durch den _lppPropArray_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="232b3-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="232b3-118">Wenn _lppPropArray_ ist, ist der Inhalt des _lpcValues_ -Parameters 0 (null).</span><span class="sxs-lookup"><span data-stu-id="232b3-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="232b3-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="232b3-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="232b3-120">Out Ein Zeiger auf einen Zeiger auf die abgerufenen Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="232b3-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="232b3-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="232b3-121">Return value</span></span>

<span data-ttu-id="232b3-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="232b3-122">S_OK</span></span> 
  
> <span data-ttu-id="232b3-123">Die Eigenschaftswerte wurden erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="232b3-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="232b3-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="232b3-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="232b3-125">Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="232b3-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="232b3-126">Der **aulPropTag** -Member des Eigenschaftswerts für jede nicht verfügbare Eigenschaft hat den Eigenschaftentyp PT_ERROR und den Bezeichner 0 (null).</span><span class="sxs-lookup"><span data-stu-id="232b3-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="232b3-127">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="232b3-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="232b3-128">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="232b3-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="232b3-129">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="232b3-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="232b3-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="232b3-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="232b3-131">0 (null) wurde im **cValues** -Element der **SPropTagArray** -Struktur übergeben, auf die durch _lpPropTagArray_verwiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="232b3-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="232b3-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="232b3-132">Remarks</span></span>

<span data-ttu-id="232b3-133">Die **IMAPIProp::** GetProps-Methode ruft die Eigenschaftswerte einer oder mehrerer Eigenschaften eines Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="232b3-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="232b3-134">Die Eigenschaftswerte werden in der Reihenfolge zurückgegeben, in der Sie angefordert wurden (die Reihenfolge der Eigenschaften im Eigenschaftentag-Array, auf die durch _lpPropTagArray_ verwiesen wird, entspricht der Reihenfolge im Array von Eigenschaftswert Strukturen, auf die durch _lppPropArray _).</span><span class="sxs-lookup"><span data-stu-id="232b3-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="232b3-135">Die in den **aulPropTag** -Elementen des Property-Tag-Arrays angegebenen Eigenschaftentypen geben den Typ des Werts an, der im **value** -Element jeder Eigenschaftswert Struktur zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="232b3-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="232b3-136">Wenn der Aufrufer den Typ einer Eigenschaft jedoch nicht kennt, kann der Typ im **aulPropTag** -Element stattdessen auf PT_UNSPECIFIED festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="232b3-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="232b3-137">Beim Abrufen des Werts legt getProps den richtigen Typ im **aulPropTag** -Element der Eigenschaftswert Struktur für die Eigenschaft fest. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="232b3-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="232b3-138">Wenn Eigenschaftstypen in der **SPropTagArray** in _lpPropTagArray_angegeben werden, haben die Eigenschaftswerte in der **SPropValue** , die in _lppPropArray_ zurückgegeben werden, Typen, die genau mit den angeforderten Typen übereinstimmen, es sei denn, ein Fehlerwert wird zurückgegeben statt.</span><span class="sxs-lookup"><span data-stu-id="232b3-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="232b3-139">Zeichenfolgeneigenschaften können einen von zwei Eigenschaftentypen aufweisen: PT_UNICODE zur Darstellung des Unicode-Formats und PT_STRING8 zur Darstellung des ANSI-Formats.</span><span class="sxs-lookup"><span data-stu-id="232b3-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="232b3-140">Wenn das MAPI_UNICODE-Flag im _ulFlags_ -Parameter festgelegt ist, wird der Wert im Unicode-Format zurückgegeben, wenn GetProps das entsprechende Format für eine String-Eigenschaft nicht ermitteln kann. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="232b3-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="232b3-141">\*\*\*\* GetProps kann in den folgenden Situationen keinen genauen String-Eigenschaftentyp bestimmen:</span><span class="sxs-lookup"><span data-stu-id="232b3-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="232b3-142">Der Parameter _lpPropTagArray_ wird auf NULL festgelegt, um alle Eigenschaften anzufordern.</span><span class="sxs-lookup"><span data-stu-id="232b3-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="232b3-143">Das **aulPropTag** -Element enthält den Wert PT_UNSPECIFIED als Eigenschafts im Property-Tag-Array.</span><span class="sxs-lookup"><span data-stu-id="232b3-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="232b3-144">Wenn der Parameter _lpPropTagArray_ auf NULL festgelegt ist, um alle Eigenschaften des Objekts abzurufen, und keine Eigenschaften vorhanden sind, führt GetProps folgende Aktionen aus: \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="232b3-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="232b3-145">Gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="232b3-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="232b3-146">Legt den count-Wert im **cValues** -Element der Eigenschaftswert Struktur auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="232b3-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="232b3-147">Legt den Inhalt von _lpcValues_ auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="232b3-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="232b3-148">Legt _lppPropArray_ auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="232b3-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="232b3-149">\*\*\*\* GetProps darf keine Eigenschaften mit mehreren Werten zurückgeben, wenn **cValues** auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="232b3-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="232b3-150">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="232b3-150">Notes to implementers</span></span>

<span data-ttu-id="232b3-151">Rufen Sie die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion auf, um zunächst Speicher für die [SPropValue](spropvalue.md) -Struktur zu reservieren, auf die von _lpPropTagArray_verwiesen wird; Rufen Sie [MAPIAllocateMore](mapiallocatemore.md) auf, um zusätzlichen Arbeitsspeicher für die Mitglieder der Struktur zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="232b3-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="232b3-152">Geben Sie MAPI_W_ERRORS_RETURNED zurück, wenn der Wert für eine oder mehrere der angeforderten Eigenschaften nicht abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="232b3-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="232b3-153">Legen Sie in der Eigenschaftswert Struktur den Typ im **aulPropTag** -Element auf PT_ERROR und den **Wert** Member auf einen Statuscode fest, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="232b3-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="232b3-154">Wenn Sie beispielsweise eine Zeichenfolge in Unicode konvertieren und Unicode nicht unterstützen, legen Sie den **Wert** Mitglied auf MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="232b3-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="232b3-155">Wenn die Eigenschaft zu hoch ist, legen Sie Sie auf MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="232b3-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="232b3-156">Wenn das Objekt die Eigenschaft nicht unterstützt, legen Sie es auf MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="232b3-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="232b3-157">Die Implementierung der getProps-Methode \*\*\*\* eines Remote Transportanbieters muss die Eigenschaftswerte des Ordners für vom Aufrufer angeforderte Eigenschaften zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="232b3-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="232b3-158">Die Implementierung muss folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="232b3-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="232b3-159">Weisen Sie ein Eigenschaftswert Array zu, um zum Aufrufer zurückzukehren, und speichern Sie dessen Adresse im für diesen Zweck übergebenen Parameter value Pointer.</span><span class="sxs-lookup"><span data-stu-id="232b3-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="232b3-160">Kopieren Sie die Eigenschaftstags aus den Eigenschaften des Ordners in die Eigenschaftstags im Eigenschafts Wertarray entsprechend dem Array von Property- \*\*\*\* Tags, die an GetProps übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="232b3-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="232b3-161">Stellen Sie sicher, dass der Eigenschaftentyp für alle an getProps übergebenen Eigenschaftstags festgelegt ist. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="232b3-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="232b3-162">Der Aufrufer kann einen Eigenschaftentyp von PT_UNSPECIFIED übergeben, in dem Fall, \*\*\*\* dass GetProps den richtigen Eigenschaftentyp für das Eigenschaftentag festlegen muss.</span><span class="sxs-lookup"><span data-stu-id="232b3-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="232b3-163">Legen Sie den Wert jeder Eigenschaft im Eigenschaftswert Array entsprechend dem-Tag fest.</span><span class="sxs-lookup"><span data-stu-id="232b3-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="232b3-164">Wenn beispielsweise das vom Aufrufer angeforderte Property-Tag **PR_OBJECT_TYPE** ([pidtagobjecttype (](pidtagobjecttype-canonical-property.md)) ist, kann \*\*\*\* GetProps den Wert auf MAPI_FOLDER festlegen.</span><span class="sxs-lookup"><span data-stu-id="232b3-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="232b3-165">Wenn der Aufrufer alle Eigenschaftentags übergibt, die von der Implementierung nicht behandelt werden, können Sie das Property-Tag für diese Eigenschaften auf PT_ERROR festlegen und den Eigenschaftswert auf MAPI_E_NOT_FOUND festlegen.</span><span class="sxs-lookup"><span data-stu-id="232b3-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="232b3-166">Gibt S_OK zurück, wenn keine Fehler aufgetreten sind, oder MAPI_W_ERRORS_RETURNED, wenn Fehler auftraten.</span><span class="sxs-lookup"><span data-stu-id="232b3-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="232b3-167">Die Implementierung der getProps-Methode \*\*\*\* eines Remote Transportanbieters muss mindestens die folgenden Eigenschaften unterstützen:</span><span class="sxs-lookup"><span data-stu-id="232b3-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="232b3-168">**PR_ACCESS** ([Pidtagaccess (](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="232b3-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="232b3-169">**PR_ACCESS_LEVEL** ([Pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="232b3-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="232b3-170">**PR_ASSOC_CONTENT_COUNT** ([Pidtagassociatedcontentcount (](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="232b3-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="232b3-171">**PR_CONTENT_COUNT** ([Pidtagcontentcount (](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="232b3-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="232b3-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="232b3-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="232b3-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="232b3-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="232b3-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="232b3-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="232b3-175">**PR_FOLDER_TYPE** ([Pidtagfoldertype (](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="232b3-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="232b3-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="232b3-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="232b3-177">**PR_SUBFOLDERS** ([Pidtagsubfolders (](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="232b3-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="232b3-178">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="232b3-178">Notes to callers</span></span>

<span data-ttu-id="232b3-179">Rufen Sie bei Eigenschaften vom Typ PT_OBJECT die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode anstelle \*\*\*\* von GetProps auf.</span><span class="sxs-lookup"><span data-stu-id="232b3-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="232b3-180">Für sichere Eigenschaften erwarten Sie Sie nicht, indem Sie getProps mit dem _lppPropTagArray_ -Parameter aufrufen, der auf NULL festgelegt ist. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="232b3-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="232b3-181">Sie müssen den Bezeichner einer sicheren Eigenschaft im **aulPropTag** -Element des Property-Tag-Arrays explizit festlegen, wenn \*\*\*\* Sie GetProps aufrufen.</span><span class="sxs-lookup"><span data-stu-id="232b3-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="232b3-182">Wann und wie eine sichere Eigenschaft verfügbar ist, liegt beim Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="232b3-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="232b3-183">Freigeben der zurückgegebenen **SPropValue** -Struktur durch Aufrufen der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion nur, wenn GetProps S_OK oder MAPI_W_ERRORS_RETURNED zurückgibt. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="232b3-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="232b3-184">Wenn \*\*\*\* GetProps MAPI_W_ERRORS_RETURNED zurückgibt, da der Zugriff auf eine oder mehrere Eigenschaften nicht möglich ist, überprüfen Sie die Eigenschaftentags der zurückgegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="232b3-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="232b3-185">Für die Eigenschaften des Fehlers werden die folgenden Werte in der Eigenschaftswert Struktur festgelegt:</span><span class="sxs-lookup"><span data-stu-id="232b3-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="232b3-186">Der Eigenschaftentyp im **aulPropTag** -Element, der auf PT_ERROR festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="232b3-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="232b3-187">Der Eigenschaftswert im **Wert** Element, der auf einen Statuscode für den Fehler festgelegt ist, beispielsweise MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="232b3-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="232b3-188">Eigenschaften, die fehlschlagen, da Sie zu umfangreich sind, um in der Eigenschaftswert \*\*\*\* Struktur bequem zurückgegeben werden zu können, sind auf MAPI_E_NOT_ENOUGH_MEMORY festgelegt.</span><span class="sxs-lookup"><span data-stu-id="232b3-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="232b3-189">Dies geschieht NormalerWeise mit String-oder Binary-Eigenschaften vom Typ PT_STRING8, PT_UNICODE oder PT_BINARY, wenn der Wert der Eigenschaft 4 KB oder größer ist.</span><span class="sxs-lookup"><span data-stu-id="232b3-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="232b3-190">Rufen Sie **IMAPIProp:: OpenProperty** auf, um umfangreiche Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="232b3-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="232b3-191">Nicht alle Implementierungen \*\*\*\* von GetProps unterstützen sowohl die Unicode-als auch die ANSI-Formate für Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="232b3-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="232b3-192">Wenn eine bestimmte Eigenschaft Zeichenfolgenformat Konvertierung erfordert \*\*\*\* und von GetProps nicht unterstützt werden kann, wird der **Wert** für die Eigenschaft auf MAPI_E_BAD_CHARWIDTH festgelegt.</span><span class="sxs-lookup"><span data-stu-id="232b3-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="232b3-193">Um zu überprüfen, ob eine PST-Datei eine SharePoint-PST ist, montieren Sie die PST \*\*\*\* -Datei mithilfe von [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md), und rufen Sie dann GetProps für das Nachrichtenspeicherobjekt auf, das diese Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="232b3-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="232b3-194">Wenn dies der Fall ist, können Sie davon ausgehen, dass die PST-Datei für SharePoint konfiguriert wurde. Wenn dies nicht der Fall ist, wurde die PST-Datei nicht als SharePoint-PST-Datei konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="232b3-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="232b3-195">Weitere Informationen zur Verwendung von getProps für den Zugriff auf Eigenschaften finden Sie unter [Abrufen von MAPI-Eigenschaften](retrieving-mapi-properties.md). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="232b3-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="232b3-196">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="232b3-196">MFCMAPI reference</span></span>

<span data-ttu-id="232b3-197">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="232b3-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="232b3-198">**Datei**</span><span class="sxs-lookup"><span data-stu-id="232b3-198">**File**</span></span>|<span data-ttu-id="232b3-199">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="232b3-199">**Function**</span></span>|<span data-ttu-id="232b3-200">**Comment**</span><span class="sxs-lookup"><span data-stu-id="232b3-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="232b3-201">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="232b3-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="232b3-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="232b3-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="232b3-203">MFCMAPI verwendet die **IMAPIProp::** GetProps-Methode, um alle Eigenschaften eines Objekts abzurufen, indem entweder NULL oder das von der [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode zurückgegebene Array im _lpPropTagArray_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="232b3-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="232b3-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="232b3-204">See also</span></span>



[<span data-ttu-id="232b3-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="232b3-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="232b3-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="232b3-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="232b3-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="232b3-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="232b3-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="232b3-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="232b3-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="232b3-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="232b3-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="232b3-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="232b3-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="232b3-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="232b3-212">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="232b3-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="232b3-213">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="232b3-213">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="232b3-214">Abrufen von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="232b3-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="232b3-215">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="232b3-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

