---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 81f35f659342d6258d60f40b12bd0a3ac2dc20b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588475"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="77ad5-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="77ad5-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="77ad5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77ad5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77ad5-105">Führt die Auflösung für einen oder mehrere Empfänger Einträge.</span><span class="sxs-lookup"><span data-stu-id="77ad5-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="77ad5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="77ad5-106">Parameters</span></span>

 <span data-ttu-id="77ad5-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="77ad5-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="77ad5-108">[in] Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags, beschreibt die Eigenschaften, die vom Anbieter zurückgegebenen [ADRLIST](adrlist.md) -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="77ad5-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="77ad5-109">Um die Standardeigenschaften des Anbieters anzufordern, übergeben Sie NULL in der _LpPropTagArray_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="77ad5-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="77ad5-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="77ad5-110">_ulFlags_</span></span>
  
> <span data-ttu-id="77ad5-111">[in] Eine Bitmaske aus Flags, die den Typ des Texts in der zurückgegebenen Zeichenfolge steuert.</span><span class="sxs-lookup"><span data-stu-id="77ad5-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="77ad5-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="77ad5-112">The following flags can be set:</span></span>
    
<span data-ttu-id="77ad5-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="77ad5-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="77ad5-114">Nur genauen Proxy Adresse Übereinstimmungen werden gefunden werden. teilweise übereinstimmenden werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="77ad5-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="77ad5-115">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="77ad5-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="77ad5-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="77ad5-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="77ad5-117">Nur das Offlineadressbuch wird zum Ausführen von namensauflösung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77ad5-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="77ad5-118">Dieses Kennzeichen können Sie beispielsweise Hilfe eine Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77ad5-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="77ad5-119">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="77ad5-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="77ad5-120">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="77ad5-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="77ad5-121">Die zurückgegebene Zeichenfolgeneigenschaften sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="77ad5-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="77ad5-122">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="77ad5-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="77ad5-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="77ad5-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="77ad5-124">[in, out] Bei der Eingabe einen Zeiger auf eine **ADRLIST** -Struktur, die enthält die Liste der Empfänger aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="77ad5-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="77ad5-125">Bei der Ausgabe einen Zeiger auf eine **ADRLIST** -Struktur, die aufgelösten Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="77ad5-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="77ad5-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="77ad5-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="77ad5-127">[in, out] Ein Zeiger auf ein Array von Flags, enthält jedes Flag auf eine [ADRENTRY](adrentry.md) -Struktur in den _LpAdrList_ -Parameter entspricht, die den Status des Vorgangs Lösung Name für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="77ad5-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="77ad5-128">Die Flags in der _LpFlagList_ -Parameter werden in der gleichen Reihenfolge in _LpAdrList_als Einträge.</span><span class="sxs-lookup"><span data-stu-id="77ad5-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="77ad5-129">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="77ad5-129">The following flags can be set:</span></span>
    
<span data-ttu-id="77ad5-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="77ad5-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="77ad5-131">Der entsprechende Empfänger aufgelöst wurde, jedoch nicht für einen Eintrag Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="77ad5-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="77ad5-132">Andere Container sollte nicht an diesen Empfänger zu beheben versuchen.</span><span class="sxs-lookup"><span data-stu-id="77ad5-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="77ad5-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="77ad5-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="77ad5-134">Der entsprechende Empfänger wurde eine eindeutige Bezeichner behoben.</span><span class="sxs-lookup"><span data-stu-id="77ad5-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="77ad5-135">Andere Container sollte nicht an diesen Empfänger zu beheben versuchen.</span><span class="sxs-lookup"><span data-stu-id="77ad5-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="77ad5-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="77ad5-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="77ad5-137">Der entsprechende Eintrag wurde nicht behoben.</span><span class="sxs-lookup"><span data-stu-id="77ad5-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="77ad5-138">Andere Container sollte versuchen, diese Empfänger aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="77ad5-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="77ad5-139">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="77ad5-139">Return value</span></span>

<span data-ttu-id="77ad5-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="77ad5-140">S_OK</span></span> 
  
> <span data-ttu-id="77ad5-141">Vorgang der Lösung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="77ad5-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="77ad5-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="77ad5-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="77ad5-143">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="77ad5-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="77ad5-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="77ad5-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="77ad5-145">Der Adressbuchanbieter unterstützt keine namensauflösung Massen mithilfe dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="77ad5-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77ad5-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77ad5-146">Remarks</span></span>

<span data-ttu-id="77ad5-147">Die **ResolveNames** -Methode versucht, nicht aufgelösten Empfänger aus dem Array der Einträge in der _LpAdrList_ -Parameter an Empfänger in dieser Adressbuchcontainer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="77ad5-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="77ad5-148">Ein nicht aufgelöster Empfänger hat in der Regel nur die Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und möglicherweise einigen andere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="77ad5-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="77ad5-149">Ein nicht aufgelöster Empfänger verfügt nicht über die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft, und die entsprechenden Flag im Parameter _LpFlagList_ auf MAPI_UNRESOLVED festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="77ad5-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="77ad5-150">Umgekehrt wurde ein aufgelöster Empfänger immer mindestens die **PR_ENTRYID** -Eigenschaft sowie einige andere Eigenschaften wie **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**und **PR_ADDRTYPE** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="77ad5-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="77ad5-151">Namensauflösung beginnt in der Regel auf, wenn ein Client die [IAddrBook::ResolveName](iaddrbook-resolvename.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="77ad5-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="77ad5-152">Outlook MAPI antwortet durch Aufrufen der Methode **ResolveNames** jedes Adressbuchcontainer enthalten im Address Book Suchpfad, durch die **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="77ad5-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="77ad5-153">Die Einträge in der _LpAdrList_ -Parameter enthalten Empfänger bereits aufgelöst werden, da sie in Containern, die für die MAPI **ResolveNames**, bereits aufgerufen wurde sind, da die Einträge weiter oben in der Suchpfad angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="77ad5-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="77ad5-154">Jeden Container versucht, die nicht aufgelösten Einträge aufzulösen, durch den Anzeigenamen des Empfängers mit dem Anzeigenamen eines der zugehörigen Einträge abgleichen.</span><span class="sxs-lookup"><span data-stu-id="77ad5-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="77ad5-155">Wenn eine eindeutige Übereinstimmung gefunden wird, fügt **ResolveNames** die **PR_ENTRYID** -Eigenschaft und andere Eigenschaften, die im Parameter _LpPropTagArray_ für den entsprechenden Eintrag in der ausgehenden **ADRLIST** -Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="77ad5-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="77ad5-156">Klicken Sie dann der **ResolveNames** Eintrag im Parameter _LpFlagList_ für MAPI_RESOLVED festgelegt.</span><span class="sxs-lookup"><span data-stu-id="77ad5-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="77ad5-157">Die Eintrags-ID in der Eigenschaft **PR_ENTRYID** gespeicherten möglich kurzfristige oder langfristige.</span><span class="sxs-lookup"><span data-stu-id="77ad5-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="77ad5-158">Nachdem alle der Container in der Suche Pfad haben versucht Vorgang der Lösung, MAPI öffnet ein Dialogfeld, wenn möglich, um den Benutzer Hilfe zum Lösen von Konflikten verbleibenden aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="77ad5-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="77ad5-159">Clients können auch die zurückgegebene **ADRLIST** -Struktur in Aufrufe der [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="77ad5-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="77ad5-160">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="77ad5-160">Notes to implementers</span></span>

<span data-ttu-id="77ad5-161">Sie sind nicht erforderlich, zur Unterstützung von namensauflösung mit der **ResolveNames** -Methode.</span><span class="sxs-lookup"><span data-stu-id="77ad5-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="77ad5-162">Stattdessen oder darüber hinaus können Sie es mit der eigenschaftseinschränkung **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="77ad5-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="77ad5-163">Wenn Sie sich entscheiden, auf die Einschränkung **PR_ANR** für namensauflösung verlassen, können Sie MAPI_E_NO_SUPPORT zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="77ad5-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="77ad5-164">For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="77ad5-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="77ad5-165">Legen Sie einen Empfänger Flag Eintrag im Parameter _LpFlagList_ für MAPI_UNRESOLVED, wenn der Empfänger nicht der Empfänger des Containers übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="77ad5-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="77ad5-166">Wenn ein Empfänger mehrere Empfänger übereinstimmt, legen Sie dessen Flag auf MAPI_AMBIGUOUS und ändern Sie die Struktur **ADRENTRY** nicht.</span><span class="sxs-lookup"><span data-stu-id="77ad5-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="77ad5-167">MAPI erfordert bestimmte Eigenschaften für den Empfänger an, die in der Liste der Empfänger einer Nachricht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="77ad5-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="77ad5-168">Sie können in der Struktur **ADRENTRY** einbinden, im Rahmen des Prozesses Lösung Name oder warten MAPI, um sie mit der Aufrufe der Methoden [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) und [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) anfordern.</span><span class="sxs-lookup"><span data-stu-id="77ad5-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="77ad5-169">Sie können diese zusätzlichen Aufrufe vermeiden und Verbessern der Leistung durch die folgenden Eigenschaften in die Strukturen **ADRENTRY** aller aufgelösten Empfänger einschließlich:</span><span class="sxs-lookup"><span data-stu-id="77ad5-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="77ad5-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="77ad5-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="77ad5-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="77ad5-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="77ad5-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="77ad5-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="77ad5-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="77ad5-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="77ad5-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="77ad5-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="77ad5-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="77ad5-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="77ad5-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="77ad5-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="77ad5-177">Wenn einige der Eigenschaften im _LpPropTagArray_ -Parameter nicht verfügbar sind – in der Regel, da der Container-Eintrag nicht unterstützt, und sie die Eigenschaften sind nicht enthalten in der Aufgabenliste des Empfängers **ADRENTRY** Member in der Struktur **ADRLIST** – Legen Sie den Eigenschaftstyp der einzelnen nicht verfügbar-Eigenschaft auf PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="77ad5-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="77ad5-178">Entfernen Sie alle Eigenschaften nicht aus einer aufgelösten Empfänger **ADRENTRY** Struktur.</span><span class="sxs-lookup"><span data-stu-id="77ad5-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="77ad5-179">Wenn Sie müssen ersetzen, anstatt eine **ADRENTRY** -Struktur zu ändern, die ursprüngliche **ADRENTRY** Struktur zuerst durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion frei, und fügen dann die Ersetzung **ADRENTRY** Struktur mit [ MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="77ad5-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="77ad5-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77ad5-180">See also</span></span>



[<span data-ttu-id="77ad5-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="77ad5-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="77ad5-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="77ad5-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="77ad5-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="77ad5-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="77ad5-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="77ad5-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="77ad5-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="77ad5-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="77ad5-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="77ad5-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="77ad5-187">PidTagAnr (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="77ad5-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="77ad5-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="77ad5-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="77ad5-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="77ad5-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

