---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334748"
---
# <a name="iablogonopentemplateid"></a><span data-ttu-id="e0438-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="e0438-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="e0438-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0438-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0438-105">Öffnet einen Empfängereintrag mit Daten in einem Host-Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="e0438-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="e0438-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0438-106">Parameters</span></span>

 <span data-ttu-id="e0438-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="e0438-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="e0438-108">[in] Die Byteanzahl in der Vorlagen-ID, auf die der  _lpTemplateID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="e0438-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="e0438-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="e0438-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="e0438-110">[in] Ein Zeiger auf die Vorlagen-ID oder **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft des zu öffnenden Empfängereintrags.</span><span class="sxs-lookup"><span data-stu-id="e0438-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="e0438-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="e0438-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="e0438-112">[in] Eine Bitmaske mit Flags, mit der angegeben wird, wie der durch die Vorlagen-ID dargestellte Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="e0438-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="e0438-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e0438-113">The following flag can be set:</span></span>
    
<span data-ttu-id="e0438-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="e0438-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="e0438-115">Der Hostanbieter erstellt einen neuen Eintrag in seinem Container basierend auf dem Durch die Vorlagen-ID dargestellten Eintrag.</span><span class="sxs-lookup"><span data-stu-id="e0438-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="e0438-116">Die **IABLogon::OpenTemplateID-Methode** sollte entweder eine bestimmte Initialisierung des Eintrags des Hostanbieters mithilfe der [IMAPIProp : IUnknown-Implementierung](imapipropiunknown.md) im  _lpMAPIPropData-Parameter_ durchführen oder eine benutzerdefinierte **IMAPIProp-Schnittstellenimplementierung** im  _lppMAPIPropNew-Parameter_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e0438-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="e0438-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="e0438-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="e0438-118">[in] Ein Zeiger auf das Eigenschaftsobjekt des Hostanbieters und die Implementierung einer Schnittstelle, die von **IMAPIProp abgeleitet ist.**</span><span class="sxs-lookup"><span data-stu-id="e0438-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="e0438-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e0438-119">_lpInterface_</span></span>
  
> <span data-ttu-id="e0438-120">[in] Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der den Typ des Schnittstellenzeigers darstellt, der im  _lppMAPIPropNew-Parameter zurückgegeben werden_ soll.</span><span class="sxs-lookup"><span data-stu-id="e0438-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="e0438-121">Durch **Übergeben von null** wird die standardmäßige Messagingbenutzeroberfläche [IMailUser : IMAPIProp zurückgegeben.](imailuserimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="e0438-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="e0438-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="e0438-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="e0438-123">[out] Ein Zeiger auf das gebundene Eigenschaftsobjekt und eine Implementierung einer Schnittstelle, die von **IMAPIProp abgeleitet ist.**</span><span class="sxs-lookup"><span data-stu-id="e0438-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="e0438-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="e0438-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="e0438-125">[out] Reserviert; muss **null sein.**</span><span class="sxs-lookup"><span data-stu-id="e0438-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0438-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0438-126">Return value</span></span>

<span data-ttu-id="e0438-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0438-127">S_OK</span></span> 
  
> <span data-ttu-id="e0438-128">Der entsprechende Code wurde erfolgreich an verwandte Daten im Hostanbieter gebunden.</span><span class="sxs-lookup"><span data-stu-id="e0438-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="e0438-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e0438-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e0438-130">Das Objekt unterstützt keine Vorlagen-IDs.</span><span class="sxs-lookup"><span data-stu-id="e0438-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="e0438-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e0438-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="e0438-132">Der im  _lpTemplateID-Parameter_ übergebene Vorlagenbezeichner wird vom Adressbuchanbieter nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="e0438-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e0438-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e0438-133">Remarks</span></span>

<span data-ttu-id="e0438-134">Die **IABLogon::OpenTemplateID-Methode** wird nur von Adressbuchanbietern implementiert, die die Kontrolle über Kopien ihrer Einträge behalten müssen, die sich in den Containern von Hostanbietern befinden.</span><span class="sxs-lookup"><span data-stu-id="e0438-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="e0438-135">Anbieter, die **OpenTemplateID implementieren,** werden als fremde Adressbuchanbieter bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e0438-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="e0438-136">Hostanbieter rufen [IMAPISupport::OpenTemplateID auf,](imapisupport-opentemplateid.md) um einen kopierten Eintrag zu erstellen oder den kopierten Eintrag zu öffnen, und MAPI übergibt den Aufruf an **IABLogon::OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="e0438-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="e0438-137">**IABLogon::OpenTemplateID** öffnet den Eintrag und bindet den Code, der ihn steuert, an Daten im Hostanbieter.</span><span class="sxs-lookup"><span data-stu-id="e0438-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="e0438-138">Anstatt einen Eintragsbezeichner zu verwenden, verwendet **IABLogon::OpenTemplateID** eine andere Eigenschaft, den Vorlagenbezeichner des Eintrags, **PR_TEMPLATEID**.</span><span class="sxs-lookup"><span data-stu-id="e0438-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="e0438-139">Vorlagenbezeichner sollten für Einträge unterstützt werden, deren Code an Daten in einem Hostanbieter gebunden sein muss.</span><span class="sxs-lookup"><span data-stu-id="e0438-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="e0438-140">Einige Beispiele dafür, wann ein Adressbuchanbieter **IABLogon::OpenTemplateID** implementieren soll, sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e0438-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="e0438-141">So aktualisieren Sie die Daten für einen kopierten Eintrag regelmäßig, damit sie mit dem Original synchronisiert bleiben.</span><span class="sxs-lookup"><span data-stu-id="e0438-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="e0438-142">So implementieren Sie Funktionen, die der Hostanbieter nicht implementieren kann, z. B. dynamisches Auffüllen einer Liste, die in der Detailtabelle des Eintrags aus Daten auf einem Server angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e0438-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="e0438-143">So steuern Sie die Interaktion zwischen Eigenschaften im Eintrag des Hostanbieters und dem ursprünglichen Eintrag, z. B. das Berechnen des **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) aus den Werten der Bearbeitungssteuerelemente in der Detailanzeige, die unterschiedliche Komponenten der Adresse enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0438-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="e0438-144">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e0438-144">Notes to implementers</span></span>

<span data-ttu-id="e0438-145">Wenn ein Hostanbieter einen Eintrag von Ihrem Anbieter kopiert oder erstellt und Sie eine Eigenschaftsobjektimplementierung über **IABLogon::OpenTemplateID** liefern, verarbeiten Sie die meisten Aufrufe zum Verwalten des Eintrags.</span><span class="sxs-lookup"><span data-stu-id="e0438-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="e0438-146">Da es jedoch aufgabe des Hostanbieters ist, diese Anrufe an Sie weiter zu weiterleiten, kann der Hostanbieter jeden Anruf abfangen und eine benutzerdefinierte Verarbeitung vor dem Weiterleiten des Anrufs durchführen.</span><span class="sxs-lookup"><span data-stu-id="e0438-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="e0438-147">Sie sollten die folgenden Richtlinien in Ihren Eigenschaftsobjektimplementierungen verwenden:</span><span class="sxs-lookup"><span data-stu-id="e0438-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="e0438-148">Wenn [IMAPIProp::GetProps](imapiprop-getprops.md) aufgerufen wird, bestimmen Sie, ob die Anforderung für eine berechnete Eigenschaft gilt, und behandeln Sie sie, falls ja.</span><span class="sxs-lookup"><span data-stu-id="e0438-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="e0438-149">Übertragen Sie alle Anforderungen für nicht komputierte Eigenschaften an den Hostanbieter.</span><span class="sxs-lookup"><span data-stu-id="e0438-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="e0438-150">Wenn [IMAPIProp::OpenProperty](imapiprop-openproperty.md) aufgerufen wird, um eine beliebige Tabelle mit Ausnahme der Detailanzeigetabelle zu öffnen, behandeln Sie die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e0438-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="e0438-151">Die meisten Tabellen können nicht exakt in den Hostanbieter kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="e0438-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="e0438-152">Sie müssen die **IMAPITable-Implementierung** für diese angeforderten Tabellen generieren.</span><span class="sxs-lookup"><span data-stu-id="e0438-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="e0438-153">Die Detailtabelle **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft muss in den Hostanbieter kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="e0438-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="e0438-154">Dadurch kann dieser Anbieter die Tabelle lokal generieren.</span><span class="sxs-lookup"><span data-stu-id="e0438-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="e0438-155">Möglicherweise möchten Sie die Implementierung der Anzeigetabelle umschließen, um Anzeigetabellebenachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="e0438-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="e0438-156">Wenn [IMAPIProp::SetProps](imapiprop-setprops.md) aufgerufen wird, kann der Hostanbieter die Daten überprüfen, bevor Sie die Eigenschaften festlegen können.</span><span class="sxs-lookup"><span data-stu-id="e0438-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="e0438-157">Sie können überprüfen, ob alle erforderlichen Eigenschaften festgelegt oder berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="e0438-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="e0438-158">Wenn ein Fehler erkannt wird, geben Sie den entsprechenden Fehlerwert und, falls dies der Fall ist, eine weitere Erläuterung über [IMAPIProp::GetLastError zurück.](imapiprop-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="e0438-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="e0438-159">Wenn [IMAPIProp::SaveChanges aufgerufen](imapiprop-savechanges.md) wird, möchte der Hostanbieter möglicherweise eine Verarbeitung durchführen, bevor Sie den Eintrag speichern.</span><span class="sxs-lookup"><span data-stu-id="e0438-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="e0438-160">Sie sollten alle Daten, die von den geänderten Eigenschaften betroffen sind, z. B. eine neue Adresse, im Eintrag des Hostanbieters speichern.</span><span class="sxs-lookup"><span data-stu-id="e0438-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="e0438-161">Im Allgemeinen sollten Sie die Implementierung des Eintrags, den Sie an den Hostanbieter übergeben, alle Methoden abfangen, um kontextspezifische Manipulationen der relevanten Eigenschaften durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="e0438-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="e0438-162">Wenn das FILL_ENTRY im  _ulTemplateFlags-Parameter_ übergeben wird, legen Sie alle Eigenschaften für den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="e0438-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="e0438-163">Wenn Sie ein neues Eigenschaftsobjekt im  _lppMAPIPropNew-Parameter_ zurückgeben, rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) des Eigenschaftsobjekts des Hostanbieters auf, um einen Verweis zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e0438-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="e0438-164">Alle Aufrufe über das gebundene Objekt, das von der in _lppMAPIPropNew_ zurückgegebenen **IMAPIProp-Implementierung** zurückgegeben wird, sollten an die entsprechende Methode im Hosteigenschaftsobjekt geroutet werden, nachdem sie vom gebundenen Objekt behandelt wurden.</span><span class="sxs-lookup"><span data-stu-id="e0438-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="e0438-165">Die Eigenschafts-IDs aller benannten Eigenschaften, die über ihr gebundenes Eigenschaftsobjekt übergeben werden, befinden sich im Bezeichnernamespace Ihres Anbieters.</span><span class="sxs-lookup"><span data-stu-id="e0438-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="e0438-166">Ihre Implementierung der [IMAPIProp::GetNamesFromIDs-Methode](imapiprop-getnamesfromids.md) sollte die Namen der Eigenschaften bestimmen, damit sie vorlagenspezifische Aufgaben ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="e0438-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="e0438-167">Ebenso müssen sich Eigenschaften, die Ihr Anbieter an den Hostanbieter weitergibt, auch in Ihrem Namespace enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0438-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="e0438-168">Wenn Sie z. B. eine benannte Eigenschaft in **OpenTemplateID** festlegen, sollten Sie einen Ihrer Bezeichner für den Namen verwenden, indem Sie sie bei Bedarf erstellen, indem Sie die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e0438-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="e0438-169">Wenn Sie den in  _lpTemplateID_ übergebenen Eintragsbezeichner nicht erkennen, geben Sie MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="e0438-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="e0438-170">Weitere Informationen zum Arbeiten mit Adressbuchvorlagenbezeichnern finden Sie unter [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e0438-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0438-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0438-171">See also</span></span>



[<span data-ttu-id="e0438-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="e0438-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="e0438-173">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e0438-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="e0438-174">PidTagTemplateid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e0438-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="e0438-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0438-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

