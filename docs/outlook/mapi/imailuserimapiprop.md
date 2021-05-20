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
# <a name="imailuser--imapiprop"></a><span data-ttu-id="53208-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="53208-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="53208-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53208-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53208-105">Bietet Zugriff auf die vielen Eigenschaften, die Messagingbenutzern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="53208-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="53208-106">Die **IMailUser-Schnittstelle** wird von Messagingbenutzerobjekten implementiert.</span><span class="sxs-lookup"><span data-stu-id="53208-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="53208-107">**IMailUser erbt** von der [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) und verfügt über keine eigenen eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="53208-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53208-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="53208-108">Header file:</span></span>  <br/> |<span data-ttu-id="53208-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53208-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="53208-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="53208-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="53208-111">Messagingbenutzerobjekte</span><span class="sxs-lookup"><span data-stu-id="53208-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="53208-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="53208-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="53208-113">Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="53208-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="53208-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="53208-114">Called by:</span></span>  <br/> |<span data-ttu-id="53208-115">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="53208-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="53208-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="53208-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="53208-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="53208-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="53208-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="53208-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="53208-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="53208-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="53208-120">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="53208-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="53208-121">Transacted</span><span class="sxs-lookup"><span data-stu-id="53208-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="53208-122">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="53208-122">Vtable order</span></span>

<span data-ttu-id="53208-123">Diese Schnittstelle verfügt nicht über eindeutige Methoden.</span><span class="sxs-lookup"><span data-stu-id="53208-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="53208-124">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="53208-124">**Required properties**</span></span>|<span data-ttu-id="53208-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="53208-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53208-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53208-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="53208-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="53208-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53208-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="53208-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="53208-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53208-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53208-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="53208-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53208-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="53208-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="53208-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53208-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53208-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="53208-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53208-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53208-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="53208-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53208-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53208-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="53208-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53208-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53208-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53208-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53208-142">Remarks</span></span>

<span data-ttu-id="53208-143">Fünf der erforderlichen Eigenschaften werden als Basisadresseneigenschaften für Empfänger bekannt:</span><span class="sxs-lookup"><span data-stu-id="53208-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="53208-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="53208-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="53208-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="53208-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="53208-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="53208-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="53208-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="53208-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="53208-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="53208-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="53208-149">Diese Eigenschaften gelten als besonders, da viele andere Gruppen ähnlicher Eigenschaften auf dieser Basisgruppe aufgebaut sind.</span><span class="sxs-lookup"><span data-stu-id="53208-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="53208-150">Die anderen Gruppen werden verwendet, um einen Empfänger in verschiedenen Rollen zu beschreiben, z. B. dem ursprünglichen Absender oder dem Stellvertretungssender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="53208-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="53208-151">Weitere Informationen zu diesen Eigenschaften und deren Verwendung finden Sie unter [MAPI Address Types](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="53208-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="53208-152">Messagingbenutzer können eine Auflistung ihrer Eigenschaften anzeigen, indem sie die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="53208-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="53208-153">**PR_DETAILS_TABLE** ist eine Anzeigetabelle, in der das Layout eines Detaildialogfelds oder einer Registerkarteneigenschaftsseite beschrieben wird, auf der Empfängereigenschaftsinformationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="53208-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="53208-154">MAPI erstellt Detaildialogfelder, wenn ein Client die [IAddrBook::D etails-Methode](iaddrbook-details.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="53208-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="53208-155">Messagingbenutzerobjekten können andere optionale Eigenschaften zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="53208-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="53208-156">MAPI definiert viele Eigenschaften, die zusätzliche Adressierungsinformationen zu einem Messagingbenutzer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="53208-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="53208-157">Alle diese Eigenschaften sind Zeichenzeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="53208-157">All of these properties are character strings.</span></span> <span data-ttu-id="53208-158">Die folgende Liste zeigt die häufiger verwendeten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="53208-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="53208-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="53208-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="53208-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="53208-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="53208-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="53208-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="53208-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53208-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="53208-166">Eine vollständige Liste der Eigenschaften finden Sie unter [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="53208-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="53208-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53208-167">See also</span></span>



[<span data-ttu-id="53208-168">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="53208-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

