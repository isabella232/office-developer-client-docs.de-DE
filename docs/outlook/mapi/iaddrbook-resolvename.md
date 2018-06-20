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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aa72085c4e50fcef1f2d3da81e5409af3d55d89b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791999"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="a8073-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="a8073-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="a8073-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8073-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8073-105">Führt Namensresolution Eintragsbezeichner an Empfänger in der Empfängerliste zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a8073-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="a8073-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8073-106">Parameters</span></span>

 <span data-ttu-id="a8073-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a8073-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a8073-108">[in] Ein Handle für das übergeordnete Fenster des ein Dialogfeld angezeigt wird, wenn angegeben, den Benutzer zum Auflösen der Mehrdeutigkeit,.</span><span class="sxs-lookup"><span data-stu-id="a8073-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="a8073-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8073-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a8073-110">[in] Eine Bitmaske aus Flags, die verschiedene Aspekte des Prozesses Lösung steuern.</span><span class="sxs-lookup"><span data-stu-id="a8073-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="a8073-111">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a8073-111">The following flags can be set:</span></span>
    
<span data-ttu-id="a8073-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="a8073-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="a8073-113">Gibt an, dass diese _LpszNewEntryTitle_ UNICODE-Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="a8073-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="a8073-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="a8073-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="a8073-115">Verwenden Sie nur das Offlineadressbuch, um namensauflösung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a8073-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="a8073-116">Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8073-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="a8073-117">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a8073-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="a8073-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a8073-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a8073-119">Zeigt ein Dialogfeld, um die Aufforderung des Benutzers für zusätzliche Namensinformationen der Lösung an.</span><span class="sxs-lookup"><span data-stu-id="a8073-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="a8073-120">Wenn dieses Flag nicht festgelegt ist, wird kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8073-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="a8073-121">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a8073-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a8073-122">Gibt an, dass die in der Adressliste zurückgegebenen Eigenschaften vom Typ PT_UNICODE anstelle von PT_STRING8 sein sollte.</span><span class="sxs-lookup"><span data-stu-id="a8073-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="a8073-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="a8073-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="a8073-124">[in] Ein Zeiger auf den Text für den Titel des Steuerelements in dem Dialogfeld, das den Benutzer auffordert, einen Empfänger eingeben.</span><span class="sxs-lookup"><span data-stu-id="a8073-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="a8073-125">Der Titel variiert je nach den Typ des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="a8073-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="a8073-126">Der Parameter _LpszNewEntryTitle_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a8073-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a8073-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="a8073-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="a8073-128">[in Out] Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die enthält die Liste der Namen der Empfänger aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="a8073-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="a8073-129">Diese Struktur **ADRLIST** kann von der [IAddrBook::Address](iaddrbook-address.md) -Methode erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a8073-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a8073-130">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a8073-130">Return value</span></span>

<span data-ttu-id="a8073-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8073-131">S_OK</span></span> 
  
> <span data-ttu-id="a8073-132">Vorgang der Lösung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a8073-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="a8073-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="a8073-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="a8073-134">Mindestens ein Empfänger im Parameter _LpAdrList_ abgeglichen mehr als einen Eintrag im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="a8073-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="a8073-135">Dieser Wert wird in der Regel zurückgegeben, wenn das Flag MAPI_DIALOG verhindern der Anzeige eines Dialogfelds festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a8073-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="a8073-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a8073-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a8073-137">Mindestens ein Empfänger in der _LpAdrList_ -Parameter kann nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="a8073-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="a8073-138">Dieser Wert wird in der Regel zurückgegeben, wenn das Flag MAPI_DIALOG verhindern der Anzeige eines Dialogfelds festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a8073-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a8073-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8073-139">Remarks</span></span>

<span data-ttu-id="a8073-140">Clients und Dienstanbieter rufen Sie die **ResolveName** -Methode, um die Namen Lösung zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="a8073-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="a8073-141">Ein nicht aufgelöster Eintrag ist ein Eintrag, der eine Eintrags-ID oder -Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a8073-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="a8073-142">**ResolveName** erfolgt über den folgenden Vorgang für jeden nicht aufgelösten Eintrag in der Adressliste im _LpAdrList_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a8073-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="a8073-143">Wenn das Format der SMTP-Adresse des Empfängers Adresstyp entspricht ( _Displayname_@ _domain.top-Level-Domäne_), **ResolveName** weist ihm einen Eingangs-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a8073-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="a8073-144">Für jeden Container in der Eigenschaft **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) Ruft **ResolveName** die [IABContainer](iabcontainer-resolvenames.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a8073-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="a8073-145">**ResolveNames** versucht, den Anzeigenamen des jeden nicht aufgelösten Empfänger mit dem Anzeigenamen zuzuordnen, die auf eine der zugehörigen Einträge gehört.</span><span class="sxs-lookup"><span data-stu-id="a8073-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="a8073-146">Wenn ein Container **ResolveNames**nicht unterstützt, schränkt **ResolveName** Inhaltstabelle des Containers mithilfe einer eigenschaftseinschränkung **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a8073-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="a8073-147">Diese Einschränkung bewirkt, dass den Container zum Ausführen eines "am besten erraten" Typs der Suche aus, um einen übereinstimmenden Empfänger zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a8073-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="a8073-148">Von allen Containern müssen der **PR_ANR** eigenschaftseinschränkung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a8073-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="a8073-149">Wenn ein Container ein Empfängers, das mehrere Namen entspricht zurückgegeben, im **ResolveName** ein Dialogfeld angezeigt, wenn das Flag MAPI_DIALOG festgelegt ist, dem den Benutzer den gewünschten Namen auswählen können.</span><span class="sxs-lookup"><span data-stu-id="a8073-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="a8073-150">Wenn alle Container in der Eigenschaft **PR_AB_SEARCH_PATH** aufgerufen wurde und keine Übereinstimmung gefunden wurde, bleibt der Empfänger nicht aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="a8073-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="a8073-151">Wenn Sie einen oder mehrere Empfänger nicht aufgelöst werden, gibt **ResolveName** MAPI_E_NOT_FOUND zurück.</span><span class="sxs-lookup"><span data-stu-id="a8073-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="a8073-152">Wenn Sie einen oder mehrere Empfänger war mehrdeutig Lösung, die mit einem Dialogfeld nicht aufgelöst werden konnte, oder da das Flag MAPI_DIALOG nicht festgelegt wurde, **ResolveName** MAPI_E_AMBIGUOUS_RECIP gibt.</span><span class="sxs-lookup"><span data-stu-id="a8073-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="a8073-153">Wenn einige der Empfänger nicht eindeutig sind und einige nicht aufgelöst werden kann, können **ResolveName** entweder Fehlerwert zurück.</span><span class="sxs-lookup"><span data-stu-id="a8073-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="a8073-154">Wenn Sie ein Namen aufgelöst werden kann, kann der Client eine einmalige Adresse erstellen, die ein speziell formatierte Adresse und Eintrags-ID verfügt.</span><span class="sxs-lookup"><span data-stu-id="a8073-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="a8073-155">Weitere Informationen zum Format von Eintragsbezeichner einmaligen finden Sie unter [Einmaligen-Eintragsbezeichner](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="a8073-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="a8073-156">Weitere Informationen zum Format von einmal-Adressen finden Sie unter [Einmal-Adressen](one-off-addresses.md).</span><span class="sxs-lookup"><span data-stu-id="a8073-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="a8073-157">MAPI unterstützt Unicode-Zeichenfolgen für die **ADRLIST** und die neuen Eintrag Titel Parameter **ResolveName**. Wenn Sie die Option MAPI_UNICODE festlegen, werden die folgenden Eigenschaften als Typ PT_UNICODE in die Strukturen [ADRENTRY](adrentry.md) zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="a8073-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="a8073-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a8073-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="a8073-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a8073-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="a8073-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a8073-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="a8073-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a8073-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="a8073-162">Die **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md))-Eigenschaft wird jedoch immer zurückgegeben, PT_STRING8 eingeben.</span><span class="sxs-lookup"><span data-stu-id="a8073-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a8073-163">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="a8073-163">MFCMAPI reference</span></span>

<span data-ttu-id="a8073-164">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a8073-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a8073-165">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a8073-165">**File**</span></span>|<span data-ttu-id="a8073-166">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a8073-166">**Function**</span></span>|<span data-ttu-id="a8073-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a8073-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a8073-168">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a8073-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a8073-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="a8073-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="a8073-170">MFCMAPI (engl.) verwendet die **ResolveName** -Methode, um eine einmal Adresse aufzulösen, vor dem Hinzufügen zu einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a8073-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="a8073-171">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a8073-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a8073-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="a8073-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="a8073-173">MFCMAPI (engl.) verwendet die **ResolveName** -Methode nach dem Anzeigenamen eines Adresseintrags Adressbuch nachzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="a8073-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8073-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8073-174">See also</span></span>



[<span data-ttu-id="a8073-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="a8073-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="a8073-176">IABContainer</span><span class="sxs-lookup"><span data-stu-id="a8073-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="a8073-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="a8073-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="a8073-178">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a8073-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="a8073-179">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a8073-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
