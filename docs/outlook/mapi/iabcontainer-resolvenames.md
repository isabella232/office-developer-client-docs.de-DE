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
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405814"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="ca76b-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="ca76b-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="ca76b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca76b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca76b-105">Führt die Namensauflösung für einen oder mehrere Empfänger Einträge aus.</span><span class="sxs-lookup"><span data-stu-id="ca76b-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="ca76b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca76b-106">Parameters</span></span>

 <span data-ttu-id="ca76b-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="ca76b-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="ca76b-108">in Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält, die die Eigenschaften beschreiben, die in die vom Anbieter zurückgegebene [ADRLIST](adrlist.md) -Struktur eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ca76b-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="ca76b-109">Um den Standardsatz von Eigenschaften des Anbieters anzufordern, übergeben Sie NULL im _lpPropTagArray_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="ca76b-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="ca76b-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ca76b-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ca76b-111">in Eine Bitmaske von Flags, die den Texttyp in den zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="ca76b-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="ca76b-112">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ca76b-112">The following flags can be set:</span></span>
    
<span data-ttu-id="ca76b-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="ca76b-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="ca76b-114">Nur genaue Proxyadressen Übereinstimmungen werden gefunden; partielle Übereinstimmungen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ca76b-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="ca76b-115">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ca76b-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="ca76b-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="ca76b-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="ca76b-117">Nur das Offlineadressbuch wird zur Durchführung der Namensauflösung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca76b-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="ca76b-118">Sie können dieses Flag beispielsweise verwenden, um eine Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus zu aktivieren und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca76b-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="ca76b-119">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ca76b-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="ca76b-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ca76b-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ca76b-121">Die zurückgegebenen Zeichenfolgeneigenschaften sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="ca76b-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="ca76b-122">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="ca76b-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ca76b-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="ca76b-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="ca76b-124">[in, out] Bei der Eingabe ein Zeiger auf eine **ADRLIST** -Struktur, die die Liste der zu lösenden Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="ca76b-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="ca76b-125">Bei der Ausgabe ein Zeiger auf eine **ADRLIST** -Struktur, die die aufgelösten Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="ca76b-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="ca76b-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="ca76b-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="ca76b-127">[in, out] Ein Zeiger auf ein Array von Flags, jedes Flag, das einer [](adrentry.md) anmietungs Struktur im _lpAdrList_ -Parameter entspricht, die den Status der Namensauflösung für den Empfänger bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ca76b-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="ca76b-128">Die Flags im _lpFlagList_ -Parameter befinden sich in der gleichen Reihenfolge wie die Einträge in _lpAdrList_.</span><span class="sxs-lookup"><span data-stu-id="ca76b-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="ca76b-129">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ca76b-129">The following flags can be set:</span></span>
    
<span data-ttu-id="ca76b-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="ca76b-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="ca76b-131">Der entsprechende Empfänger wurde aufgelöst, jedoch nicht zu einer eindeutigen Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="ca76b-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="ca76b-132">Andere Container sollten nicht versuchen, diesen Empfänger aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="ca76b-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="ca76b-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="ca76b-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="ca76b-134">Der entsprechende Empfänger wurde in eine eindeutige Eintrags-ID aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="ca76b-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="ca76b-135">Andere Container sollten nicht versuchen, diesen Empfänger aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="ca76b-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="ca76b-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="ca76b-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="ca76b-137">Der entsprechende Eintrag wurde nicht aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="ca76b-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="ca76b-138">Andere Container sollten versuchen, diesen Empfänger aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="ca76b-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca76b-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca76b-139">Return value</span></span>

<span data-ttu-id="ca76b-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca76b-140">S_OK</span></span> 
  
> <span data-ttu-id="ca76b-141">Der Prozess der Namensauflösung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ca76b-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="ca76b-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ca76b-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ca76b-143">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="ca76b-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="ca76b-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ca76b-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ca76b-145">Der Adressbuchanbieter unterstützt die Auflösung von Massen Namen nicht mithilfe dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="ca76b-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca76b-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca76b-146">Remarks</span></span>

<span data-ttu-id="ca76b-147">Die **ResolveNames** -Methode versucht, nicht aufgelöste Empfänger aus dem Array der Einträge im _lpAdrList_ -Parameter an Empfänger in diesem Adressbuchcontainer anzupassen.</span><span class="sxs-lookup"><span data-stu-id="ca76b-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="ca76b-148">Ein nicht aufgelöster Empfänger hat in der Regel nur die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft und möglicherweise einige andere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ca76b-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="ca76b-149">Ein nicht aufgelöster Empfänger verfügt nicht über die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft, und das entsprechende Flag im _LPFLAGLIST_ -Parameter ist auf MAPI_UNRESOLVED festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ca76b-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="ca76b-150">Umgekehrt hat ein aufgelöster Empfänger immer mindestens die **PR_ENTRYID** -Eigenschaft und mehrere andere Eigenschaften wie **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**und **PR_ADDRTYPE** ([ Pidtagaddresstype (](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ca76b-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="ca76b-151">Die Namensauflösung wird in der Regel gestartet, wenn ein Client die [IAddrBook::](iaddrbook-resolvename.md) ResolveName-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="ca76b-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="ca76b-152">Outlook MAPI antwortet durch Aufrufen der **ResolveNames** -Methode jedes Adressbuch Containers, der im Adressbuch Suchpfad enthalten ist, angegeben durch die **PR_AB_SEARCH_PATH** ([pidtagabsearchpath (](pidtagabsearchpath-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ca76b-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="ca76b-153">Die Einträge im _lpAdrList_ -Parameter enthalten bereits aufgelöste Empfänger, da Sie sich in Containern befinden, für die MAPI bereits **ResolveNames**aufgerufen hat, da die Einträge weiter oben im Suchpfad angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ca76b-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="ca76b-154">Jeder Container versucht, die nicht aufgelösten Einträge aufzulösen, indem der Anzeigename des Empfängers mit dem Anzeigenamen eines seiner Einträge abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="ca76b-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="ca76b-155">Wenn eine eindeutige Übereinstimmung gefunden wird, fügt **ResolveNames** die **PR_ENTRYID** -Eigenschaft und andere Eigenschaften, die im _lpPropTagArray_ -Parameter enthalten sind, dem entsprechenden Eintrag in der ausgehenden **ADRLIST** -Struktur hinzu.</span><span class="sxs-lookup"><span data-stu-id="ca76b-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="ca76b-156">**ResolveNames** legt dann den Eintrag im _lpFlagList_ -Parameter auf MAPI_RESOLVED fest.</span><span class="sxs-lookup"><span data-stu-id="ca76b-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="ca76b-157">Die in der **PR_ENTRYID** -Eigenschaft gespeicherte Eintrags-ID kann kurzfristig oder langfristig sein.</span><span class="sxs-lookup"><span data-stu-id="ca76b-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="ca76b-158">Nachdem alle Container im Suchpfad den Prozess der Namensauflösung versucht haben, öffnet MAPI ein Dialogfeld, um den Benutzer aufzufordern, Hilfe beim Beheben von verbleibenden Konflikten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ca76b-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="ca76b-159">Clients können die zurückgegebene **ADRLIST** -Struktur auch in Aufrufen der [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca76b-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ca76b-160">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="ca76b-160">Notes to implementers</span></span>

<span data-ttu-id="ca76b-161">Sie müssen die Namensauflösung nicht mit der **ResolveNames** -Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ca76b-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="ca76b-162">Stattdessen oder zusätzlich können Sie diese mit der **PR_ANR** ([pidtaganr (](pidtaganr-canonical-property.md))-Eigenschaftseinschränkung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ca76b-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="ca76b-163">Wenn Sie sich dafür entscheiden, die **PR_ANR** -Einschränkung für die Namensauflösung zu verwenden, können Sie MAPI_E_NO_SUPPORT zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ca76b-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="ca76b-164">For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="ca76b-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="ca76b-165">Legen Sie den Flag-Eintrag eines Empfängers im _lpFlagList_ -Parameter auf MAPI_UNRESOLVED fest, wenn der Empfänger keinem der Empfänger des Containers entspricht.</span><span class="sxs-lookup"><span data-stu-id="ca76b-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="ca76b-166">Wenn ein Empfänger mit mehreren Empfängern übereinstimmt, legen Sie sein Flag auf MAPI_AMBIGUOUS, und ändern Sie die zugehörige **Miet** Struktur nicht.</span><span class="sxs-lookup"><span data-stu-id="ca76b-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="ca76b-167">MAPI erfordert bestimmte Eigenschaften für Empfänger, die in der Empfängerliste einer Nachricht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ca76b-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="ca76b-168">Sie können Sie als Teil des Namens Auflösungsprozesses in die **Miet** Struktur aufnehmen oder warten, bis MAPI Sie mit Aufrufen der Methoden [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) und [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md) anfordert.</span><span class="sxs-lookup"><span data-stu-id="ca76b-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="ca76b-169">Sie können diese zusätzlichen Anrufe beseitigen und die Leistung verbessern, indem Sie die folgenden Eigenschaften in die **Miet** Strukturen aller aufgelösten Empfänger einbeziehen:</span><span class="sxs-lookup"><span data-stu-id="ca76b-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="ca76b-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="ca76b-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="ca76b-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="ca76b-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="ca76b-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="ca76b-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="ca76b-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="ca76b-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="ca76b-174">**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ca76b-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="ca76b-175">**PR_SEARCH_KEY** ([Pidtagsearchkey (](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ca76b-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="ca76b-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([Pidtagtransmittabledisplayname (](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ca76b-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="ca76b-177">Wenn einige der Eigenschaften im _lpPropTagArray_ -Parameter nicht verfügbar sind (in der Regel, da der Container Eintrag die Eigenschaften nicht unterstützt und Sie nicht in der **ADRLIST** - \*\*\*\* Struktur des Empfängers enthalten sind) Legen Sie den Eigenschaftentyp jeder nicht verfügbaren Eigenschaft auf PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="ca76b-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="ca76b-178">Entfernen Sie keine Eigenschaften aus der **Miet** Struktur eines aufgelösten Empfängers.</span><span class="sxs-lookup"><span data-stu-id="ca76b-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="ca76b-179">Wenn Sie eine **Miet** Struktur ersetzen und nicht ändern müssen, können Sie zuerst die ursprüngliche **Miet** Struktur freigeben, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen und dann die Ersatz- **Miet** Struktur mit [ MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ca76b-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ca76b-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca76b-180">See also</span></span>



[<span data-ttu-id="ca76b-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="ca76b-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="ca76b-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="ca76b-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="ca76b-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="ca76b-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="ca76b-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="ca76b-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="ca76b-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="ca76b-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="ca76b-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="ca76b-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="ca76b-187">Kanonische Pidtaganr (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ca76b-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="ca76b-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="ca76b-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="ca76b-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ca76b-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

