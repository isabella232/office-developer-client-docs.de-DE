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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0c70d16d294426d30f3ac5f00b6bc46992386a86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792070"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="9db11-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9db11-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="9db11-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9db11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9db11-105">Bietet Zugriff auf die viele Eigenschaften, die messaging-Benutzer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9db11-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="9db11-106">Die **IMailUser** -Schnittstelle wird von messaging Benutzerobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="9db11-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="9db11-107">**IMailUser** erbt von der [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle und verfügt über keine eindeutigen Methoden eigenen.</span><span class="sxs-lookup"><span data-stu-id="9db11-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9db11-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9db11-108">Header file:</span></span>  <br/> |<span data-ttu-id="9db11-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9db11-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9db11-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="9db11-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="9db11-111">Messaging User-Objekte</span><span class="sxs-lookup"><span data-stu-id="9db11-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="9db11-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9db11-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="9db11-113">Von adressbuchanbietern implementierte</span><span class="sxs-lookup"><span data-stu-id="9db11-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="9db11-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9db11-114">Called by:</span></span>  <br/> |<span data-ttu-id="9db11-115">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="9db11-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="9db11-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="9db11-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9db11-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="9db11-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="9db11-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="9db11-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="9db11-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="9db11-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="9db11-120">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="9db11-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="9db11-121">Durchgeführt</span><span class="sxs-lookup"><span data-stu-id="9db11-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9db11-122">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="9db11-122">Vtable order</span></span>

<span data-ttu-id="9db11-123">Diese Schnittstelle hat keinen eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="9db11-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="9db11-124">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="9db11-124">**Required properties**</span></span>|<span data-ttu-id="9db11-125">**Zugriff**</span><span class="sxs-lookup"><span data-stu-id="9db11-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9db11-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9db11-127">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="9db11-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="9db11-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9db11-129">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="9db11-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="9db11-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9db11-131">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9db11-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="9db11-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9db11-133">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="9db11-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="9db11-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9db11-135">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9db11-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="9db11-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9db11-137">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9db11-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="9db11-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9db11-139">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9db11-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="9db11-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9db11-141">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9db11-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9db11-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9db11-142">Remarks</span></span>

<span data-ttu-id="9db11-143">Fünf erforderlichen Eigenschaften sind als die Eigenschaften Basisadresse für Empfänger bekannt:</span><span class="sxs-lookup"><span data-stu-id="9db11-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="9db11-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9db11-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="9db11-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="9db11-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="9db11-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="9db11-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="9db11-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="9db11-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="9db11-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="9db11-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="9db11-149">Diese Eigenschaften gelten besondere, da viele andere Gruppen von ähnlichen Eigenschaften auf dieser Basis Gruppe basieren.</span><span class="sxs-lookup"><span data-stu-id="9db11-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="9db11-150">Die anderen Gruppen werden verwendet, um einen Empfänger in verschiedenen Rollen wird beschrieben, wie eine Nachricht ursprünglichen's oder Absender delegieren.</span><span class="sxs-lookup"><span data-stu-id="9db11-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="9db11-151">Weitere Informationen zu diesen Eigenschaften und deren Verwendung finden Sie unter [MAPI-Adresstypen](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="9db11-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="9db11-152">Messaging-Benutzer kann eine Auflistung von deren Eigenschaften anzeigen, indem Sie die Eigenschaft **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9db11-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="9db11-153">**PR_DETAILS_TABLE** ist eine zeigt die Tabelle, die beschreibt das Layout einer im Dialogfeld Details oder eine der Eigenschaftenseiten, die Empfänger-Eigenschafteninformationen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9db11-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="9db11-154">MAPI erstellt Details Dialogfelder, wenn ein Client die [IAddrBook::Details](iaddrbook-details.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="9db11-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="9db11-155">Messaging User-Objekte kann weitere optionalen Eigenschaften zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="9db11-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="9db11-156">MAPI definiert viele Eigenschaften, die zusätzliche reagieren auf Informationen über ein messaging-Benutzer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9db11-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="9db11-157">Alle diese Eigenschaften sind Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="9db11-157">All of these properties are character strings.</span></span> <span data-ttu-id="9db11-158">Die folgende Liste enthält mehrere Eigenschaften häufig verwendet:</span><span class="sxs-lookup"><span data-stu-id="9db11-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="9db11-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9db11-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9db11-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9db11-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9db11-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9db11-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9db11-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9db11-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="9db11-166">Eine vollständige Liste der Eigenschaften finden Sie unter [Zuordnen von kanonischen Eigenschaftennamen MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="9db11-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9db11-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9db11-167">See also</span></span>



[<span data-ttu-id="9db11-168">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9db11-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

