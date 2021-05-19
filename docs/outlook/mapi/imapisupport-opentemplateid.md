---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418505"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="6dfb0-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="6dfb0-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="6dfb0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dfb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dfb0-105">Öffnet einen Empfängereintrag in einem fremden Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a><span data-ttu-id="6dfb0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dfb0-106">Parameters</span></span>

 <span data-ttu-id="6dfb0-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="6dfb0-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="6dfb0-108">[in] Die Byteanzahl in der Vorlagen-ID, auf die _von lpTemplateID verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="6dfb0-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="6dfb0-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="6dfb0-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="6dfb0-110">[in] Ein Zeiger auf die **Vorlagen-ID PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft des zu öffnenden Empfängereintrags.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="6dfb0-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="6dfb0-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="6dfb0-112">[in] Eine Bitmaske mit Flags, mit der das Öffnen des Eintrags beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="6dfb0-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6dfb0-113">The following flag can be set:</span></span>
    
<span data-ttu-id="6dfb0-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="6dfb0-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="6dfb0-115">Ein neuer Eintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-115">A new entry is being created.</span></span> <span data-ttu-id="6dfb0-116">Wenn der fremde Anbieter den nachfolgenden [IABLogon::OpenTemplateID-Aufruf](iablogon-opentemplateid.md) von MAPI empfängt, kann er steuern, wie der Eintrag erstellt wird, indem Eigenschaften geändert werden, auf die der  _lpMAPIPropData-Parameter_ verweist, oder indem er eine bestimmte Schnittstellenimplementierung in  _lppMAPIPropNew_ zurück gibt, um zu steuern, wie Eigenschaften für den neuen Eintrag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="6dfb0-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="6dfb0-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="6dfb0-118">[in] Ein Zeiger auf die Schnittstellenimplementierung, die der Aufrufer für den Zugriff auf den Eintrag verwendet.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="6dfb0-119">Dies ist die Implementierung, die der fremde Anbieter mit einer eigenen Implementierung umschließen und im  _lppMAPIPropNew-Parameter zurückgeben_ kann.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="6dfb0-120">Der  _lpMAPIPropData-Parameter_ muss auf eine Lese-/Schreibschnittstellenimplementierung verweisen, die von [IMAPIProp : IUnknown](imapipropiunknown.md) ab leitet und die Schnittstelle unterstützt, die im  _lpInterface-Parameter_ angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="6dfb0-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6dfb0-121">_lpInterface_</span></span>
  
> <span data-ttu-id="6dfb0-122">[in] Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf den Eintrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="6dfb0-123">Der _lppMAPIPropNew-Parameter_ verweist auf eine Schnittstelle des typs, der durch _lpInterface angegeben wird._</span><span class="sxs-lookup"><span data-stu-id="6dfb0-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="6dfb0-124">Durch Übergeben von NULL wird die Standardschnittstelle für einen Messagingbenutzer IID_IMailUser.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="6dfb0-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="6dfb0-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="6dfb0-126">[out] Ein Zeiger auf die Schnittstellenimplementierung, die der fremde Anbieter für den Zugriff auf den Eintrag zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="6dfb0-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="6dfb0-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="6dfb0-128">Reserviert; muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6dfb0-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6dfb0-129">Return value</span></span>

<span data-ttu-id="6dfb0-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="6dfb0-130">S_OK</span></span> 
  
> <span data-ttu-id="6dfb0-131">Der Bindungsprozess war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-131">The binding process was successful.</span></span>
    
<span data-ttu-id="6dfb0-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6dfb0-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="6dfb0-133">Der fremde Adressbuchanbieter ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6dfb0-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6dfb0-134">Remarks</span></span>

<span data-ttu-id="6dfb0-135">Die **IMAPISupport::OpenTemplateID-Methode** wird nur für Unterstützungsobjekte des Adressbuchanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="6dfb0-136">**OpenTemplateID** wird nur von Adressbuchanbietern aufgerufen, die als Hosts für Einträge fungieren können, die zu anderen Adressbuchanbietern gehören, auch als fremde Anbieter bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="6dfb0-137">Hostanbieter rufen **OpenTemplateID auf,** um einen fremden Eintrag zu öffnen, der auftritt, wenn Daten im Hostanbieter an Code im fremden Anbieter gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6dfb0-138">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="6dfb0-138">Notes to callers</span></span>

<span data-ttu-id="6dfb0-139">Rufen **Sie OpenTemplateID** nur auf, wenn Sie die Speicherung von Einträgen mit Vorlagenbezeichnern von fremden Adressbuchanbietern unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="6dfb0-140">Diese Unterstützung stellt zusätzliche Anforderungen an Ihre [IABContainer::CreateEntry-](iabcontainer-createentry.md) und [IABLogon::OpenEntry-Implementierungen.](iablogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="6dfb0-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="6dfb0-141">Weitere Informationen finden Sie in den Beschreibungen dieser Methoden und [in Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6dfb0-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="6dfb0-142">Wenn der **OpenTemplateID-Aufruf** als gebundene Schnittstelle dieselbe Eigenschaftsobjektimplementierung zurückgibt, die Sie übergeben haben, können Sie Den Verweis auf Ihr Eigenschaftsobjekt los.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="6dfb0-143">Dies liegt daran, dass der fremde Anbieter die **AddRef-Methode** des Objekts aufgerufen hat, um einen eigenen Verweis zu behalten.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="6dfb0-144">Wenn der fremde Anbieter keinen Verweis auf das Eigenschaftsobjekt behalten muss, gibt **OpenTemplateID** das ungebundene Eigenschaftsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="6dfb0-145">Wenn **OpenTemplateID** mit MAPI_E_UNKNOWN_ENTRYID fehlert, versuchen Sie, den Eintrag als schreibgeschützt zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="6dfb0-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6dfb0-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dfb0-146">See also</span></span>



[<span data-ttu-id="6dfb0-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="6dfb0-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="6dfb0-148">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6dfb0-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="6dfb0-149">PidTagTemplateid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6dfb0-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="6dfb0-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6dfb0-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

