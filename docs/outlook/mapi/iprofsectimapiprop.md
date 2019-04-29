---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406598"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="92c64-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="92c64-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="92c64-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92c64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92c64-105">Kann mit den Eigenschaften von profile section-Objekten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92c64-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92c64-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="92c64-106">Header file:</span></span>  <br/> |<span data-ttu-id="92c64-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="92c64-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="92c64-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="92c64-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="92c64-109">Profile section-Objekte</span><span class="sxs-lookup"><span data-stu-id="92c64-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="92c64-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="92c64-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="92c64-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="92c64-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="92c64-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="92c64-112">Called by:</span></span>  <br/> |<span data-ttu-id="92c64-113">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="92c64-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="92c64-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="92c64-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="92c64-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="92c64-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="92c64-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="92c64-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="92c64-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="92c64-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="92c64-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="92c64-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="92c64-119">Nicht durchgeführten</span><span class="sxs-lookup"><span data-stu-id="92c64-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="92c64-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="92c64-120">Vtable order</span></span>

<span data-ttu-id="92c64-121">Diese Schnittstelle hat keine eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="92c64-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="92c64-122">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="92c64-122">**Required properties**</span></span>|<span data-ttu-id="92c64-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="92c64-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="92c64-124">**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="92c64-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="92c64-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92c64-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="92c64-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="92c64-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="92c64-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92c64-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="92c64-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="92c64-128">Notes to callers</span></span>

<span data-ttu-id="92c64-129">Die **IProfSect** -Schnittstelle hat keine eigenen eindeutigen Methoden, aber Sie können die [IMAPIProp](imapipropiunknown.md) -Methoden des profile-Abschnitts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="92c64-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="92c64-130">Es gibt einige Unterschiede zwischen der **IProfSect** -Implementierung und anderen Implementierungen von **IMAPIProp**:</span><span class="sxs-lookup"><span data-stu-id="92c64-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="92c64-131">**IProfSect** unterstützt kein Transaktionsmodell.</span><span class="sxs-lookup"><span data-stu-id="92c64-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="92c64-132">**IProfSect** unterstützt keine benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92c64-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="92c64-133">**IProfSect** reserviert den bezeichnerbereich 0x67F0 zu 0x67ff für sichere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92c64-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="92c64-134">Nicht die Unterstützung eines Transaktionsmodells bewirkt, dass alle Änderungen, die an einem Profil Abschnitt vorgenommen wurden, nach Aufrufen der Methoden [IMAPIProp:: CopyProps](imapiprop-copyprops.md) und [IMAPIProp:: CopyTo](imapiprop-copyto.md) sofort stattfinden.</span><span class="sxs-lookup"><span data-stu-id="92c64-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="92c64-135">Aufrufe der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode sind erfolgreich, speichern jedoch tatsächlich keine Änderungen.</span><span class="sxs-lookup"><span data-stu-id="92c64-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="92c64-136">Um vor Änderungen zu schützen, die vorzeitig auftreten, müssen Dienstanbieter Kopien Ihrer Profilabschnitte erstellen, die Benutzern über Eigenschaftenblätter angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="92c64-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="92c64-137">Die Eigenschaftenblätter sollten mit der Kopie statt mit dem Abschnitt Real profile funktionieren.</span><span class="sxs-lookup"><span data-stu-id="92c64-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="92c64-138">Wenn der Benutzer auf die Schaltfläche **OK** klickt, um zu überprüfen, ob die Änderungen korrekt sind, können die Änderungen im Abschnitt Real Profile gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="92c64-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="92c64-139">Gehen Sie folgendermaßen vor, um ein Eigenschaftenfenster mithilfe eines kopierten Profil Abschnitts zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="92c64-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="92c64-140">Öffnen Sie den Profil Abschnitt, indem Sie die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -oder [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="92c64-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="92c64-141">Rufen Sie die [CreateIProp](createiprop.md) -Funktion auf, um ein Property-Datenobjekt abzurufen, ein Objekt, das die **IPropData** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="92c64-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="92c64-142">Rufen Sie die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode des profile-Abschnitts auf, um die Eigenschaften zu kopieren, die im Eigenschaftenfenster aus dem Profil Abschnitt in das Datenobjekt der Eigenschaft angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="92c64-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="92c64-143">Rufen Sie die [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) -Methode auf, um anzufordern, dass der Dienstanbieter ein Eigenschaftenfenster anzeigt, und übergeben Sie einen Zeiger auf das Datenobjekt der Eigenschaft im _lpConfigData_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="92c64-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="92c64-144">Wenn der Benutzer Änderungen an den Konfigurationseigenschaften im Eigenschaftenblatt speichert, rufen Sie die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode auf, um die Eigenschaften aus dem Eigenschaftendaten Objekt zurück in den Profil Abschnitt zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="92c64-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="92c64-145">Profilabschnitte unterstützen im Gegensatz zu anderen Objekten keine benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92c64-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="92c64-146">Die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) -Methoden geben MAPI_E_NO_SUPPORT zurück, wenn Sie für ein profile section-Objekt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="92c64-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="92c64-147">Wenn Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode verwenden, um Eigenschaftenbezeichner im 0X8000-Wert festzulegen, wird der PT_ERROR-Eigenschaftentyp zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="92c64-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="92c64-148">Profilabschnitte reservieren Sie den bezeichnerbereich 0x67F0 zu 0x67FF für sichere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92c64-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="92c64-149">Dienstanbieter können diese Bereiche verwenden, um Kennwörter und andere anbieterspezifische Anmeldeinformationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="92c64-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="92c64-150">Eigenschaften in diesem Bereichen werden nicht in der vollständigen Liste der Eigenschaften zurückgegeben, wenn NULL im _lpPropTag_ -Parameter der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode übergeben wird, noch werden Sie im _lppPropTagArray_ -Parameter des [ IMAPIProp::](imapiprop-getproplist.md) Getproplist-Methode.</span><span class="sxs-lookup"><span data-stu-id="92c64-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="92c64-151">Sichere Eigenschaften müssen speziell durch ihre Bezeichner angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="92c64-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="92c64-152">MAPI liefert einen Profil Abschnitt mit der hartcodierten Konstanten MUID_PROFILE_INSTANCE als Bezeichner und **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md)) als einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="92c64-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="92c64-153">MAPI stellt sicher, dass der Wert der **PR_SEARCH_KEY** -Eigenschaft für alle erstellten Profile eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="92c64-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="92c64-154">Verwenden Sie **PR_SEARCH_KEY** anstelle von **PR_PROFILE_NAME** , wenn Eindeutigkeit wichtig ist, da ein gelöschtes Profil von einem anderen Profil mit demselben Namen gefolgt werden kann.</span><span class="sxs-lookup"><span data-stu-id="92c64-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="92c64-155">Weitere Informationen zur Verwendung von Profil Abschnitten finden Sie unter [Verwalten von Profilen und Nachrichtendiensten](administering-profiles-and-message-services.md).</span><span class="sxs-lookup"><span data-stu-id="92c64-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="92c64-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92c64-156">See also</span></span>



[<span data-ttu-id="92c64-157">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="92c64-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

