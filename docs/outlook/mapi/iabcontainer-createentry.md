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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287028"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="ab7f5-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="ab7f5-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="ab7f5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab7f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab7f5-105">Erstellt einen neuen Eintrag, bei dem es sich um einen Messagingbenutzer, eine Verteilerliste oder einen anderen Container handeln kann.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="ab7f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab7f5-106">Parameters</span></span>

 <span data-ttu-id="ab7f5-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ab7f5-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ab7f5-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ab7f5-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ab7f5-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ab7f5-110">in Ein Zeiger auf den Eintragsbezeichner einer Vorlage zum Erstellen neuer Einträge eines bestimmten Typs.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="ab7f5-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="ab7f5-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="ab7f5-112">in Eine Bitmaske von Flags, die die Ausführung der Eintragserstellung steuert.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="ab7f5-113">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ab7f5-113">The following flags can be set:</span></span>
    
<span data-ttu-id="ab7f5-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="ab7f5-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="ab7f5-115">Es sollte eine Ebene doppelter Eintrags Überprüfung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="ab7f5-116">Die Implementierung von Loose Duplicate entry checking ist Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="ab7f5-117">Ein Anbieter kann beispielsweise eine lockere Übereinstimmung als zwei Einträge definieren, die den gleichen Anzeigenamen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="ab7f5-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="ab7f5-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="ab7f5-119">Es sollte eine strenge doppelte Eintrags Überprüfung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="ab7f5-120">Die Implementierung einer strengen doppelten Eintrags Überprüfung ist Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="ab7f5-121">Ein Anbieter kann beispielsweise eine strikte Übereinstimmung als zwei Einträge definieren, die den gleichen Anzeigenamen und die gleiche Messaging Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="ab7f5-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="ab7f5-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="ab7f5-123">Ein neuer Eintrag sollte ein vorhandenes ersetzen, wenn festgestellt wird, dass die beiden Duplikate sind.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="ab7f5-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="ab7f5-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="ab7f5-125">Out Ein Zeiger auf einen Zeiger auf den neu erstellten Eintrag.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ab7f5-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab7f5-126">Return value</span></span>

<span data-ttu-id="ab7f5-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab7f5-127">S_OK</span></span> 
  
> <span data-ttu-id="ab7f5-128">Der neue Eintrag wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab7f5-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab7f5-129">Remarks</span></span>

<span data-ttu-id="ab7f5-130">Die **IABContainer:: CreateEntry** -Methode erstellt einen neuen Eintrag eines bestimmten Typs im angegebenen Container und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, um weiteren Zugriff auf den Eintrag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="ab7f5-131">Der neue Eintrag wird mithilfe einer Vorlage erstellt, die aus der Liste der verfügbaren Vorlagen des Containers ausgewählt wurde, die in der einmaligen Tabelle veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="ab7f5-132">Aufrufer greifen auf die einmalige Tabelle eines Containers zu, indem Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode aufrufen und die **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft anfordern.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ab7f5-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="ab7f5-133">Notes to implementers</span></span>

<span data-ttu-id="ab7f5-134">Alle Container, die die **IABContainer:: CreateEntry** -Methode unterstützen, müssen geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="ab7f5-135">Legen Sie das AB_MODIFIABLE-Flag ihres Containers in seiner **PR_CONTAINER_FLAGS** ([pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))-Eigenschaft fest, um anzugeben, dass es veränderbar ist.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="ab7f5-136">Sie sollten alle _ulCreateFlags_ -Flags unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="ab7f5-137">Die Interpretation und Verwendung dieser Flags ist jedoch implementierungsspezifisch, d. h., Sie können bestimmen, welche Semantik von CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT im Kontext ihrer Implementierung bedeuten.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="ab7f5-138">Wenn Sie nicht oder nicht feststellen können, ob ein Eintrag ein Duplikat ist, dürfen Sie immer den Eintrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="ab7f5-139">Einige Anbieter implementieren strenge Eingabeprüfungen, indem Sie den Anzeigenamen, die Messaging Adresse und den Suchschlüssel in einem Eintrag vergleichen. andere Anbieter begrenzen die Übereinstimmung auf Anzeigename und-Adresse.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="ab7f5-140">Die Überprüfung des losen Eintrags wird häufig durch Überprüfen des Anzeigenamens implementiert.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="ab7f5-141">Hinweise für Host-Adressbuchanbieter-Implementierer</span><span class="sxs-lookup"><span data-stu-id="ab7f5-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="ab7f5-142">Wenn Ihr Container Einträge aus den Vorlagen anderer Anbieter erstellen kann, sollte Ihre Implementierung von **CreateEntry** Speicher für einige oder alle Eigenschaften bereitstellen, die den erstellten Einträgen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="ab7f5-143">Wenn Sie beispielsweise Speicher für die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft eines Eintrags bereitstellen, können Sie das Dialogfeld Details generieren, ohne vom fremden Anbieter abhängig zu sein.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="ab7f5-144">Wenn der Container Einträge erstellen kann, die die **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft unterstützen, \*\*\*\* muss die Implementierung von CreateEntry wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="ab7f5-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="ab7f5-145">Rufen Sie die [IMAPISupport::](imapisupport-opentemplateid.md) opentemplatecode-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="ab7f5-146">\*\*\*\* Opentemplateable aktiviert den Code des fremden Anbieters für den Eintrag, um eine Bindung an den neuen Eintrag zu erstellen, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="ab7f5-147">Ausländische Anbieter unterstützen diesen Bindungsprozess, um die Kontrolle über Einträge, die aus ihren Vorlagen erstellt wurden, in die Container von Host Adressbuch Anbietern zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="ab7f5-148">Führen Sie alle erforderlichen Initialisierungen aus, und füllen Sie das neue Objekt mit allen Eigenschaften aus dem Eintrag im fremden Anbieter, den das Objekt im _lppMAPIPropNew_ -Parameter \*\*\*\* von opentemplatecollection zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="ab7f5-149">Wenn \*\*\*\* opentemplatename erfolgreich ist, kopieren Sie die Eigenschaften in die Implementierung, auf die durch den _lppMAPIPropNew_ -Parameter verwiesen wird, statt direkt auf die Implementierung, auf die durch den _lpMAPIPropData_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="ab7f5-150">Initialisieren Sie den neuen Eintrag für die Offlineverwendung wie jeder andere Eintrag eines fremden Anbieters.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="ab7f5-151">Wenn \*\*\*\* opentemplatecollection einen Fehler zurückgibt, sollte CreateEntry fehlschlagen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ab7f5-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="ab7f5-152">Lassen Sie den Eintrag nicht erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="ab7f5-153">Da der fremde Anbieter Annahmen über die Daten in Ihrem Anbieter treffen kann, erstellen Sie keinen Eintrag mit einem Vorlagenbezeichner, der nicht erfolgreich an den fremden Anbieter gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ab7f5-154">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ab7f5-154">Notes to callers</span></span>

<span data-ttu-id="ab7f5-155">Wenn **CreateEntry** zurückgegeben wird, können Sie möglicherweise nicht sofort auf die Eintrags-ID für den neuen Eintrag zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="ab7f5-156">Einige Adressbuchanbieter stellen Sie erst dann zur Verfügung, wenn Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode des neuen Eintrags aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="ab7f5-157">Obwohl doppelt überprüfende Kennzeichnungen als Parameter \*\*\*\* an CreateEntry übergeben werden, tritt der Vorgang der doppelten Überprüfung erst auf, wenn **SaveChanges** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ab7f5-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="ab7f5-158">Daher werden verwandte Fehler wie MAPI_E_COLLISION, die darauf hindeuten, dass ein Versuch unternommen wurde, einen bereits vorhandenen Eintrag zu erstellen, \*\*\*\* von SaveChanges anstelle von CreateEntry zurückgegeben. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ab7f5-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ab7f5-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab7f5-159">See also</span></span>



[<span data-ttu-id="ab7f5-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="ab7f5-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="ab7f5-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="ab7f5-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="ab7f5-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="ab7f5-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="ab7f5-163">Kanonische Pidtagcreatetemplates (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ab7f5-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="ab7f5-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ab7f5-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

