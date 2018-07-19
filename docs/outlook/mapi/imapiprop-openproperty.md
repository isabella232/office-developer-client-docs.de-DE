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
ms.openlocfilehash: 656e5c5532edfc6c791ca30aa30f4c4d96847295
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792284"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="cf73f-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="cf73f-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="cf73f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cf73f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cf73f-105">Gibt einen Zeiger auf eine Schnittstelle, die Zugriff auf eine Eigenschaft verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="cf73f-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="cf73f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf73f-106">Parameters</span></span>

 <span data-ttu-id="cf73f-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="cf73f-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="cf73f-108">[in] Die Eigenschaftentag für die Eigenschaft zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="cf73f-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="cf73f-109">Der Bezeichner und der Typ müssen in das Eigenschafts-Tag enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="cf73f-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="cf73f-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="cf73f-110">_lpiid_</span></span>
  
> <span data-ttu-id="cf73f-111">[in] Ein Zeiger auf den Bezeichner für die Schnittstelle für den Zugriff auf die Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf73f-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="cf73f-112">Der Parameter _Lpiid_ darf nicht **null**sein.</span><span class="sxs-lookup"><span data-stu-id="cf73f-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="cf73f-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="cf73f-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="cf73f-114">[in] Daten, die die Benutzeroberfläche, die vom Parameter _Lpiid_ beziehen.</span><span class="sxs-lookup"><span data-stu-id="cf73f-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="cf73f-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf73f-115">_ulFlags_</span></span>
  
> <span data-ttu-id="cf73f-116">[in] Eine Bitmaske der Flags, die Steuerung des Zugriffs auf die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cf73f-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="cf73f-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cf73f-117">The following flags can be set:</span></span>
    
<span data-ttu-id="cf73f-118">MAPI_CREATE IST</span><span class="sxs-lookup"><span data-stu-id="cf73f-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="cf73f-119">Wenn die Eigenschaft nicht vorhanden ist, sollte er erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cf73f-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="cf73f-120">Wenn die Eigenschaft vorhanden ist, sollte der aktuelle Wert der Eigenschaft verworfen.</span><span class="sxs-lookup"><span data-stu-id="cf73f-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="cf73f-121">Wenn ein Anrufer das Flag MAPI_CREATE ist festlegt, sollte auch die Kennzeichen MAPI_MODIFY festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf73f-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="cf73f-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="cf73f-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="cf73f-123">Ermöglicht **OpenProperty** erfolgreich, möglicherweise beendet, bevor das Objekt an den Anrufer vollständig verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cf73f-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="cf73f-124">Wenn das Objekt nicht verfügbar ist, kann die nachfolgenden Objekt Anrufen ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="cf73f-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="cf73f-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="cf73f-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="cf73f-126">MAPI_MODIFY ist in den folgenden Situationen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="cf73f-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="cf73f-127">Wenn eine Stream-Eigenschaft, wie beispielsweise **IID_IStream**zum Bearbeiten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cf73f-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="cf73f-128">Wenn eine Anlage eingebettete Nachricht öffnen, wie [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) mit **IID_IMessage**zum Bearbeiten geöffnet.</span><span class="sxs-lookup"><span data-stu-id="cf73f-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="cf73f-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="cf73f-129">_lppUnk_</span></span>
  
> <span data-ttu-id="cf73f-130">[out] Ein Zeiger auf die angeforderte Schnittstelle für den Zugriff auf Eigenschaften verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf73f-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf73f-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf73f-131">Return value</span></span>

<span data-ttu-id="cf73f-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf73f-132">S_OK</span></span> 
  
> <span data-ttu-id="cf73f-133">Der angeforderte Schnittstellenzeiger wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf73f-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="cf73f-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="cf73f-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="cf73f-135">Die angeforderte Schnittstelle wird für diese Eigenschaft nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cf73f-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="cf73f-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="cf73f-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="cf73f-137">Der Aufrufer verfügt nicht über ausreichende Berechtigungen zum Zugriff auf die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cf73f-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="cf73f-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cf73f-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="cf73f-139">Das Objekt kann nicht über Zugriff auf diese Eigenschaft über die angeforderte Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="cf73f-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="cf73f-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cf73f-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cf73f-141">Die angeforderte-Eigenschaft ist nicht vorhanden und MAPI_CREATE ist in der _UlFlags_ -Parameter nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="cf73f-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="cf73f-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cf73f-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="cf73f-143">Der Eigenschaftentyp im Tag wird auf PT_UNSPECIFIED festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf73f-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf73f-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf73f-144">Remarks</span></span>

<span data-ttu-id="cf73f-145">Die **IMAPIProp::OpenProperty** -Methode ermöglicht den Zugriff auf eine Eigenschaft über eine bestimmte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cf73f-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="cf73f-146">**OpenProperty** ist eine Alternative an die Methoden [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="cf73f-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="cf73f-147">Rufen Sie **GetProps** oder **SetProps** fehlschlägt, weil die Eigenschaft zu groß oder zu komplex ist, **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="cf73f-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="cf73f-148">**OpenProperty** wird in der Regel vom Typ PT_OBJECT Eigenschaften zugreifen.</span><span class="sxs-lookup"><span data-stu-id="cf73f-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cf73f-149">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="cf73f-149">Notes to callers</span></span>

<span data-ttu-id="cf73f-150">Öffnen Sie den Zugriff auf e-Mail-Anlagen die **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))-Eigenschaft mit einem anderen Schnittstellenbezeichner, je nach Art der Anlage ein.</span><span class="sxs-lookup"><span data-stu-id="cf73f-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="cf73f-151">In der folgenden Tabelle wird beschrieben, wie für die verschiedenen Typen von Anlagen **OpenProperty** aufrufen:</span><span class="sxs-lookup"><span data-stu-id="cf73f-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="cf73f-152">**Typ der Anlage**</span><span class="sxs-lookup"><span data-stu-id="cf73f-152">**Type of attachment**</span></span>|<span data-ttu-id="cf73f-153">**Schnittstellenbezeichner, der verwendet**</span><span class="sxs-lookup"><span data-stu-id="cf73f-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf73f-154">Binary</span><span class="sxs-lookup"><span data-stu-id="cf73f-154">Binary</span></span>  <br/> |<span data-ttu-id="cf73f-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="cf73f-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="cf73f-156">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cf73f-156">String</span></span>  <br/> |<span data-ttu-id="cf73f-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="cf73f-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="cf73f-158">Nachricht</span><span class="sxs-lookup"><span data-stu-id="cf73f-158">Message</span></span>  <br/> |<span data-ttu-id="cf73f-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="cf73f-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="cf73f-160">OLE 2.0</span><span class="sxs-lookup"><span data-stu-id="cf73f-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="cf73f-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="cf73f-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="cf73f-162">**IStreamDocfile** ist eine Ableitung von der [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) -Schnittstelle, die auf eine Verbunddatei OLE 2.0 basiert.</span><span class="sxs-lookup"><span data-stu-id="cf73f-162">**IStreamDocfile** is a derivative of the [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="cf73f-163">**IStreamDocfile** ist die beste Wahl für den Zugriff auf OLE 2.0-Anlagen, da er den geringsten Aufwand erfordert.</span><span class="sxs-lookup"><span data-stu-id="cf73f-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="cf73f-164">Sie können IID_IStreamDocFile für diese Eigenschaften verwenden, die in strukturierten Speicher verfügbar über die Schnittstelle [IStorage](http://msdn.microsoft.com/de-de/library/aa380015%28VS.85%29.aspx) gespeicherte Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="cf73f-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](http://msdn.microsoft.com/de-de/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="cf73f-165">Weitere Informationen zur Verwendung von **OpenProperty** mit Anlagen finden Sie unter der **PR_ATTACH_DATA_OBJ** -Eigenschaft und [eine Anlage zu öffnen](opening-an-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="cf73f-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="cf73f-166">Verwenden Sie nicht den **IStream** Zeiger, den Sie erhalten, um entweder die [Seek](http://msdn.microsoft.com/de-de/library/aa380043%28v=VS.85%29.aspx) oder [SetSize](http://msdn.microsoft.com/de-de/library/aa380044%28v=VS.85%29.aspx) -Methode aufrufen, es sei denn, Sie eine NULL Variable Größe oder Position verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf73f-166">Do not use the **IStream** pointer that you receive to call either its [Seek](http://msdn.microsoft.com/de-de/library/aa380043%28v=VS.85%29.aspx) or [SetSize](http://msdn.microsoft.com/de-de/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="cf73f-167">Darüber hinaus verlassen Sie sich nicht auf dem Wert der _PlibNewPosition_ Output-Parameter des Aufrufs **Seek** .</span><span class="sxs-lookup"><span data-stu-id="cf73f-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="cf73f-168">Wenn Sie **OpenProperty** Zugriff auf eine Eigenschaft mit der **IStream** -Schnittstelle aufrufen, verwenden Sie nur die Schnittstelle, es zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cf73f-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="cf73f-169">Versuchen Sie nicht so aktualisieren Sie die Eigenschaft mit den anderen [IMAPIProp: IUnknown](imapipropiunknown.md) Methoden, wie **SetProps** oder [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span><span class="sxs-lookup"><span data-stu-id="cf73f-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="cf73f-170">Versuchen Sie nicht mehr als einmal eine Eigenschaft mit **OpenProperty** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="cf73f-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="cf73f-171">Die Ergebnisse sind nicht definiert, da sie von Anbieter zu Anbieter unterschiedlich sein können.</span><span class="sxs-lookup"><span data-stu-id="cf73f-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="cf73f-172">Wenn Sie so ändern Sie die Eigenschaft geöffnet werden soll müssen, legen Sie das MAPI_MODIFY-Flag.</span><span class="sxs-lookup"><span data-stu-id="cf73f-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="cf73f-173">Wenn Sie nicht sicher sind, ob das Objekt die Eigenschaft unterstützt, aber es sollte Ihrer Meinung, legen Sie die Kennzeichen MAPI_CREATE ist und MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="cf73f-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="cf73f-174">Bei jedem MAPI_CREATE ist festgelegt ist, muss auch MAPI_MODIFY festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cf73f-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="cf73f-175">Sie sind verantwortlich für recasting Zeiger der Schnittstelle, die für die Schnittstelle im _Lpiid_ -Parameter angegebene geeignet ist im Parameter _LppUnk_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf73f-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="cf73f-176">Sie müssen außerdem den zurückgegebenen Zeiger verwenden, seine [IUnknown](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen, wenn Sie mit ihm fertig sind.</span><span class="sxs-lookup"><span data-stu-id="cf73f-176">You must also use the returned pointer to call its [IUnknown::Release](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="cf73f-177">In einigen Fällen festlegen die Kennzeichen in der _UlFlags_ -Parameter ist nicht genug sind, um den Zugriff auf die Eigenschaft anzugeben, der erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cf73f-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="cf73f-178">Sie können zusätzliche Daten enthält, wie Flags, die im Parameter _UlInterfaceOptions_ abgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf73f-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="cf73f-179">Diese Daten werden abhängige Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cf73f-179">This data is interface dependent.</span></span> <span data-ttu-id="cf73f-180">Einige Schnittstellen (wie **IStream**) verwenden, und andere nicht.</span><span class="sxs-lookup"><span data-stu-id="cf73f-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="cf73f-181">Legen Sie die Kennzeichen STGM_WRITE im Parameter _UlInterfaceOptions_ neben MAPI_MODIFY beispielsweise beim Öffnen einer Eigenschaft mit **IStream**geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf73f-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="cf73f-182">Beim Öffnen einer Tabelle mithilfe der [IMAPITable](imapitableiunknown.md) -Schnittstelle können Sie _UlInterfaceOptions_ festlegen, um Parameter MAPI_UNICODE, um anzugeben, ob die Spalten in der Tabelle, die Zeichenfolgeneigenschaften enthalten, im Unicode-Format sein soll.</span><span class="sxs-lookup"><span data-stu-id="cf73f-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cf73f-183">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="cf73f-183">MFCMAPI reference</span></span>

<span data-ttu-id="cf73f-184">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cf73f-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cf73f-185">**Datei**</span><span class="sxs-lookup"><span data-stu-id="cf73f-185">**File**</span></span>|<span data-ttu-id="cf73f-186">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="cf73f-186">**Function**</span></span>|<span data-ttu-id="cf73f-187">**Comment**</span><span class="sxs-lookup"><span data-stu-id="cf73f-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf73f-188">StreamEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="cf73f-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="cf73f-189">CStreamEditor::ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="cf73f-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="cf73f-190">MFCMAPI (engl.) wird die **IMAPIProp::OpenProperty** -Methode verwendet, um eine Stream-Schnittstelle für große Text- und binäre Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cf73f-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf73f-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf73f-191">See also</span></span>

- [<span data-ttu-id="cf73f-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="cf73f-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="cf73f-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="cf73f-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="cf73f-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="cf73f-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="cf73f-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="cf73f-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="cf73f-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="cf73f-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="cf73f-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf73f-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="cf73f-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf73f-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="cf73f-199">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="cf73f-199">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="cf73f-200">Öffnen einer Anlage</span><span class="sxs-lookup"><span data-stu-id="cf73f-200">Opening an Attachment</span></span>](opening-an-attachment.md)

