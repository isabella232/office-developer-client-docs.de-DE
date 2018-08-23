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
ms.openlocfilehash: a120fb1710bf2bd351d956e4d05eb0af346ef4c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583386"
---
# <a name="iablogonopentemplateid"></a><span data-ttu-id="08be2-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="08be2-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="08be2-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08be2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08be2-105">Öffnet einen Empfänger-Eintrag, der Daten in einer Host-Adressbuchanbieter hat.</span><span class="sxs-lookup"><span data-stu-id="08be2-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="08be2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08be2-106">Parameters</span></span>

 <span data-ttu-id="08be2-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="08be2-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="08be2-108">[in] Die Byteanzahl von in der Vorlagenbezeichner auf den durch den Parameter _LpTemplateID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="08be2-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="08be2-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="08be2-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="08be2-110">[in] Ein Zeiger auf die Vorlagenbezeichner oder **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft des Empfängers Eintrags geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08be2-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="08be2-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="08be2-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="08be2-112">[in] Eine Bitmaske der Flags verwendet, um anzugeben, wie den Eintrag dargestellt durch die ID der Vorlage zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="08be2-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="08be2-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="08be2-113">The following flag can be set:</span></span>
    
<span data-ttu-id="08be2-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="08be2-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="08be2-115">Hostanbieter wird einen neuen Eintrag im Container basierend auf den Eintrag, dargestellt durch die ID der Vorlage erstellen.</span><span class="sxs-lookup"><span data-stu-id="08be2-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="08be2-116">Die **OpenTemplateID** -Methode sollte entweder bestimmte Initialisierung des Eintrags für die Hostanbieter ausführen, mithilfe der [IMAPIProp: IUnknown](imapipropiunknown.md) Implementierung im Parameter _LpMAPIPropData_ oder Rückgabe eines benutzerdefinierten **IMAPIProp **-Schnittstelle im _LppMAPIPropNew_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="08be2-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="08be2-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="08be2-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="08be2-118">[in] Ein Zeiger auf die Hostanbieter Property-Objekt und Implementierung einer Schnittstelle abgeleitet **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="08be2-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="08be2-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="08be2-119">_lpInterface_</span></span>
  
> <span data-ttu-id="08be2-120">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die den Typ des Zeigertools der Schnittstelle in der _LppMAPIPropNew_ -Parameter zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="08be2-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="08be2-121">Übergeben von **null** gibt die messaging-Benutzeroberfläche, [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="08be2-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="08be2-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="08be2-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="08be2-123">[out] Ein Zeiger auf das gebundenen Property-Objekt und eine Implementierung einer Schnittstelle **IMAPIProp**abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="08be2-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="08be2-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="08be2-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="08be2-125">[out] Reserviert. **null**muss sein.</span><span class="sxs-lookup"><span data-stu-id="08be2-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="08be2-126">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="08be2-126">Return value</span></span>

<span data-ttu-id="08be2-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="08be2-127">S_OK</span></span> 
  
> <span data-ttu-id="08be2-128">Der entsprechende Code wurde erfolgreich zu verwandten Daten in Hostanbieter gebunden.</span><span class="sxs-lookup"><span data-stu-id="08be2-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="08be2-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="08be2-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="08be2-130">Das Objekt unterstützt keine Vorlagen-IDs.</span><span class="sxs-lookup"><span data-stu-id="08be2-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="08be2-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="08be2-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="08be2-132">Die Vorlage-ID in der _LpTemplateID_ -Parameter übergeben wird von der Adressbuchanbieter nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="08be2-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="08be2-133">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="08be2-133">Remarks</span></span>

<span data-ttu-id="08be2-134">Die **OpenTemplateID** -Methode ist nur von adressbuchanbietern implementierte implementiert, die Kontrolle über Kopien der darin enthaltenen Einträge beibehalten werden, die in der Hostanbieter den Containern befinden.</span><span class="sxs-lookup"><span data-stu-id="08be2-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="08be2-135">Anbieter, **die OpenTemplateID** implementieren, werden als fremden adressbuchanbietern implementierte bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="08be2-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="08be2-136">Hostanbieter [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) um kopierten Eintrag erstellen oder öffnen Sie den kopierten Eintrag aufrufen und MAPI für den Aufruf von **OpenTemplateID**übergibt.</span><span class="sxs-lookup"><span data-stu-id="08be2-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="08be2-137">**OpenTemplateID** öffnet den Eintrag und bindet den Code, der mit Daten in Hostanbieter gesteuert.</span><span class="sxs-lookup"><span data-stu-id="08be2-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="08be2-138">Statt eine Eintrags-ID verwenden, wird **OpenTemplateID** einer anderen-Eigenschaft, den Eintrag Vorlagenbezeichner, **PR_TEMPLATEID**verwendet.</span><span class="sxs-lookup"><span data-stu-id="08be2-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="08be2-139">Vorlage Bezeichner sollte für Einträge unterstützt werden, dessen Code in ein Hostanbieter an Daten gebunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="08be2-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="08be2-140">Einige Beispiele für beim Adressbuch-Dienstanbieter **OpenTemplateID** implementieren sollten sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="08be2-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="08be2-141">Die Daten in einem Eintrag der kopierten regelmäßig aktualisieren, damit es mit der ursprünglichen synchronisiert bleibt.</span><span class="sxs-lookup"><span data-stu-id="08be2-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="08be2-142">Zum Implementieren der Funktionalität, mit denen Hostanbieter implementiert ist nicht möglich, wie dynamisches Auffüllen von Listen, die anhand von Daten auf einem Server in den Eintrag Detailtabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="08be2-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="08be2-143">Steuern die Interaktion zwischen Eigenschaften in der Hostanbieter-Eintrag und der ursprünglichen Eintrag, beispielsweise Netzwerke die **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) aus den Werten der Bearbeitungssteuerelemente in der Anzeige der Details, die verschiedene enthalten Komponenten der Adresse.</span><span class="sxs-lookup"><span data-stu-id="08be2-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="08be2-144">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="08be2-144">Notes to implementers</span></span>

<span data-ttu-id="08be2-145">Wenn ein Hostanbieter kopiert oder von Ihrem Dienstanbieter ein Eintrag erstellt, und Sie die Implementierung einer Eigenschaft-Objekt über **OpenTemplateID geben**, behandeln Sie die meisten Anrufe verwalten den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="08be2-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="08be2-146">Da es bis zu Hostanbieter diese Anrufe an Sie weitergeleitet wird, kann Hostanbieter jedoch intercept jeder Aufruf und benutzerdefinierte Verarbeitung vor dem Weiterleiten des Anrufs führen.</span><span class="sxs-lookup"><span data-stu-id="08be2-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="08be2-147">Sie sollten die folgenden Richtlinien in Ihrer Eigenschaft Objekt Implementierungen verwenden:</span><span class="sxs-lookup"><span data-stu-id="08be2-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="08be2-148">Wenn [IMAPIProp::GetProps](imapiprop-getprops.md) aufgerufen wird, bestimmen Sie, ob die Anforderung für eine berechnete Eigenschaft ist und es es zu behandeln ist.</span><span class="sxs-lookup"><span data-stu-id="08be2-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="08be2-149">Übertragen Sie alle Anfragen für nicht berechneten Eigenschaften in Hostanbieter.</span><span class="sxs-lookup"><span data-stu-id="08be2-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="08be2-150">[IMAPIProp::OpenProperty](imapiprop-openproperty.md) aufgerufen wird, um zu öffnen eine Tabelle mit Ausnahme der Details Tabelle anzuzeigen, die Anforderung behandelt.</span><span class="sxs-lookup"><span data-stu-id="08be2-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="08be2-151">Die meisten Tabellen werden nicht genau in Hostanbieter kopiert.</span><span class="sxs-lookup"><span data-stu-id="08be2-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="08be2-152">Sie müssen die **IMAPITable** -Implementierung für diese angeforderten Tabellen generieren.</span><span class="sxs-lookup"><span data-stu-id="08be2-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="08be2-153">Die Details Tabelle **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft muss für den Hostanbieter kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="08be2-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="08be2-154">Dies ermöglicht diesen Anbieter zum Generieren der Tabelle lokal.</span><span class="sxs-lookup"><span data-stu-id="08be2-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="08be2-155">Möglicherweise möchten Sie die Display-Tabelle-Implementierung, um anzeigebenachrichtigungen Tabelle generieren umbrochen.</span><span class="sxs-lookup"><span data-stu-id="08be2-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="08be2-156">Wenn [IMAPIProp::SetProps](imapiprop-setprops.md) aufgerufen wird, kann die Daten von Hostanbieter überprüft werden, vor, sodass Sie die Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="08be2-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="08be2-157">Sie können überprüfen, ob alle erforderlichen Eigenschaften festzulegen oder berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="08be2-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="08be2-158">Den entsprechende Fehlermeldung-Wert zurück, wenn ein Fehler erkannt wurde, und, sofern möglich, eine beliebige zusätzliche Erläuterung über [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="08be2-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="08be2-159">Wenn [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird, sollten die Hostanbieter Verarbeitung auszuführen, bevor Sie den Eintrag zu speichern.</span><span class="sxs-lookup"><span data-stu-id="08be2-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="08be2-160">Speichern Sie alle Daten, die durch die geänderten Eigenschaften, wie eine neue Adresse ein, in der Hostanbieter Eintrag betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="08be2-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="08be2-161">Im Allgemeinen nehmen Sie die Implementierung des Eintrags, der Sie übergeben wieder Hostanbieter intercept alle Methoden zum Ausführen der kontextbezogenen Bearbeitung der relevanten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08be2-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="08be2-162">Wenn das Flag FILL_ENTRY im _UlTemplateFlags_ -Parameter übergeben wird, legen Sie alle Eigenschaften für den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="08be2-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="08be2-163">Wenn Sie ein neues Property-Objekt in der _LppMAPIPropNew_ -Parameter zurückgeben möchten, rufen Sie die [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) -Methode der Hostanbieter Property-Objekts einen Verweis zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="08be2-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="08be2-164">Nachdem sie von der gebundenen Objekt behandelt werden, müssen alle Anrufe über das gebundenen-Objekt, das die Implementierung **IMAPIProp** in _LppMAPIPropNew_ zurückgegeben, die entsprechende Methode in der Host Property-Objekt weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="08be2-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="08be2-165">Die Eigenschaftenbezeichner der keine benannten Eigenschaften auf, die über Ihre gebundenen Property-Objekt übergeben werden befinden sich im Ihres Anbieters Bezeichner Namespace.</span><span class="sxs-lookup"><span data-stu-id="08be2-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="08be2-166">Die Implementierung der [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) -Methode sollte die Namen der Eigenschaften festlegen, so, dass es Vorlage-spezifischen Aufgaben ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="08be2-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="08be2-167">Eigenschaften, die vom Dienstanbieter für dem Hostanbieter übergibt müssen auf ähnliche Weise auch in Ihren Namespace sein.</span><span class="sxs-lookup"><span data-stu-id="08be2-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="08be2-168">Beispielsweise wenn Sie eine benannte Eigenschaft in **OpenTemplateID**festlegen, verwenden Sie Ihre-Bezeichner für den Namen – es, falls erforderlich, durch Aufrufen der [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode erstellen.</span><span class="sxs-lookup"><span data-stu-id="08be2-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="08be2-169">Wenn Sie die Eintrags-ID _LpTemplateID_übergebenen nicht kennen, geben Sie MAPI_E_UNKNOWN_ENTRYID zurück.</span><span class="sxs-lookup"><span data-stu-id="08be2-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="08be2-170">Weitere Informationen zum Arbeiten mit-Adressbuch Vorlage Adress-IDs finden Sie unter [als einen fremden Adressbuchanbieter fungiert](acting-as-a-foreign-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="08be2-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08be2-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08be2-171">See also</span></span>



[<span data-ttu-id="08be2-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="08be2-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="08be2-173">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="08be2-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="08be2-174">PidTagTemplateid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="08be2-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="08be2-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08be2-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

