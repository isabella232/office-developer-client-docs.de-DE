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
ms.openlocfilehash: a8152a9cad7623a077cd9df3f678a9ada56e3960
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577961"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="0110f-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0110f-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="0110f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0110f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0110f-105">Funktioniert mit den Eigenschaften des Profils Section-Objekten.</span><span class="sxs-lookup"><span data-stu-id="0110f-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0110f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0110f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0110f-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="0110f-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="0110f-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="0110f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0110f-109">Profil Section-Objekten</span><span class="sxs-lookup"><span data-stu-id="0110f-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="0110f-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0110f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0110f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="0110f-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="0110f-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0110f-112">Called by:</span></span>  <br/> |<span data-ttu-id="0110f-113">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0110f-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="0110f-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="0110f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0110f-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="0110f-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="0110f-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="0110f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0110f-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="0110f-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="0110f-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="0110f-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="0110f-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="0110f-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0110f-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="0110f-120">Vtable order</span></span>

<span data-ttu-id="0110f-121">Diese Schnittstelle hat keinen eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="0110f-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="0110f-122">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="0110f-122">**Required properties**</span></span>|<span data-ttu-id="0110f-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="0110f-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0110f-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0110f-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0110f-125">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0110f-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="0110f-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0110f-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0110f-127">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0110f-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="0110f-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0110f-128">Notes to callers</span></span>

<span data-ttu-id="0110f-129">Die Schnittstelle **IProfSect** hat keinen eindeutigen Methoden eigenen, aber Sie können das Profil des Abschnitts [IMAPIProp](imapipropiunknown.md) Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0110f-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="0110f-130">Es gibt einige Unterschiede zwischen den **IProfSect** Implementierung und Implementierungen **IMAPIProp**:</span><span class="sxs-lookup"><span data-stu-id="0110f-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="0110f-131">Ein Transaktionsmodell unterstützt **IProfSect** nicht.</span><span class="sxs-lookup"><span data-stu-id="0110f-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="0110f-132">**IProfSect** unterstützt keine benannte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0110f-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="0110f-133">**IProfSect** reserviert Bezeichner Bereich 0x67F0 zu 0x67ff sicheren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0110f-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="0110f-134">Nicht unterstützt, eine Transaktionsmodell bedeutet, dass alle Änderungen vorgenommen wurden, die ein Profil im folgenden Abschnitt zu den [IMAPIProp::CopyProps](imapiprop-copyprops.md) aufruft und [IMAPIProp::CopyTo](imapiprop-copyto.md) Methoden unmittelbar ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0110f-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="0110f-135">Aufrufe der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode erfolgreich ausgeführt, aber nicht tatsächlich Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="0110f-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="0110f-136">Um von Änderungen geschützt werden, die vorzeitig auftreten, müssen Dienstanbieter Kopien der Abschnitte, deren Profil erstellen, die Benutzer über Eigenschaftenseiten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0110f-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="0110f-137">Die Eigenschaftenseiten sollte mit der Kopie, anstatt Abschnitts realen Profile funktionieren.</span><span class="sxs-lookup"><span data-stu-id="0110f-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="0110f-138">Wenn der Benutzer klickt auf die Schaltfläche **OK** , um sicherzustellen, dass die Änderungen korrekt sind, können die Änderungen in den Profilabschnitt realen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0110f-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="0110f-139">Zur Implementierung von einem Eigenschaftenfenster unter Verwendung eines Abschnitts kopierte Profil verwenden Sie die folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0110f-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="0110f-140">Öffnen Sie den Profilabschnitt, durch die [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) oder [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0110f-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="0110f-141">Rufen Sie die [CreateIProp](createiprop.md) -Funktion zum Abrufen einer Eigenschaft Datenobjekt – ein Objekt, das die **IPropData** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0110f-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="0110f-142">Rufen Sie den Profilabschnitt [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode zum Kopieren Sie der Eigenschaften, die auf der Eigenschaftenseite auf die Daten Property-Objekt aus dem Profilabschnitt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0110f-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="0110f-143">Rufen Sie die [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) -Methode, um anzufordern, dass der Dienstanbieter Anzeigen eines Eigenschaftenblatts und einen Zeiger auf das Eigenschaftenobjekt Daten im _LpConfigData_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="0110f-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="0110f-144">Wenn der Benutzer Änderungen auf die Konfigurationseigenschaften im Eigenschaftenfenster speichert, rufen Sie die [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode, um die Eigenschaften aus der Eigenschaftenobjekt Daten zurück in den Profilabschnitt kopieren.</span><span class="sxs-lookup"><span data-stu-id="0110f-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="0110f-145">Profil Abschnitte, im Gegensatz zu anderen Objekten unterstützen keine benannte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0110f-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="0110f-146">Die Methoden [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) zurück MAPI_E_NO_SUPPORT, wenn sie auf ein Profil Section-Objekt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0110f-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="0110f-147">Wenn Sie im Bereich über 0 x 8000 Eigenschaftenbezeichner festlegen die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode verwenden, werden der Typ der PT_ERROR-Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0110f-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="0110f-148">Profil Abschnitte reservieren Bezeichner Bereich 0x67F0 zu 0x67FF sicheren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0110f-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="0110f-149">Dienstanbieter können diesen Bereich zum Speichern von Kennwörtern und anderen anbieterspezifische Anmeldeinformationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="0110f-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="0110f-150">Eigenschaften in diesem Bereich werden nicht in die vollständige Liste der Eigenschaften zurückgegeben, wenn NULL im _LpPropTag_ -Parameter der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode übergeben wird, noch werden sie in der _LppPropTagArray_ -Parameter, der die [zurückgegeben IMAPIProp::GetPropList](imapiprop-getproplist.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="0110f-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="0110f-151">Schützen von Eigenschaften müssen insbesondere anhand der dazugehörigen Bezeichner angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0110f-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="0110f-152">MAPI stellt einen Profilabschnitt mit hartcodierten Konstante MUID_PROFILE_INSTANCE als Bezeichner und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) als ihre einzige Eigenschaft bereit.</span><span class="sxs-lookup"><span data-stu-id="0110f-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="0110f-153">MAPI wird sichergestellt, dass der Wert der **PR_SEARCH_KEY** -Eigenschaft für alle erstellten Profile eindeutig sein wird.</span><span class="sxs-lookup"><span data-stu-id="0110f-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="0110f-154">Verwenden Sie **PR_SEARCH_KEY** anstelle **PR_PROFILE_NAME** , wenn die Eindeutigkeit wichtig ist, da es zu einem anderen Profil mit dem gleichen Namen folgen gelöschten Profil möglich ist.</span><span class="sxs-lookup"><span data-stu-id="0110f-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="0110f-155">Weitere Informationen zur Verwendung von Profil Abschnitten finden Sie unter [Verwalten von Benutzerprofilen und Message-Dienste](administering-profiles-and-message-services.md).</span><span class="sxs-lookup"><span data-stu-id="0110f-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0110f-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0110f-156">See also</span></span>



[<span data-ttu-id="0110f-157">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0110f-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

