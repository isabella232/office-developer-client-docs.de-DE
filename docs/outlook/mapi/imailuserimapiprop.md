---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436594"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="6211a-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6211a-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="6211a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6211a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6211a-105">Ermöglicht den Zugriff auf die vielen Eigenschaften, die Messaging Benutzern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6211a-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="6211a-106">Die **IMailUser** -Schnittstelle wird von Messaging-Benutzerobjekten implementiert.</span><span class="sxs-lookup"><span data-stu-id="6211a-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="6211a-107">**IMailUser** erbt von der [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle und verfügt über keine eigenen eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="6211a-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6211a-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6211a-108">Header file:</span></span>  <br/> |<span data-ttu-id="6211a-109">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6211a-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6211a-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="6211a-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="6211a-111">Messaging-Benutzerobjekte</span><span class="sxs-lookup"><span data-stu-id="6211a-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="6211a-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6211a-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="6211a-113">Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="6211a-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="6211a-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6211a-114">Called by:</span></span>  <br/> |<span data-ttu-id="6211a-115">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6211a-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="6211a-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="6211a-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6211a-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="6211a-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="6211a-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="6211a-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="6211a-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="6211a-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="6211a-120">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="6211a-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="6211a-121">Durchgeführt</span><span class="sxs-lookup"><span data-stu-id="6211a-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6211a-122">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="6211a-122">Vtable order</span></span>

<span data-ttu-id="6211a-123">Diese Schnittstelle hat keine eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="6211a-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="6211a-124">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="6211a-124">**Required properties**</span></span>|<span data-ttu-id="6211a-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="6211a-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6211a-126">**PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6211a-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6211a-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="6211a-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6211a-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6211a-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="6211a-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6211a-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6211a-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="6211a-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6211a-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6211a-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="6211a-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6211a-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6211a-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="6211a-136">**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6211a-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6211a-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="6211a-138">**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6211a-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6211a-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="6211a-140">**PR_SEARCH_KEY** ([Pidtagsearchkey (](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6211a-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6211a-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6211a-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6211a-142">Remarks</span></span>

<span data-ttu-id="6211a-143">Fünf der erforderlichen Eigenschaften werden als Basis Adresseigenschaften für Empfänger bezeichnet:</span><span class="sxs-lookup"><span data-stu-id="6211a-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="6211a-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="6211a-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="6211a-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="6211a-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="6211a-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="6211a-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="6211a-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="6211a-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="6211a-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="6211a-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="6211a-149">Diese Eigenschaften gelten als besonders, da viele andere Gruppen ähnlicher Eigenschaften auf dieser Basisgruppe basieren.</span><span class="sxs-lookup"><span data-stu-id="6211a-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="6211a-150">Die anderen Gruppen werden zur Beschreibung eines Empfängers in verschiedenen Rollen verwendet, beispielsweise als ursprünglicher oder Stellvertreter der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6211a-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="6211a-151">Weitere Informationen zu diesen Eigenschaften und deren Verwendung finden Sie unter [MAPI address types](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="6211a-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="6211a-152">Messaging Benutzer können eine Auflistung ihrer Eigenschaften anzeigen, indem Sie die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6211a-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="6211a-153">**PR_DETAILS_TABLE** ist eine Anzeigetabelle, die das Layout eines Details-Dialogfelds oder einer Eigenschaftenseite mit Registerkarten beschreibt, auf dem Informationen zu Empfänger Eigenschaften angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6211a-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="6211a-154">MAPI erstellt Detail Dialogfelder, wenn ein Client die [IAddrBook::D ails](iaddrbook-details.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="6211a-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="6211a-155">Für Messaging-Benutzerobjekte können andere optionale Eigenschaften zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6211a-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="6211a-156">MAPI definiert viele Eigenschaften, die zusätzliche Adressinformationen zu einem Messagingbenutzer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6211a-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="6211a-157">Alle diese Eigenschaften sind Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="6211a-157">All of these properties are character strings.</span></span> <span data-ttu-id="6211a-158">Die folgende Liste zeigt die häufiger verwendeten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6211a-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="6211a-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6211a-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6211a-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6211a-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6211a-163">**PR_GOVERNMENT_ID_NUMBER** ([Pidtaggovernmentidnumber (](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6211a-164">**PR_LOCALITY** ([Pidtaglocality (](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6211a-165">**PR_POSTAL_ADDRESS** ([Pidtagpostaladdress (](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6211a-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="6211a-166">Eine vollständige Liste der Eigenschaften finden Sie unter [Zuordnen von kanonischEn Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="6211a-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6211a-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6211a-167">See also</span></span>



[<span data-ttu-id="6211a-168">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6211a-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

