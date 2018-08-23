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
ms.openlocfilehash: 462d42d68bddba72fd81b97e2aeb9eb5ee8c9c20
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588006"
---
# <a name="imapipropgetprops"></a><span data-ttu-id="c557d-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c557d-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="c557d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c557d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c557d-105">Ruft den Wert der Eigenschaft um, der eine oder mehrere Eigenschaften eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="c557d-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="c557d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c557d-106">Parameters</span></span>

 <span data-ttu-id="c557d-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="c557d-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="c557d-108">[in] Ein Zeiger auf ein Array von Eigenschaftentags, mit denen die Eigenschaften, deren Werte abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c557d-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="c557d-109">Der Parameter _LpPropTagArray_ muss entweder NULL-Wert zurück, der angibt, dass Werte für alle Eigenschaften des Objekts zurückgegeben werden soll, oder zeigen Sie auf eine [SPropTagArray](sproptagarray.md) -Struktur, die einen oder mehrere Eigenschaftentags enthält.</span><span class="sxs-lookup"><span data-stu-id="c557d-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="c557d-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c557d-110">_ulFlags_</span></span>
  
> <span data-ttu-id="c557d-111">[in] Eine Bitmaske aus Flags, die das Format für Eigenschaften angibt, die den Typ PT_UNSPECIFIED aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c557d-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="c557d-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c557d-112">The following flag can be set:</span></span>
    
<span data-ttu-id="c557d-113">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c557d-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c557d-114">Die Zeichenfolgenwerte für diese Eigenschaften sollte das Unicode-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c557d-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="c557d-115">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgenwerte im ANSI-Format zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c557d-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="c557d-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="c557d-116">_lpcValues_</span></span>
  
> <span data-ttu-id="c557d-117">[out] Ein Zeiger auf eine Anzahl von Eigenschaftswerten auf den durch den Parameter _LppPropArray_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="c557d-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="c557d-118">Wenn _LppPropArray_ NULL ist, wird der Inhalt des Parameters _LpcValues_ 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c557d-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="c557d-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="c557d-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="c557d-120">[out] Ein Zeiger auf einen Zeiger auf die abgerufenen Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="c557d-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c557d-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c557d-121">Return value</span></span>

<span data-ttu-id="c557d-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="c557d-122">S_OK</span></span> 
  
> <span data-ttu-id="c557d-123">Die Eigenschaftswerte wurden erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c557d-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="c557d-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="c557d-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="c557d-125">Der Aufruf war insgesamt erfolgreich, aber eine oder mehrere Eigenschaften konnte nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="c557d-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="c557d-126">**AulPropTag** Mitglied der Eigenschaftswert für jeden nicht verfügbar-Eigenschaft hat einen Eigenschaftentyp PT_ERROR und eine Kennung von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c557d-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="c557d-127">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c557d-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c557d-128">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="c557d-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c557d-129">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="c557d-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="c557d-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c557d-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="c557d-131">0 (null) wurde im **cValues** -Member der **SPropTagArray** -Struktur, die auf den _LpPropTagArray_übergeben.</span><span class="sxs-lookup"><span data-stu-id="c557d-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c557d-132">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c557d-132">Remarks</span></span>

<span data-ttu-id="c557d-133">Die **IMAPIProp::GetProps** -Methode ruft die Eigenschaftswerte der eine oder mehrere Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="c557d-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="c557d-134">Die Eigenschaftswerte werden in der gleichen Reihenfolge zurückgegeben, wie angefordert wurden (d. h., die Reihenfolge der Eigenschaften im Array Tag-Eigenschaft auf den _LpPropTagArray_ entspricht der Reihenfolge, in dem Array der Eigenschaft Wert Strukturen auf den _LppPropArray _).</span><span class="sxs-lookup"><span data-stu-id="c557d-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="c557d-135">Die in der **AulPropTag** Elemente von Arrays der Tag-Eigenschaft angegebene Eigenschaftentypen angeben des Typs des Werts, der in der Member **Wert** jeder Eigenschaft-Wert-Struktur zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c557d-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="c557d-136">Wenn der Anrufer nicht den Typ einer Eigenschaft bekannt ist, kann jedoch der Typ im **AulPropTag** -Member stattdessen auf PT_UNSPECIFIED festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c557d-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="c557d-137">In das Abrufen des Werts, legt **GetProps** den korrekten Typ in der **AulPropTag** Member der Eigenschaft Wert Struktur für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c557d-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="c557d-138">Eigenschaftentypen in der **SPropTagArray** in _LpPropTagArray_angegeben, haben der Eigenschaftswerte in den **SPropValue** im _LppPropArray_ zurückgegebenen Typen, die die angeforderten Typen exakt übereinstimmen, sofern Sie kein Fehlerwert zurückgegeben wird Stattdessen.</span><span class="sxs-lookup"><span data-stu-id="c557d-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="c557d-139">Zeichenfolgeneigenschaften können einen der beiden Typen aufweisen: PT_UNICODE PT_STRING8 zur Darstellung von ANSI-Format und die Unicode-Format dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c557d-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="c557d-140">Wenn die Option MAPI_UNICODE im Parameter _UlFlags_ festgelegt ist, wenn nicht das entsprechende Format für eine Zeichenfolgeneigenschaft **GetProps** bestimmen kann, wird den Wert in das Unicode-Format zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c557d-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="c557d-141">Eine exakte Zeichenfolge Eigenschaftentyp in den folgenden Situationen kann nicht **GetProps** ermitteln:</span><span class="sxs-lookup"><span data-stu-id="c557d-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="c557d-142">Der Parameter _LpPropTagArray_ ist auf NULL festgelegt, so fordern Sie alle Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="c557d-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="c557d-143">Das **AulPropTag** -Element enthält den Wert PT_UNSPECIFIED als Eigenschaftentyp in Array der Tag-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c557d-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="c557d-144">Wenn der _LpPropTagArray_ -Parameter auf NULL festgelegt ist, um alle Eigenschaften des Objekts abzurufen und keine Eigenschaften vorhanden, führt **GetProps** Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="c557d-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="c557d-145">Gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="c557d-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="c557d-146">Der Count-Wert festgelegt im **cValues** -Member der Eigenschaft Wert Struktur auf 0.</span><span class="sxs-lookup"><span data-stu-id="c557d-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="c557d-147">Der Inhalt des _LpcValues_ festgelegt auf 0.</span><span class="sxs-lookup"><span data-stu-id="c557d-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="c557d-148">_LppPropArray_ festgelegt auf NULL.</span><span class="sxs-lookup"><span data-stu-id="c557d-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="c557d-149">**GetProps** müssen keine zurück, dass Eigenschaften mit mehreren Werten mit **cValues** auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c557d-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c557d-150">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c557d-150">Notes to implementers</span></span>

<span data-ttu-id="c557d-151">Rufen Sie die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, um Speicher ursprünglich für die [SPropValue](spropvalue.md) -Struktur, die auf den _LpPropTagArray_; Rufen Sie [MAPIAllocateMore](mapiallocatemore.md) zum Reservieren alle zusätzlichen Speichers für die Struktur Elemente erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c557d-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="c557d-152">Zurückgeben Sie MAPI_W_ERRORS_RETURNED, wenn Sie den Wert für eine oder mehrere der angeforderten Eigenschaften abrufen können.</span><span class="sxs-lookup"><span data-stu-id="c557d-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="c557d-153">Legen Sie den Typ der Eigenschaft Wert Struktur in der Member **AulPropTag** PT_ERROR und der **Wert** Member einen Statuscode, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c557d-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="c557d-154">Beispielsweise wenn Sie eine Zeichenfolge in Unicode konvertieren und Unicode nicht unterstützt, legen Sie den **Wert** Member auf MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="c557d-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="c557d-155">Wenn die Eigenschaft zu groß ist, legen Sie es auf MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="c557d-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="c557d-156">Wenn das Objekt die-Eigenschaft nicht unterstützt, festlegen Sie jedoch auf MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="c557d-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="c557d-157">Implementierung der **GetProps** -Methode eines remote-Transport-Anbieters muss den Ordner Eigenschaftswerte für Eigenschaften, die vom Anrufer angefordert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c557d-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="c557d-158">Die Implementierung muss die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c557d-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="c557d-159">Reservieren Sie eine Eigenschaft Wertearray, um an den Anrufer zurückgeben, und speichern Sie die Adresse in der Eigenschaft Value Zeiger-Parameter für diesen Zweck bestimmten übergeben.</span><span class="sxs-lookup"><span data-stu-id="c557d-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="c557d-160">Kopieren Sie die Eigenschaftentags aus den Eigenschaften des Ordners, in die Eigenschaftentags im Array Eigenschaft Wert gemäß dem Array der Eigenschaftentags **GetProps**übergeben.</span><span class="sxs-lookup"><span data-stu-id="c557d-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="c557d-161">Stellen Sie sicher, dass für alle Eigenschaftentags **GetProps**übergeben der Eigenschaftentyp festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c557d-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="c557d-162">Der Eigenschaftentyp PT_UNSPECIFIED, kann der Aufrufer übergeben in dem Fall **GetProps** den richtigen Eigenschaftstyp für diese Eigenschaftentag festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c557d-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="c557d-163">Legen Sie den Wert jeder Eigenschaft im Array Eigenschaft Wert entsprechend der Tag.</span><span class="sxs-lookup"><span data-stu-id="c557d-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="c557d-164">Angenommen, wenn das durch den Aufrufer angeforderte Eigenschafts-Tag **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) ist, können **GetProps** den Wert auf MAPI_FOLDER festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c557d-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="c557d-165">Wenn der Aufrufer eine beliebige Eigenschaftentags, die die Implementierung nicht behandelt wird übergibt, können Sie das Eigenschafts-Tag auf PT_ERROR für diese Eigenschaften festgelegt und den Wert der Eigenschaft auf MAPI_E_NOT_FOUND festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c557d-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="c557d-166">Geben Sie S_OK zurück, wenn keine Fehler aufgetreten sind oder MAPI_W_ERRORS_RETURNED zurück, wenn Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c557d-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="c557d-167">Implementierung eines remote-Transport-Anbieters der **GetProps** -Methode muss mindestens die folgenden Eigenschaften unterstützen:</span><span class="sxs-lookup"><span data-stu-id="c557d-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="c557d-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c557d-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="c557d-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c557d-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="c557d-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c557d-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="c557d-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c557d-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="c557d-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c557d-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="c557d-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c557d-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="c557d-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c557d-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="c557d-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c557d-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="c557d-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="c557d-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="c557d-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c557d-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="c557d-178">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c557d-178">Notes to callers</span></span>

<span data-ttu-id="c557d-179">Rufen Sie für Eigenschaften vom Typ PT_OBJECT die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode statt **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="c557d-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="c557d-180">Für sichere Eigenschaften davon ausgehen, dass sie abrufen durch Aufrufen von **GetProps** mit der _LppPropTagArray_ -Parameter auf NULL festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c557d-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="c557d-181">Sie müssen beim Aufruf **GetProps**explizit eine sichere Eigenschaftenbezeichner im **AulPropTag** Mitglied des Arrays die Tag-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="c557d-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="c557d-182">Wann und wie eine sichere Eigenschaft verfügbar ist, wird bis zum Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c557d-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="c557d-183">Frei die zurückgegebene Struktur **SPropValue** durch Aufrufen der Funktion [MAPIFreeBuffer](mapifreebuffer.md) nur, wenn **GetProps** S_OK oder MAPI_W_ERRORS_RETURNED zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c557d-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="c557d-184">Wenn **GetProps** MAPI_W_ERRORS_RETURNED zurückgibt, da eine oder mehrere Eigenschaften nicht zugegriffen werden konnte, überprüfen Sie die Eigenschaftentags der zurückgegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c557d-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="c557d-185">Fehlgeschlagenen Eigenschaften müssen die folgenden Werte in die Struktur der Eigenschaft Wert festlegen:</span><span class="sxs-lookup"><span data-stu-id="c557d-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="c557d-186">Der Eigenschaftentyp im **AulPropTag** -Member auf PT_ERROR festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c557d-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="c557d-187">Der Wert der Eigenschaft im Member **Wert** auf einen Statuscode des Fehlers, wie etwa MAPI_E_NOT_FOUND festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c557d-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="c557d-188">Eigenschaften, die nicht, da sie bequem in der Eigenschaft Wert Struktur zurückgegeben werden zu groß sind haben **ihre Element auf MAPI_E_NOT_ENOUGH_MEMORY festgelegt** .</span><span class="sxs-lookup"><span data-stu-id="c557d-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="c557d-189">In der Regel Dies tritt auf, mit Zeichenfolgen oder binäre Eigenschaften vom Typ PT_STRING8, PT_UNICODE oder PT_BINARY Wenn der Wert der Eigenschaft 4 KB oder größer.</span><span class="sxs-lookup"><span data-stu-id="c557d-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="c557d-190">Rufen Sie **IMAPIProp::OpenProperty** um große Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c557d-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="c557d-191">Nicht alle Implementierungen von **GetProps** unterstützen die Unicode- und die ANSI-Formate für Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="c557d-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="c557d-192">Wenn eine bestimmte Eigenschaft eine Zeichenfolge formatkonvertierung erforderlich und **GetProps** nicht wird unterstützt kann, wird der **Wert** Member für die Eigenschaft auf MAPI_E_BAD_CHARWIDTH festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c557d-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="c557d-193">Um zu überprüfen, ob eine PST-Datei auf einer SharePoint-PST-Datei ist, binden Sie die PST-Datei **GetProps** verwenden und [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), klicken Sie dann auf diese Eigenschaft anfordern Message Store-Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c557d-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="c557d-194">Wenn es vorhanden ist, können Sie davon ausgehen, dass die PST-Datei für SharePoint konfiguriert wurde; Wenn dies nicht der Fall ist, wird die PST-Datei als eine SharePoint-PST-Datei wurde nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c557d-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="c557d-195">Weitere Informationen zur Verwendung von **GetProps** für den Zugriff auf Eigenschaften, finden Sie unter [Abrufen von MAPI-Eigenschaften](retrieving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c557d-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c557d-196">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="c557d-196">MFCMAPI reference</span></span>

<span data-ttu-id="c557d-197">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c557d-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c557d-198">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c557d-198">**File**</span></span>|<span data-ttu-id="c557d-199">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c557d-199">**Function**</span></span>|<span data-ttu-id="c557d-200">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c557d-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c557d-201">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="c557d-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c557d-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="c557d-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="c557d-203">MFCMAPI (engl.) verwendet die **IMAPIProp::GetProps** -Methode, um alle Eigenschaften für ein Objekt abrufen, indem Sie entweder NULL oder von der [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode im Parameter _LpPropTagArray_ zurückgegebenen Array übergeben.</span><span class="sxs-lookup"><span data-stu-id="c557d-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c557d-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c557d-204">See also</span></span>



[<span data-ttu-id="c557d-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="c557d-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="c557d-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="c557d-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="c557d-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c557d-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="c557d-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="c557d-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="c557d-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c557d-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c557d-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c557d-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="c557d-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c557d-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="c557d-212">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c557d-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="c557d-213">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c557d-213">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c557d-214">Abrufen von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c557d-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="c557d-215">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="c557d-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

