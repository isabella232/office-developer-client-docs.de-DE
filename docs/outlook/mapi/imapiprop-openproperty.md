---
title: IMAPIPropOpenProperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319810"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="379d9-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="379d9-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="379d9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="379d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="379d9-105">Gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf eine Eigenschaft verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="379d9-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="379d9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="379d9-106">Parameters</span></span>

 <span data-ttu-id="379d9-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="379d9-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="379d9-108">[in] Das Eigenschaftstag für die Eigenschaft, auf die zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="379d9-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="379d9-109">Sowohl der Bezeichner als auch der Typ müssen im Eigenschaftstag enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="379d9-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="379d9-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="379d9-110">_lpiid_</span></span>
  
> <span data-ttu-id="379d9-111">[in] Ein Zeiger auf den Bezeichner für die Schnittstelle, die für den Zugriff auf die Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="379d9-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="379d9-112">Der _lpiid-Parameter_ darf nicht null **sein.**</span><span class="sxs-lookup"><span data-stu-id="379d9-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="379d9-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="379d9-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="379d9-114">[in] Daten, die sich auf die durch den  _lpiid-Parameter identifizierte Schnittstelle_ beziehen.</span><span class="sxs-lookup"><span data-stu-id="379d9-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="379d9-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="379d9-115">_ulFlags_</span></span>
  
> <span data-ttu-id="379d9-116">[in] Eine Bitmaske mit Flags, die den Zugriff auf die Eigenschaft steuert.</span><span class="sxs-lookup"><span data-stu-id="379d9-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="379d9-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="379d9-117">The following flags can be set:</span></span>
    
<span data-ttu-id="379d9-118">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="379d9-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="379d9-119">Wenn die Eigenschaft nicht vorhanden ist, sollte sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="379d9-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="379d9-120">Wenn die Eigenschaft vorhanden ist, sollte der aktuelle Wert der Eigenschaft verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="379d9-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="379d9-121">Wenn ein Anrufer das MAPI_CREATE legt, sollte es auch das MAPI_MODIFY festlegen.</span><span class="sxs-lookup"><span data-stu-id="379d9-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="379d9-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="379d9-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="379d9-123">Ermöglicht die erfolgreiche Rückgabe von **OpenProperty,** möglicherweise bevor das Objekt vollständig für den Aufrufer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="379d9-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="379d9-124">Wenn das Objekt nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="379d9-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="379d9-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="379d9-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="379d9-126">MAPI_MODIFY ist in folgenden Situationen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="379d9-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="379d9-127">Beim Öffnen einer Streameigenschaft, **z. B. IID_IStream**, um sie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="379d9-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="379d9-128">Wenn Sie eine eingebettete Nachrichtenanlage öffnen, z. [B.](pidtagattachdataobject-canonical-property.md) PR_ATTACH_DATA_OBJ mit IID_IMessage **,** um sie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="379d9-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="379d9-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="379d9-129">_lppUnk_</span></span>
  
> <span data-ttu-id="379d9-130">[out] Ein Zeiger auf die angeforderte Schnittstelle, die für den Eigenschaftszugriff verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="379d9-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="379d9-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="379d9-131">Return value</span></span>

<span data-ttu-id="379d9-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="379d9-132">S_OK</span></span> 
  
> <span data-ttu-id="379d9-133">Der angeforderte Schnittstellenzeiger wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="379d9-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="379d9-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="379d9-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="379d9-135">Die angeforderte Schnittstelle wird für diese Eigenschaft nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="379d9-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="379d9-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="379d9-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="379d9-137">Der Aufrufer verfügt über unzureichende Berechtigungen für den Zugriff auf die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="379d9-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="379d9-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="379d9-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="379d9-139">Das Objekt kann keinen Zugriff auf diese Eigenschaft über die angeforderte Schnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="379d9-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="379d9-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="379d9-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="379d9-141">Die angeforderte Eigenschaft ist nicht vorhanden, und MAPI_CREATE wurde nicht im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="379d9-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="379d9-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="379d9-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="379d9-143">Der Eigenschaftentyp im Tag ist auf PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="379d9-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="379d9-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="379d9-144">Remarks</span></span>

<span data-ttu-id="379d9-145">Die **IMAPIProp::OpenProperty-Methode** ermöglicht den Zugriff auf eine Eigenschaft über eine bestimmte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="379d9-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="379d9-146">**OpenProperty** ist eine Alternative zu den [Methoden IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="379d9-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="379d9-147">Wenn bei **GetProps oder** **SetProps** ein Fehler auftritt, da die Eigenschaft zu groß oder zu komplex ist, rufen Sie **OpenProperty auf.**</span><span class="sxs-lookup"><span data-stu-id="379d9-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="379d9-148">**OpenProperty** wird in der Regel verwendet, um auf Eigenschaften vom Typ PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="379d9-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="379d9-149">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="379d9-149">Notes to callers</span></span>

<span data-ttu-id="379d9-150">Öffnen Sie zum Zugreifen auf **Nachrichtenanlagen die PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) -Eigenschaft mit einem anderen Schnittstellenbezeichner, je nach Anlagetyp.</span><span class="sxs-lookup"><span data-stu-id="379d9-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="379d9-151">In der folgenden Tabelle wird das Aufrufen **von OpenProperty für** die verschiedenen Anlagentypen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="379d9-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="379d9-152">**Anlagetyp**</span><span class="sxs-lookup"><span data-stu-id="379d9-152">**Type of attachment**</span></span>|<span data-ttu-id="379d9-153">**Zu verwendende Schnittstellen-ID**</span><span class="sxs-lookup"><span data-stu-id="379d9-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="379d9-154">Binär</span><span class="sxs-lookup"><span data-stu-id="379d9-154">Binary</span></span>  <br/> |<span data-ttu-id="379d9-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="379d9-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="379d9-156">String</span><span class="sxs-lookup"><span data-stu-id="379d9-156">String</span></span>  <br/> |<span data-ttu-id="379d9-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="379d9-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="379d9-158">Message</span><span class="sxs-lookup"><span data-stu-id="379d9-158">Message</span></span>  <br/> |<span data-ttu-id="379d9-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="379d9-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="379d9-160">OLE 2.0</span><span class="sxs-lookup"><span data-stu-id="379d9-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="379d9-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="379d9-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="379d9-162">**IStreamDocfile** ist eine Ableitung der [IStream-Schnittstelle,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) die auf einer OLE 2.0-Verbunddatei basiert.</span><span class="sxs-lookup"><span data-stu-id="379d9-162">**IStreamDocfile** is a derivative of the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="379d9-163">**IStreamDocfile** ist die beste Wahl für den Zugriff auf OLE 2.0-Anlagen, da dies den geringsten Aufwand mit sich bringt.</span><span class="sxs-lookup"><span data-stu-id="379d9-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="379d9-164">Sie können IID_IStreamDocFile eigenschaften verwenden, die Daten enthalten, die im strukturierten Speicher gespeichert sind, die über die [IStorage-Schnittstelle verfügbar](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) sind.</span><span class="sxs-lookup"><span data-stu-id="379d9-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="379d9-165">Weitere Informationen zur Verwendung von **OpenProperty** mit Anlagen finden Sie unter **PR_ATTACH_DATA_OBJ-Eigenschaft** und [Öffnen einer Anlage](opening-an-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="379d9-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="379d9-166">Verwenden Sie nicht den **IStream-Zeiger,** den Sie erhalten, um die [Seek-](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) oder [SetSize-Methode](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) auf aufruft, es sei denn, Sie verwenden eine Nullposition oder Größenvariable.</span><span class="sxs-lookup"><span data-stu-id="379d9-166">Do not use the **IStream** pointer that you receive to call either its [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) or [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="379d9-167">Verlassen Sie sich außerdem nicht auf den Wert des  _plibNewPosition-Ausgabeparameters,_ der vom **Seek-Aufruf zurückgegeben** wird.</span><span class="sxs-lookup"><span data-stu-id="379d9-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="379d9-168">Wenn Sie **OpenProperty aufrufen,** um auf eine Eigenschaft mit der **IStream-Schnittstelle** zu zugreifen, verwenden Sie nur diese Schnittstelle, um Änderungen daran vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="379d9-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="379d9-169">Versuchen Sie nicht, die Eigenschaft mit einer der anderen [IMAPIProp : IUnknown-Methoden](imapipropiunknown.md) wie **SetProps** oder [IMAPIProp::D eleteProps](imapiprop-deleteprops.md)zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="379d9-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="379d9-170">Versuchen Sie nicht, eine Eigenschaft mit **OpenProperty mehr** als einmal zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="379d9-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="379d9-171">Die Ergebnisse sind nicht definiert, da sie von Anbieter zu Anbieter variieren können.</span><span class="sxs-lookup"><span data-stu-id="379d9-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="379d9-172">Wenn Sie die zu öffnende Eigenschaft ändern müssen, legen Sie das Flag MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="379d9-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="379d9-173">Wenn Sie nicht sicher sind, ob das Objekt die Eigenschaft unterstützt, aber sie sollte, legen Sie die MAPI_CREATE- und MAPI_MODIFY fest.</span><span class="sxs-lookup"><span data-stu-id="379d9-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="379d9-174">Wenn MAPI_CREATE festgelegt ist, muss MAPI_MODIFY festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="379d9-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="379d9-175">Sie sind für das Neucasting des im  _lppUnk-Parameter_ zurückgegebenen Schnittstellenzeigers auf einen für die im  _lpiid-Parameter_ angegebene Schnittstelle verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="379d9-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="379d9-176">Sie müssen auch den zurückgegebenen Zeiger verwenden, um die [IUnknown::Release-Methode auf](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufruft, wenn Sie damit fertig sind.</span><span class="sxs-lookup"><span data-stu-id="379d9-176">You must also use the returned pointer to call its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="379d9-177">Manchmal reicht das Festlegen der Flags im  _ulFlags-Parameter_ nicht aus, um den Typ des Zugriffs auf die erforderliche Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="379d9-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="379d9-178">Sie können zusätzliche Daten, z. B. Flags, im  _ulInterfaceOptions-Parameter_ speichern.</span><span class="sxs-lookup"><span data-stu-id="379d9-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="379d9-179">Diese Daten sind schnittstellenabhängig.</span><span class="sxs-lookup"><span data-stu-id="379d9-179">This data is interface dependent.</span></span> <span data-ttu-id="379d9-180">Einige Schnittstellen (z. **B. IStream)** verwenden sie, andere nicht.</span><span class="sxs-lookup"><span data-stu-id="379d9-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="379d9-181">Wenn Sie beispielsweise eine Eigenschaft öffnen, die mit **IStream** geändert werden soll, legen Sie das STGM_WRITE-Flag im  _ulInterfaceOptions-Parameter_ zusätzlich zu MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="379d9-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="379d9-182">Wenn Sie eine Tabelle mithilfe der [IMAPITable-Schnittstelle](imapitableiunknown.md) öffnen, können Sie  _ulInterfaceOptions_ auf MAPI_UNICODE festlegen, um anzugeben, ob die Spalten in der Tabelle, die Zeichenfolgeneigenschaften enthalten, im Unicode-Format vorliegen sollen.</span><span class="sxs-lookup"><span data-stu-id="379d9-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="379d9-183">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="379d9-183">MFCMAPI reference</span></span>

<span data-ttu-id="379d9-184">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="379d9-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="379d9-185">**Datei**</span><span class="sxs-lookup"><span data-stu-id="379d9-185">**File**</span></span>|<span data-ttu-id="379d9-186">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="379d9-186">**Function**</span></span>|<span data-ttu-id="379d9-187">**Comment**</span><span class="sxs-lookup"><span data-stu-id="379d9-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="379d9-188">StreamEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="379d9-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="379d9-189">CStreamEditor::ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="379d9-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="379d9-190">MFCMAPI verwendet die **IMAPIProp::OpenProperty-Methode,** um eine Streamschnittstelle für große Text- und Binäreigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="379d9-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="379d9-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="379d9-191">See also</span></span>

- [<span data-ttu-id="379d9-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="379d9-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="379d9-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="379d9-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="379d9-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="379d9-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="379d9-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="379d9-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="379d9-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="379d9-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="379d9-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="379d9-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="379d9-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="379d9-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="379d9-199">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="379d9-199">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="379d9-200">Öffnen einer Anlage</span><span class="sxs-lookup"><span data-stu-id="379d9-200">Opening an Attachment</span></span>](opening-an-attachment.md)

