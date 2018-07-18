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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f99843bcdf3689acad72145a33d6a9804175a413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792408"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="85297-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="85297-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="85297-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85297-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85297-105">Öffnet einen Empfänger Eintrag in einem fremden Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="85297-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="85297-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85297-106">Parameters</span></span>

 <span data-ttu-id="85297-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="85297-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="85297-108">[in] Die Byteanzahl von in der Vorlagenbezeichner auf _LpTemplateID_zeigt.</span><span class="sxs-lookup"><span data-stu-id="85297-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="85297-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="85297-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="85297-110">[in] Ein Zeiger auf den Vorlagenbezeichner **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft des Empfängers Eintrags geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85297-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="85297-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="85297-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="85297-112">[in] Eine Bitmaske der Flags verwendet, um den Eintrag öffnen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="85297-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="85297-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="85297-113">The following flag can be set:</span></span>
    
<span data-ttu-id="85297-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="85297-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="85297-115">Ein neuer Eintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="85297-115">A new entry is being created.</span></span> <span data-ttu-id="85297-116">Wenn der Anbieter fremde den nachfolgenden [OpenTemplateID](iablogon-opentemplateid.md) Aufruf von MAPI empfängt, können sie steuern, wie der Eintrag erstellt wird, durch Ändern der Eigenschaften auf die durch den Parameter _LpMAPIPropData_ oder durch eine bestimmte Schnittstelle zurückgeben Implementierung in _LppMAPIPropNew_ steuern, wie die Eigenschaften für den neuen Eintrag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="85297-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="85297-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="85297-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="85297-118">[in] Ein Zeiger auf die Implementierung der Schnittstelle, die der Anrufer wird verwendet, um den Eintrag zugreifen.</span><span class="sxs-lookup"><span data-stu-id="85297-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="85297-119">Dies ist die Implementierung, die der fremde Anbieter mit einer eigenen Implementierung umschließen und im Parameter _LppMAPIPropNew_ zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="85297-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="85297-120">Der Parameter _LpMAPIPropData_ muss zeigen Sie auf eine Implementierung der Lese-Schreib-Schnittstelle, die von abgeleitet wird [IMAPIProp: IUnknown](imapipropiunknown.md) und unterstützt die Schnittstelle im Parameter _LpInterface_ angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="85297-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="85297-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="85297-121">_lpInterface_</span></span>
  
> <span data-ttu-id="85297-122">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, um Zugriff auf den Eintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="85297-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="85297-123">Der Parameter _LppMAPIPropNew_ verweist auf eine Schnittstelle des Typs durch _LpInterface_angegeben.</span><span class="sxs-lookup"><span data-stu-id="85297-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="85297-124">Übergeben von NULL gibt die Standardschnittstelle für ein messaging-Benutzer IID_IMailUser zurück.</span><span class="sxs-lookup"><span data-stu-id="85297-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="85297-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="85297-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="85297-126">[out] Ein Zeiger auf die Implementierung, die der fremde Anbieter für den Zugriff auf den Eintrag bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="85297-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="85297-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="85297-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="85297-128">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="85297-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="85297-129">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="85297-129">Return value</span></span>

<span data-ttu-id="85297-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="85297-130">S_OK</span></span> 
  
> <span data-ttu-id="85297-131">Der Bindungsprozess war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="85297-131">The binding process was successful.</span></span>
    
<span data-ttu-id="85297-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="85297-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="85297-133">Die foreign-Adressbuchanbieter ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="85297-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85297-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85297-134">Remarks</span></span>

<span data-ttu-id="85297-135">Die **IMAPISupport::OpenTemplateID** -Methode ist nur für Address Book Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="85297-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="85297-136">**OpenTemplateID** wird nur von adressbuchanbietern implementierte aufgerufen, die als Hosts für Einträge verwendet werden können, die andere adressbuchanbietern implementierte, auch bekannt als fremden Anbietern angehören.</span><span class="sxs-lookup"><span data-stu-id="85297-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="85297-137">Hostanbieter Aufrufen **OpenTemplateID** um einen fremden Eintrag öffnen, in dem tritt auf, wenn Daten in Hostanbieter Code im fremden Anbieter gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="85297-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="85297-138">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="85297-138">Notes to callers</span></span>

<span data-ttu-id="85297-139">Rufen Sie **OpenTemplateID** nur, wenn Sie die Speicherung von Einträgen mit Vorlage Bezeichner aus fremden adressbuchanbietern implementierte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="85297-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="85297-140">Eine solche Unterstützung platziert zusätzliche Anforderungen in Ihrer [IABContainer::CreateEntry](iabcontainer-createentry.md) und [IABLogon::OpenEntry](iablogon-openentry.md) Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="85297-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="85297-141">Weitere Informationen finden Sie in den Beschreibungen dieser Methoden und [fungiert als ein Host-Adressbuchanbieter](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="85297-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="85297-142">Wenn der Anruf **OpenTemplateID** als gebundenen Schnittstelle die Implementierung der gleichen Eigenschaft-Objekt, der Sie übergeben zurückgibt, können Sie den Verweis auf Ihre Property-Objekt freigeben.</span><span class="sxs-lookup"><span data-stu-id="85297-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="85297-143">Dies ist, da der fremde Anbieter das Objekt **AddRef** -Methode, um einen eigenen Verweis behalten aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="85297-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="85297-144">Wenn der fremde Anbieter keinen Verweis auf das Property-Objekt behalten muss, gibt **OpenTemplateID** ungebundenen Property-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="85297-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="85297-145">Wenn **OpenTemplateID** mit MAPI_E_UNKNOWN_ENTRYID fehlschlägt, versuchen Sie, fortfahren, indem Sie den Eintrag im schreibgeschützten Modus behandelt.</span><span class="sxs-lookup"><span data-stu-id="85297-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85297-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85297-146">See also</span></span>



[<span data-ttu-id="85297-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="85297-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="85297-148">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="85297-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="85297-149">PidTagTemplateid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="85297-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="85297-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="85297-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

