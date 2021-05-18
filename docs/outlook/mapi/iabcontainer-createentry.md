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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f80130279e3437dd9be947de97d3f0d4181165e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411274"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="c0a0a-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="c0a0a-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="c0a0a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0a0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0a0a-105">Erstellt einen neuen Eintrag, der ein Messagingbenutzer, eine Verteilerliste oder ein anderer Container sein kann.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="c0a0a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0a0a-106">Parameters</span></span>

 <span data-ttu-id="c0a0a-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c0a0a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c0a0a-108">[in] Die Anzahl der Bytes in der Eintrags-ID, auf die der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c0a0a-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c0a0a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c0a0a-110">[in] Ein Zeiger auf die Eintrags-ID einer Vorlage zum Erstellen neuer Einträge eines bestimmten Typs.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="c0a0a-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="c0a0a-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="c0a0a-112">[in] Eine Bitmaske mit Flags, die steuert, wie die Erstellung von Eingaben ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="c0a0a-113">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c0a0a-113">The following flags can be set:</span></span>
    
<span data-ttu-id="c0a0a-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="c0a0a-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="c0a0a-115">Es sollte eine lose Ebene doppelter Eingabeprüfungen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="c0a0a-116">Die Implementierung der Überprüfung von losen doppelten Einträgen ist anbieterspezifisch.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="c0a0a-117">Beispielsweise kann ein Anbieter eine lose Übereinstimmung als zwei beliebige Einträge definieren, die denselben Anzeigenamen haben.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="c0a0a-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="c0a0a-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="c0a0a-119">Es sollte eine strenge Stufe doppelter Eingabeprüfungen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="c0a0a-120">Die Implementierung einer strengen Doppelten Eintragsprüfung ist anbieterspezifisch.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="c0a0a-121">Ein Anbieter kann z. B. eine strikte Übereinstimmung als zwei Einträge definieren, die denselben Anzeigenamen und dieselbe Messagingadresse haben.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="c0a0a-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="c0a0a-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="c0a0a-123">Ein neuer Eintrag sollte einen vorhandenen Eintrag ersetzen, wenn festgestellt wird, dass es sich bei den beiden um Duplikate handelt.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="c0a0a-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="c0a0a-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="c0a0a-125">[out] Ein Zeiger auf einen Zeiger auf den neu erstellten Eintrag.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0a0a-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0a0a-126">Return value</span></span>

<span data-ttu-id="c0a0a-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0a0a-127">S_OK</span></span> 
  
> <span data-ttu-id="c0a0a-128">Der neue Eintrag wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0a0a-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0a0a-129">Remarks</span></span>

<span data-ttu-id="c0a0a-130">Die **IABContainer::CreateEntry-Methode** erstellt einen neuen Eintrag eines bestimmten Typs im angegebenen Container und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, um weiteren Zugriff auf den Eintrag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="c0a0a-131">Der neue Eintrag wird mithilfe einer Vorlage erstellt, die aus der Liste der verfügbaren Vorlagen ausgewählt wurde, die in der einzigen Tabelle veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="c0a0a-132">Aufrufer greifen auf die #A0 eines Containers zu, indem sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) aufrufen und die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft anfordern.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c0a0a-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c0a0a-133">Notes to implementers</span></span>

<span data-ttu-id="c0a0a-134">Alle Container, die die **IABContainer::CreateEntry-Methode** unterstützen, müssen veränderbar sein.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="c0a0a-135">Legen Sie das AB_MODIFIABLE des Containers in der **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) -Eigenschaft fest, um anzugeben, dass es veränderbar ist.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="c0a0a-136">Sie sollten alle  _ulCreateFlags-Flags_ unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="c0a0a-137">Die Interpretation und Verwendung dieser Flags ist jedoch implementierungsspezifisch, d. h. Sie können bestimmen, was die Semantik von CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT im Kontext Ihrer Implementierung bedeutet.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="c0a0a-138">Wenn Sie nicht ermitteln können oder nicht, ob es sich bei einem Eintrag um ein Duplikat handelt, lassen Sie immer zu, dass der Eintrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="c0a0a-139">Einige Anbieter implementieren eine strenge Eintragsprüfung, indem sie den Anzeigenamen, die Messagingadresse und den Suchschlüssel in einem Eintrag abgleichen. Andere Anbieter beschränken die Übereinstimmung auf den Anzeigenamen und die Adresse.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="c0a0a-140">Die Überprüfung der losen Eingabe wird häufig implementiert, indem nur der Anzeigename überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="c0a0a-141">Hinweise zum Hosten von Adressbuchanbieter-Implementierern</span><span class="sxs-lookup"><span data-stu-id="c0a0a-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="c0a0a-142">Wenn Ihr Container Einträge aus den Vorlagen anderer Anbieter erstellen kann, sollte Ihre Implementierung von **CreateEntry** Speicher für einige oder alle Eigenschaften bereitstellen, die den erstellten Einträgen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="c0a0a-143">Wenn Sie beispielsweise Speicher für die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft eines Eintrags bereitstellen, können Sie das Dialogfeld Details generieren, ohne vom fremden Anbieter abhängig zu sein.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="c0a0a-144">Wenn Ihr Container Einträge erstellen **kann,** die die PR_TEMPLATEID ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) -Eigenschaft unterstützen, muss Ihre Implementierung von **CreateEntry** die folgenden Schritte tun:</span><span class="sxs-lookup"><span data-stu-id="c0a0a-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="c0a0a-145">Rufen Sie [die IMAPISupport::OpenTemplateID-Methode](imapisupport-opentemplateid.md) auf.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="c0a0a-146">**Mit OpenTemplateID** kann der Code des fremden Anbieters für den Eintrag an den zu erstellenden neuen Eintrag gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="c0a0a-147">Fremde Anbieter unterstützen diesen Bindungsprozess, um die Kontrolle über Einträge zu behalten, die aus ihren Vorlagen in den Containern von Host-Adressbuchanbietern erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="c0a0a-148">Führen Sie alle erforderlichen Initialisierungen durch, und füllen Sie das neue Objekt mit allen Eigenschaften aus dem Eintrag im fremden Anbieter auf, den das Objekt im  _lppMAPIPropNew-Parameter_ von **OpenTemplateID** zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="c0a0a-149">Wenn **OpenTemplateID** erfolgreich ist, kopieren Sie die Eigenschaften in die Implementierung, auf die der  _lppMAPIPropNew-Parameter_ verweist, anstatt direkt auf die Implementierung zu verweist, auf die der  _lpMAPIPropData-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="c0a0a-150">Initialisieren Sie den neuen Eintrag für die Offlineverwendung, wie bei jedem anderen Eintrag von einem fremden Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="c0a0a-151">Wenn **OpenTemplateID** einen Fehler zurückgibt, **sollte CreateEntry** fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="c0a0a-152">Lassen Sie das Erstellen des Eintrags nicht zu.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="c0a0a-153">Da der fremde Anbieter Annahmen zu den Daten in Ihrem Anbieter treffen kann, erstellen Sie keinen Eintrag mit einem Vorlagenbezeichner, der nicht erfolgreich an den fremden Anbieter gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c0a0a-154">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c0a0a-154">Notes to callers</span></span>

<span data-ttu-id="c0a0a-155">Wenn **CreateEntry zurückgegeben** wird, können Sie möglicherweise nicht sofort auf die Eintrags-ID für den neuen Eintrag zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="c0a0a-156">Einige Adressbuchanbieter stellen sie erst zur Verfügung, nachdem Sie die [IMAPIProp::SaveChanges-Methode des](imapiprop-savechanges.md) neuen Eintrags aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="c0a0a-157">Obwohl doppelte Überprüfungskennzeichen als Parameter an **CreateEntry** übergeben werden, tritt der Doppelte Überprüfungsvorgang erst auf, wenn **SaveChanges** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c0a0a-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="c0a0a-158">Daher werden verwandte Fehler wie MAPI_E_COLLISION, die angeben, dass versucht wurde, einen bereits vorhandenen Eintrag zu erstellen, von **SaveChanges** anstelle von **CreateEntry zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="c0a0a-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0a0a-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0a0a-159">See also</span></span>



[<span data-ttu-id="c0a0a-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="c0a0a-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="c0a0a-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="c0a0a-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="c0a0a-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c0a0a-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c0a0a-163">PidTagCreateTemplates (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c0a0a-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="c0a0a-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c0a0a-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

