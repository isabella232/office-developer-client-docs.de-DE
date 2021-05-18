---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408131"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="1c769-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="1c769-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="1c769-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c769-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c769-105">Führt die Namensauflösung durch und weist Empfängern in einer Empfängerliste Eintragsbezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="1c769-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="1c769-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c769-106">Parameters</span></span>

 <span data-ttu-id="1c769-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1c769-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1c769-108">[in] Ein Handle zum übergeordneten Fenster eines Dialogfelds, das angezeigt wird, falls angegeben, um den Benutzer zur Lösung von Mehrdeutigkeiten aufforderen.</span><span class="sxs-lookup"><span data-stu-id="1c769-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="1c769-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1c769-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1c769-110">[in] Eine Bitmaske mit Flags, die verschiedene Aspekte des Auflösungsprozesses steuern.</span><span class="sxs-lookup"><span data-stu-id="1c769-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="1c769-111">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1c769-111">The following flags can be set:</span></span>
    
<span data-ttu-id="1c769-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="1c769-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="1c769-113">Gibt an,  _dass lpszNewEntryTitle eine_ UNICODE-Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="1c769-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="1c769-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="1c769-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="1c769-115">Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="1c769-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="1c769-116">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung zu ermöglichen, die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und aus dem Cache auf einen Eintrag in diesem Adressbuch zu zugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c769-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="1c769-117">Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c769-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="1c769-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1c769-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="1c769-119">Zeigt ein Dialogfeld an, in dem der Benutzer weitere Informationen zur Namensauflösung einfordert.</span><span class="sxs-lookup"><span data-stu-id="1c769-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="1c769-120">Wenn dieses Kennzeichen nicht festgelegt ist, wird kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c769-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="1c769-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1c769-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1c769-122">Gibt an, dass die in der Adressliste zurückgegebenen Eigenschaften vom Typ PT_UNICODE anstatt PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="1c769-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="1c769-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="1c769-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="1c769-124">[in] Ein Zeiger auf Text für den Titel des Steuerelements im Dialogfeld, mit dem der Benutzer zur Eingabe eines Empfängers aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="1c769-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="1c769-125">Der Titel variiert je nach Empfängertyp.</span><span class="sxs-lookup"><span data-stu-id="1c769-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="1c769-126">Der  _lpszNewEntryTitle-Parameter_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1c769-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="1c769-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="1c769-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="1c769-128">[in-out] Ein Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die die Liste der empfängernamen enthält, die aufgelöst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1c769-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="1c769-129">Diese **ADRLIST-Struktur** kann mit der [IAddrBook::Address-Methode erstellt](iaddrbook-address.md) werden.</span><span class="sxs-lookup"><span data-stu-id="1c769-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1c769-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c769-130">Return value</span></span>

<span data-ttu-id="1c769-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="1c769-131">S_OK</span></span> 
  
> <span data-ttu-id="1c769-132">Der Namensauflösungsprozess ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1c769-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="1c769-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="1c769-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="1c769-134">Mindestens ein Empfänger im  _lpAdrList-Parameter_ hat mehreren Eintrag im Adressbuch entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1c769-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="1c769-135">In der Regel wird dieser Wert zurückgegeben, wenn MAPI_DIALOG festgelegt ist, was die Anzeige eines Dialogfelds verhindert.</span><span class="sxs-lookup"><span data-stu-id="1c769-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="1c769-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1c769-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1c769-137">Mindestens ein Empfänger im  _lpAdrList-Parameter_ kann nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="1c769-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="1c769-138">In der Regel wird dieser Wert zurückgegeben, wenn MAPI_DIALOG festgelegt ist, was die Anzeige eines Dialogfelds verhindert.</span><span class="sxs-lookup"><span data-stu-id="1c769-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1c769-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c769-139">Remarks</span></span>

<span data-ttu-id="1c769-140">Clients und Dienstanbieter rufen die **ResolveName-Methode** auf, um den Namensauflösungsprozess zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="1c769-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="1c769-141">Ein nicht aufgelöster Eintrag ist ein Eintrag, der noch keinen Eintragsbezeichner oder keine **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft hat.</span><span class="sxs-lookup"><span data-stu-id="1c769-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="1c769-142">**ResolveName** durchgeht den folgenden Prozess für jeden nicht aufgelösten Eintrag in der Adressliste, der im  _lpAdrList-Parameter übergeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="1c769-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="1c769-143">Wenn der Adresstyp des Empfängers dem Format einer SMTP-Adresse ( _Anzeigename_ @  _domain.top-level-domain)_ zuzuordnen ist, weist **ResolveName** ihm eine eindeutige Eintrags-ID zu.</span><span class="sxs-lookup"><span data-stu-id="1c769-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="1c769-144">Für jeden Container in der **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) -Eigenschaft ruft **ResolveName** die [IABContainer::ResolveNames-Methode](iabcontainer-resolvenames.md) auf.</span><span class="sxs-lookup"><span data-stu-id="1c769-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="1c769-145">**ResolveNames** versucht, dem Anzeigenamen jedes nicht aufgelösten Empfängers einen Anzeigenamen zu geben, der zu einem seiner Einträge gehört.</span><span class="sxs-lookup"><span data-stu-id="1c769-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="1c769-146">Wenn ein Container **ResolveNames** nicht unterstützt, **schränkt ResolveName** die Inhaltstabelle des Containers mithilfe einer **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) -Eigenschaftseinschränkung ein.</span><span class="sxs-lookup"><span data-stu-id="1c769-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="1c769-147">Diese Einschränkung bewirkt, dass der Container eine "best guess"-Suchart zum Suchen eines übereinstimmenden Empfängers durch führt.</span><span class="sxs-lookup"><span data-stu-id="1c769-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="1c769-148">Alle Container müssen die Einschränkung der **PR_ANR** unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1c769-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="1c769-149">Wenn ein Container einen Empfänger zurückgibt, der mehreren Namen entspricht, zeigt **ResolveName** ein Dialogfeld an, wenn das flag MAPI_DIALOG festgelegt ist, wodurch der Benutzer den richtigen Namen auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="1c769-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="1c769-150">Wenn alle Container in der PR_AB_SEARCH_PATH **aufgerufen** wurden und keine Übereinstimmung gefunden wurde, bleibt der Empfänger ungelöst.</span><span class="sxs-lookup"><span data-stu-id="1c769-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="1c769-151">Wenn ein oder mehrere Empfänger nicht aufgelöst werden, gibt **ResolveName** MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="1c769-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="1c769-152">Wenn ein oder mehrere Empfänger eine mehrdeutige Auflösung hatten, die nicht mit einem Dialogfeld aufgelöst werden konnte, oder weil das MAPI_DIALOG-Flag nicht festgelegt wurde, gibt **ResolveName** MAPI_E_AMBIGUOUS_RECIP.</span><span class="sxs-lookup"><span data-stu-id="1c769-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="1c769-153">Wenn einige der Empfänger mehrdeutig sind und einige nicht aufgelöst werden können, kann **ResolveName** einen der Fehlerwerte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1c769-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="1c769-154">Wenn ein Name nicht aufgelöst werden kann, kann der Client eine eindeutige Adresse mit einer speziell formatierten Adresse und einem Eintragsbezeichner erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c769-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="1c769-155">Weitere Informationen zum Format von one-off-Eintragsbezeichnern finden Sie unter [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="1c769-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="1c769-156">Weitere Informationen zum Format von einmal verwendeten Adressen finden Sie unter [One-Off Addresses](one-off-addresses.md).</span><span class="sxs-lookup"><span data-stu-id="1c769-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="1c769-157">MAPI unterstützt Unicode-Zeichenzeichenfolgen für **die ADRLIST** und die neuen Eintragstitelparameter zu **ResolveName**; Wenn Sie das MAPI_UNICODE festlegen, werden die folgenden Eigenschaften als Typ zurückgegeben, PT_UNICODE in den [ADRENTRY-Strukturen](adrentry.md) verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="1c769-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="1c769-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c769-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c769-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c769-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c769-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c769-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c769-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c769-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="1c769-162">Die eigenschaft **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) wird jedoch immer als Typ PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="1c769-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1c769-163">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="1c769-163">MFCMAPI reference</span></span>

<span data-ttu-id="1c769-164">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1c769-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1c769-165">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1c769-165">**File**</span></span>|<span data-ttu-id="1c769-166">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1c769-166">**Function**</span></span>|<span data-ttu-id="1c769-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1c769-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c769-168">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1c769-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1c769-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="1c769-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="1c769-170">MFCMAPI verwendet die **ResolveName-Methode,** um eine einmal festgelegte Adresse zu lösen, bevor sie einer Nachricht hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="1c769-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="1c769-171">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1c769-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1c769-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="1c769-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="1c769-173">MFCMAPI verwendet die **ResolveName-Methode,** um einen Adressbucheintrag nach Anzeigenamen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1c769-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c769-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c769-174">See also</span></span>



[<span data-ttu-id="1c769-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="1c769-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="1c769-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="1c769-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="1c769-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="1c769-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="1c769-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1c769-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="1c769-179">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1c769-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

