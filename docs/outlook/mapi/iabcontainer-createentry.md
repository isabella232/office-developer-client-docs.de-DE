---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: acf9cee9bf0713b909b0d82fc606b015ac28474e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791977"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="dc4f2-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="dc4f2-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="dc4f2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc4f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc4f2-105">Erstellt einen neuen Eintrag, der ein messaging-Benutzer, eine Verteilerliste oder einen anderen Container sein kann.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="dc4f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc4f2-106">Parameters</span></span>

 <span data-ttu-id="dc4f2-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="dc4f2-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="dc4f2-108">[in] Die Anzahl von Bytes in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="dc4f2-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="dc4f2-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="dc4f2-110">[in] Ein Zeiger auf die Eintrags-ID eine Vorlage zum Erstellen neuer Einträge eines bestimmten Typs.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="dc4f2-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="dc4f2-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="dc4f2-112">[in] Eine Bitmaske aus Flags, die steuert, wie der Eintrag Erstellung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="dc4f2-113">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="dc4f2-113">The following flags can be set:</span></span>
    
<span data-ttu-id="dc4f2-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="dc4f2-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="dc4f2-115">Eine weit Ebene der Überprüfung doppelten Eintrags sollte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="dc4f2-116">Die Implementierung der weit doppelter Eintrag Überprüfung ist anbieterspezifisch.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="dc4f2-117">Beispielsweise kann ein Anbieter eine niedrigen Übereinstimmung definieren, wie alle zwei Einträge, die den gleichen Namen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="dc4f2-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="dc4f2-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="dc4f2-119">Eine strikt Überprüfen doppelter Eintrag sollte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="dc4f2-120">Die Implementierung der exakte doppelter Eintrag Überprüfung ist anbieterspezifisch.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="dc4f2-121">Ein Anbieter kann beispielsweise eine exakte Übereinstimmung definieren, wie alle zwei Einträge, die beide den gleichen Namen und die messaging-Adresse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="dc4f2-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="dc4f2-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="dc4f2-123">Ein neuer Eintrag sollte eine vorhandene ersetzen, wenn festgestellt wird, dass die beiden Duplikate sind.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="dc4f2-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="dc4f2-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="dc4f2-125">[out] Ein Zeiger auf einen Zeiger auf den neu erstellten Eintrag.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc4f2-126">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="dc4f2-126">Return value</span></span>

<span data-ttu-id="dc4f2-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc4f2-127">S_OK</span></span> 
  
> <span data-ttu-id="dc4f2-128">Der neue Eintrag wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc4f2-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc4f2-129">Remarks</span></span>

<span data-ttu-id="dc4f2-130">Die **IABContainer::CreateEntry** -Methode erstellt einen neuen Eintrag eines bestimmten Typs im angegebenen Container, einen Zeiger auf eine schnittstellenimplementierung für den weiteren Zugriff auf den Eintrag zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="dc4f2-131">Der neue Eintrag wird erstellt, mithilfe einer Vorlage, die aus dem Container-Liste der verfügbaren Vorlagen in der einmaligen Tabelle veröffentlicht ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="dc4f2-132">Anrufer zum Öffnen des Containers einmaligen Tabelle Aufrufen seiner [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode und die Eigenschaft **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) anfordern.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dc4f2-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="dc4f2-133">Notes to implementers</span></span>

<span data-ttu-id="dc4f2-134">Alle Container, die die **IABContainer::CreateEntry** -Methode unterstützen müssen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="dc4f2-135">Festlegen des Containers AB_MODIFIABLE Flag in seiner **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))-Eigenschaft, um anzugeben, dass es geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="dc4f2-136">Sie sollten alle Flags _UlCreateFlags_ unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="dc4f2-137">Die Interpretation und die Verwendung dieser Flags Implementierung ist jedoch bestimmte – d. h., können Sie ermitteln, Bedeutung der Semantik der CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT im Zusammenhang mit der Implementierung.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="dc4f2-138">Wenn Sie nicht oder nicht bestimmen, ob ein Eintrag vorhanden ist, können Sie immer den Eintrag erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="dc4f2-139">Einige Anbieter implementieren strenge Kontrolle durch den Anzeigenamen übereinstimmenden Eintrag messaging-Adresse und Suche Schlüssel in einem Eintrag. andere Anbieter beschränken Sie die Übereinstimmung um Namen und Adresse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="dc4f2-140">Überprüfung der weit Eintrag wird häufig Mobilgeräts auf nur den Anzeigenamen implementiert.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="dc4f2-141">Hinweise für Address Book Anbieterimplementierer hosten</span><span class="sxs-lookup"><span data-stu-id="dc4f2-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="dc4f2-142">Wenn Ihre Container Einträge aus den Vorlagen von anderen Anbietern erstellen kann, sollte die Implementierung von **CreateEntry** Speicher für einige oder alle erstellten Posten zugeordneten Eigenschaften bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="dc4f2-143">Wenn Sie Speicher für einen Eintrag **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft angeben, können Sie beispielsweise das Dialogfeld Details generieren, ohne abhängig von der fremde Anbieter.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="dc4f2-144">Wenn Ihre Container Einträge, die die **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft unterstützen erstellen kann, muss die Implementierung von **CreateEntry** Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="dc4f2-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="dc4f2-145">Rufen Sie die [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="dc4f2-146">**OpenTemplateID** ermöglicht der fremde Anbieter Code für den Eintrag zum Binden an den neuen Eintrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="dc4f2-147">Foreign Anbieter unterstützt diesen Bindungsvorgang um Kontrolle über die Einträge aus ihrer Vorlagen in die Container der Host von adressbuchanbietern implementierte erstellten erhalten.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="dc4f2-148">Führen Sie eine beliebige erforderliche Initialisierung, und füllen Sie das neue Objekt mit allen Eigenschaften aus den Eintrag in der fremden Anbieter, den das Objekt im Parameter _LppMAPIPropNew_ von **OpenTemplateID**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="dc4f2-149">Wenn **OpenTemplateID** erfolgreich ist, kopieren Sie die Eigenschaften auf die Implementierung auf das durch den Parameter _LppMAPIPropNew_ und nicht direkt an die Implementierung der auf den durch den Parameter _LpMAPIPropData_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="dc4f2-150">Initialisieren Sie den neuen Eintrag für die Offlineverwendung, wie Sie einen anderen Eintrag von einem fremden Anbieter.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="dc4f2-151">Wenn **OpenTemplateID** einen Fehler zurückgibt, sollte **CreateEntry** fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="dc4f2-152">Lassen Sie nicht den Eintrag erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="dc4f2-153">Da der fremde Anbieter Annahmen über die Daten im Anbieter machen kann, erstellen Sie einen Eintrag nicht mit einer Vorlage-ID, die nicht erfolgreich an den foreign Anbieter gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dc4f2-154">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="dc4f2-154">Notes to callers</span></span>

<span data-ttu-id="dc4f2-155">Wenn **CreateEntry** zurückgibt, Sie oder möglicherweise nicht sofort die Eintrags-ID für den neuen Eintrag zugreifen.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="dc4f2-156">Einige adressbuchanbietern implementierte machen nicht es erst verfügbar, nachdem Sie den neuen Eintrag [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="dc4f2-157">Obwohl doppelte Überprüfung Flags an **CreateEntry**als Parameter übergeben werden, tritt das Duplikat Überprüfung der Vorgang nicht bis **SaveChanges** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="dc4f2-158">Aus diesem Grund werden verwandte Fehler wie MAPI_E_COLLISION, gibt an, dass versucht wurde, einen bereits vorhandenen Eintrag erstellen, von **SaveChanges** statt **CreateEntry**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc4f2-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc4f2-159">See also</span></span>



[<span data-ttu-id="dc4f2-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="dc4f2-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="dc4f2-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="dc4f2-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="dc4f2-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="dc4f2-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="dc4f2-163">PidTagCreateTemplates (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dc4f2-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="dc4f2-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="dc4f2-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

