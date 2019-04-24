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
# <a name="iablogonopentemplateid"></a><span data-ttu-id="9f767-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="9f767-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="9f767-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f767-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f767-105">Öffnet einen Empfängereintrag mit Daten, die sich in einem Host-Adressbuchanbieter befinden.</span><span class="sxs-lookup"><span data-stu-id="9f767-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="9f767-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f767-106">Parameters</span></span>

 <span data-ttu-id="9f767-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="9f767-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="9f767-108">in Die Anzahl der Bytes im Vorlagenbezeichner, auf die durch den _lpTemplateID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9f767-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="9f767-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="9f767-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="9f767-110">in Ein Zeiger auf den Vorlagenbezeichner oder die **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft des Empfänger Eintrags, der geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f767-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="9f767-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="9f767-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="9f767-112">in Eine Bitmaske von Flags, mit der angegeben wird, wie der durch den Vorlagenbezeichner dargestellte Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="9f767-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="9f767-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9f767-113">The following flag can be set:</span></span>
    
<span data-ttu-id="9f767-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="9f767-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="9f767-115">Der Hostanbieter erstellt anhand des vom Vorlagenbezeichner dargestellten Eintrags einen neuen Eintrag im Container.</span><span class="sxs-lookup"><span data-stu-id="9f767-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="9f767-116">Die **IABLogon::** opentemplatecollection-Methode sollte entweder eine bestimmte Initialisierung des Eintrags des Host Anbieters durchführen, indem Sie die [IMAPIProp: IUnknown](imapipropiunknown.md) -Implementierung im _lpMAPIPropData_ -Parameter verwenden oder eine benutzerdefinierte IMAPIProp zurückgeben. \*\* \*\*Schnittstellenimplementierung im _lppMAPIPropNew_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="9f767-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="9f767-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="9f767-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="9f767-118">in Ein Zeiger auf das Property-Objekt des Host Anbieters und die Implementierung einer von **IMAPIProp**abgeleiteten Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9f767-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="9f767-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="9f767-119">_lpInterface_</span></span>
  
> <span data-ttu-id="9f767-120">in Ein Zeiger auf die Schnittstellen-ID (IID), die den Typ des Schnittstellenzeigers darstellt, der im _lppMAPIPropNew_ -Parameter zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f767-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="9f767-121">Durch das Übergeben von **null** wird die standardmäßige Messaging-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9f767-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="9f767-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="9f767-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="9f767-123">Out Ein Zeiger auf das gebundene Property-Objekt und eine Implementierung einer von **IMAPIProp**abgeleiteten Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9f767-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="9f767-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="9f767-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="9f767-125">Out Reserviert muss **null**sein.</span><span class="sxs-lookup"><span data-stu-id="9f767-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f767-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f767-126">Return value</span></span>

<span data-ttu-id="9f767-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f767-127">S_OK</span></span> 
  
> <span data-ttu-id="9f767-128">Der entsprechende Code wurde erfolgreich an verknüpfte Daten im Hostanbieter gebunden.</span><span class="sxs-lookup"><span data-stu-id="9f767-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="9f767-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9f767-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9f767-130">Das Objekt unterstützt keine Vorlagen-IDs.</span><span class="sxs-lookup"><span data-stu-id="9f767-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="9f767-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9f767-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="9f767-132">Der im _lpTemplateID_ -Parameter übergebene Vorlagenbezeichner wird vom Adressbuchanbieter nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="9f767-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9f767-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f767-133">Remarks</span></span>

<span data-ttu-id="9f767-134">Die **IABLogon::** opentemplatecode-Methode wird nur von Adressbuch Anbietern implementiert, die die Kontrolle über Kopien Ihrer Einträge behalten müssen, die sich in den Containern von Hostanbietern befinden.</span><span class="sxs-lookup"><span data-stu-id="9f767-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="9f767-135">Anbieter, die \*\*\*\* opentemplatecode implementieren, werden als fremde Adressbuchanbieter bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9f767-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="9f767-136">Host Anbieter rufen [IMAPISupport::](imapisupport-opentemplateid.md) opentemplatecode auf, um einen kopierten Eintrag zu erstellen oder den kopierten Eintrag zu öffnen, und MAPI übergibt den Aufruf an **IABLogon::** opentemplatecode.</span><span class="sxs-lookup"><span data-stu-id="9f767-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="9f767-137">**IABLogon::** opentemplatecode öffnet den Eintrag und bindet den Code, der ihn steuert, an Daten im Hostanbieter.</span><span class="sxs-lookup"><span data-stu-id="9f767-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="9f767-138">Statt eine Eintrags-ID zu verwenden, verwendet **IABLogon::** opentemplatecode eine andere Eigenschaft, den Vorlagenbezeichner des Eintrags, **PR_TEMPLATEID**.</span><span class="sxs-lookup"><span data-stu-id="9f767-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="9f767-139">Vorlagenbezeichner sollten für Einträge unterstützt werden, deren Code an Daten in einem Hostanbieter gebunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="9f767-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="9f767-140">Einige Beispiele dafür, wann ein Adressbuchanbieter **IABLogon::** opentemplateserver implementieren sollte, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9f767-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="9f767-141">So aktualisieren Sie die Daten für einen kopierten Eintrag in regelmäßigen Abständen, damit Sie mit dem Original synchronisiert bleiben.</span><span class="sxs-lookup"><span data-stu-id="9f767-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="9f767-142">Zum Implementieren von Funktionen, die der Hostanbieter nicht implementieren kann, wie das dynamische Auffüllen einer Liste, die in der Details-Tabelle des Eintrags angezeigt wird, aus Daten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="9f767-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="9f767-143">Um die Interaktion zwischen den Eigenschaften im Eintrag des Host Anbieters und dem ursprünglichen Eintrag zu steuern, wie etwa dem Berechnen des **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) aus den Werten der Bearbeitungssteuerelemente in der Detailanzeige, die unterschiedliche Komponenten der Adresse.</span><span class="sxs-lookup"><span data-stu-id="9f767-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="9f767-144">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="9f767-144">Notes to implementers</span></span>

<span data-ttu-id="9f767-145">Wenn ein Hostanbieter einen Eintrag von Ihrem Anbieter kopiert oder erstellt und Sie eine Property-Objekt Implementierung über **IABLogon::** opentemplatecollection bereitstellen, behandeln Sie die meisten Aufrufe, um den Eintrag zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="9f767-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="9f767-146">Da der Hostanbieter diese Anrufe an Sie weiterleiten muss, kann der Hostanbieter jedoch alle Anrufe abfangen und eine benutzerdefinierte Verarbeitung durchführen, bevor der Anruf weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="9f767-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="9f767-147">Sie sollten die folgenden Richtlinien in ihren Property-Objekt-Implementierungen verwenden:</span><span class="sxs-lookup"><span data-stu-id="9f767-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="9f767-148">Wenn [IMAPIProp::](imapiprop-getprops.md) GetProps aufgerufen wird, bestimmen Sie, ob es sich bei der Anforderung um eine berechnete Eigenschaft handelt, und behandeln Sie diese.</span><span class="sxs-lookup"><span data-stu-id="9f767-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="9f767-149">Übertragen Sie alle Anforderungen für nicht berechnete Eigenschaften an den Hostanbieter.</span><span class="sxs-lookup"><span data-stu-id="9f767-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="9f767-150">Wenn [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) aufgerufen wird, um eine Tabelle mit Ausnahme der Details-Anzeigetabelle zu öffnen, behandeln Sie die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9f767-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="9f767-151">Die meisten Tabellen können nicht genau in den Hostanbieter kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f767-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="9f767-152">Sie müssen die **IMAPITable** -Implementierung für diese angeforderten Tabellen generieren.</span><span class="sxs-lookup"><span data-stu-id="9f767-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="9f767-153">Die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft der Details-Tabelle muss in den Hostanbieter kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f767-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="9f767-154">Dies ermöglicht es diesem Anbieter, die Tabelle lokal zu generieren.</span><span class="sxs-lookup"><span data-stu-id="9f767-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="9f767-155">Möglicherweise möchten Sie die Implementierung der Display-Tabelle umbrechen, um Anzeige Tabellen Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="9f767-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="9f767-156">Wenn [IMAPIProp::](imapiprop-setprops.md) SetProps aufgerufen wird, kann der Hostanbieter die Daten überprüfen, bevor Sie die Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="9f767-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="9f767-157">Sie können überprüfen, ob alle erforderlichen Eigenschaften festgelegt oder berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="9f767-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="9f767-158">Wenn ein Fehler erkannt wird, geben Sie den entsprechenden Fehlerwert und, falls möglich, weitere Erläuterungen über [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="9f767-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="9f767-159">Wenn [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) aufgerufen wird, kann der Hostanbieter die Verarbeitung vor dem Speichern des Eintrags ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f767-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="9f767-160">Sie sollten alle Daten, die von den geänderten Eigenschaften betroffen sind, wie beispielsweise eine neue Adresse, im Eintrag des Host Anbieters speichern.</span><span class="sxs-lookup"><span data-stu-id="9f767-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="9f767-161">Im Allgemeinen sollten Sie die Implementierung des Eintrags, den Sie an den Hostanbieter zurückgeben, abfangen, um alle Methoden zum Durchführen einer kontextspezifischen Manipulation der relevanten Eigenschaften zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="9f767-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="9f767-162">Wenn das FILL_ENTRY-Flag im _ulTemplateFlags_ -Parameter übergeben wird, legen Sie alle Eigenschaften für den Eintrag fest.</span><span class="sxs-lookup"><span data-stu-id="9f767-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="9f767-163">Wenn Sie ein neues Property-Objekt im _lppMAPIPropNew_ -Parameter zurückgeben, rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) -Methode des Property-Objekts des Host Anbieters auf, um einen Verweis zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="9f767-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="9f767-164">Alle Aufrufe über das gebundene Objekt, die die **IMAPIProp** -Implementierung in _lppMAPIPropNew_ zurückgegeben wird, sollten an Ihre entsprechende Methode im Host Property-Objekt weitergeleitet werden, nachdem Sie vom gebundenen Objekt behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="9f767-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="9f767-165">Die Eigenschaftenbezeichner aller benannten Eigenschaften, die durch das gebundene Property-Objekt übergeben werden, befinden sich im Bezeichner-Namespace Ihres Anbieters.</span><span class="sxs-lookup"><span data-stu-id="9f767-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="9f767-166">Durch die Implementierung der [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) -Methode sollten die Namen der Eigenschaften bestimmt werden, sodass Vorlagenspezifische Aufgaben ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="9f767-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="9f767-167">Entsprechend müssen Eigenschaften, die Ihr Anbieter an den Hostanbieter übergibt, auch in Ihrem Namespace sein.</span><span class="sxs-lookup"><span data-stu-id="9f767-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="9f767-168">Wenn Sie beispielsweise eine benannte Eigenschaft in openTemplatecode festlegen, sollten Sie einen ihrer Bezeichner für den Namen verwenden, um ihn gegebenenfalls zu erstellen, indem Sie die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode aufrufen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9f767-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="9f767-169">Wenn Sie den in _lpTemplateID_übergebenen Eintragsbezeichner nicht erkennen, geben Sie MAPI_E_UNKNOWN_ENTRYID zurück.</span><span class="sxs-lookup"><span data-stu-id="9f767-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="9f767-170">Weitere Informationen zum Arbeiten mit Adressbuchvorlagen-IDs finden Sie unter [agieren als ein fremder Adressbuchanbieter](acting-as-a-foreign-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9f767-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f767-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f767-171">See also</span></span>



[<span data-ttu-id="9f767-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="9f767-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="9f767-173">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9f767-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="9f767-174">Kanonische Pidtagtemplateid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9f767-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="9f767-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f767-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

