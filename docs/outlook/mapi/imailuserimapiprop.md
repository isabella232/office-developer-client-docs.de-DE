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
ms.openlocfilehash: 7a6971504ec8f4f5ac8593b6b78777a12ff92b3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564563"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="899cf-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="899cf-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="899cf-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="899cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="899cf-105">Bietet Zugriff auf die viele Eigenschaften, die messaging-Benutzer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="899cf-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="899cf-106">Die **IMailUser** -Schnittstelle wird von messaging Benutzerobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="899cf-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="899cf-107">**IMailUser** erbt von der [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle und verfügt über keine eindeutigen Methoden eigenen.</span><span class="sxs-lookup"><span data-stu-id="899cf-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="899cf-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="899cf-108">Header file:</span></span>  <br/> |<span data-ttu-id="899cf-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="899cf-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="899cf-110">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="899cf-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="899cf-111">Messaging User-Objekte</span><span class="sxs-lookup"><span data-stu-id="899cf-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="899cf-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="899cf-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="899cf-113">Von adressbuchanbietern implementierte</span><span class="sxs-lookup"><span data-stu-id="899cf-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="899cf-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="899cf-114">Called by:</span></span>  <br/> |<span data-ttu-id="899cf-115">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="899cf-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="899cf-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="899cf-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="899cf-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="899cf-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="899cf-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="899cf-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="899cf-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="899cf-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="899cf-120">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="899cf-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="899cf-121">Durchgeführt</span><span class="sxs-lookup"><span data-stu-id="899cf-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="899cf-122">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="899cf-122">Vtable order</span></span>

<span data-ttu-id="899cf-123">Diese Schnittstelle hat keinen eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="899cf-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="899cf-124">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="899cf-124">**Required properties**</span></span>|<span data-ttu-id="899cf-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="899cf-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="899cf-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="899cf-127">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="899cf-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="899cf-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="899cf-129">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="899cf-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="899cf-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="899cf-131">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="899cf-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="899cf-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="899cf-133">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="899cf-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="899cf-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="899cf-135">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="899cf-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="899cf-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="899cf-137">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="899cf-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="899cf-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="899cf-139">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="899cf-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="899cf-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="899cf-141">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="899cf-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="899cf-142">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="899cf-142">Remarks</span></span>

<span data-ttu-id="899cf-143">Fünf erforderlichen Eigenschaften sind als die Eigenschaften Basisadresse für Empfänger bekannt:</span><span class="sxs-lookup"><span data-stu-id="899cf-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="899cf-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="899cf-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="899cf-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="899cf-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="899cf-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="899cf-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="899cf-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="899cf-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="899cf-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="899cf-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="899cf-149">Diese Eigenschaften gelten besondere, da viele andere Gruppen von ähnlichen Eigenschaften auf dieser Basis Gruppe basieren.</span><span class="sxs-lookup"><span data-stu-id="899cf-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="899cf-150">Die anderen Gruppen werden verwendet, um einen Empfänger in verschiedenen Rollen wird beschrieben, wie eine Nachricht ursprünglichen's oder Absender delegieren.</span><span class="sxs-lookup"><span data-stu-id="899cf-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="899cf-151">Weitere Informationen zu diesen Eigenschaften und deren Verwendung finden Sie unter [MAPI-Adresstypen](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="899cf-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="899cf-152">Messaging-Benutzer kann eine Auflistung von deren Eigenschaften anzeigen, indem Sie die Eigenschaft **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="899cf-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="899cf-153">**PR_DETAILS_TABLE** ist eine zeigt die Tabelle, die beschreibt das Layout einer im Dialogfeld Details oder eine der Eigenschaftenseiten, die Empfänger-Eigenschafteninformationen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="899cf-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="899cf-154">MAPI erstellt Details Dialogfelder, wenn ein Client die [IAddrBook::Details](iaddrbook-details.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="899cf-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="899cf-155">Messaging User-Objekte kann weitere optionalen Eigenschaften zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="899cf-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="899cf-156">MAPI definiert viele Eigenschaften, die zusätzliche reagieren auf Informationen über ein messaging-Benutzer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="899cf-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="899cf-157">Alle diese Eigenschaften sind Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="899cf-157">All of these properties are character strings.</span></span> <span data-ttu-id="899cf-158">Die folgende Liste enthält mehrere Eigenschaften häufig verwendet:</span><span class="sxs-lookup"><span data-stu-id="899cf-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="899cf-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="899cf-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="899cf-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="899cf-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="899cf-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="899cf-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="899cf-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="899cf-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="899cf-166">Eine vollständige Liste der Eigenschaften finden Sie unter [Zuordnen von kanonischen Eigenschaftennamen MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="899cf-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="899cf-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="899cf-167">See also</span></span>



[<span data-ttu-id="899cf-168">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="899cf-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

