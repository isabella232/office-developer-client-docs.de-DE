---
title: Vorbereiten eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 51241009262471bf30f7d71e3108b896bbce8df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795306"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="e5ece-103">Vorbereiten eines Empfängers</span><span class="sxs-lookup"><span data-stu-id="e5ece-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="e5ece-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5ece-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5ece-105">Eine Clientanwendung vorbereitet Empfänger ihre kurzfristige-Eintragsbezeichner in langfristige-Eintragsbezeichner konvertieren und möglicherweise hinzufügen, ändern oder Neuanordnen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e5ece-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="e5ece-106">Sie können die Empfänger an, die sind Bestandteil einer Empfängerliste für eine Nachricht oder Empfänger, die nicht im Zusammenhang mit einer Nachricht sind vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="e5ece-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="e5ece-107">In der Regel rufen Clients [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) direkt um kurzfristige-Eintragsbezeichner in langfristige-Eintragsbezeichner für Empfänger zu übersetzen, die im Dialogfeld allgemeine Adresse enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e5ece-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="e5ece-108">Für den Empfänger an, die eine ausgehende Nachricht zugeordnet sind, wird die Empfänger zur Vorbereitung von Vorgang der Lösung behandelt.</span><span class="sxs-lookup"><span data-stu-id="e5ece-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="e5ece-109">Rufen Sie auf, um eine Liste von Empfängern vorzubereiten, **IAddrBook::PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="e5ece-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="e5ece-110">**PrepareRecips** akzeptiert eine [ADRLIST](adrlist.md) -Struktur und eine Liste der Eigenschaftentags.</span><span class="sxs-lookup"><span data-stu-id="e5ece-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="e5ece-111">Die **ADRLIST** -Datenstruktur enthält die Empfänger vorbereitet werden, während die Eigenschaftenliste Tag Eigenschaften darstellt, die jeden Empfänger unterstützt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5ece-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="e5ece-112">**PrepareRecips** versucht, die Eigenschaften, die in der Eigenschaftenliste Tag am Anfang der Struktur **ADRLIST** enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e5ece-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="e5ece-113">Wenn eine der Eigenschaften in der Liste aus der Struktur **ADRLIST** fehlen, ruft MAPI--Adressbuchanbieter, um diese bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e5ece-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="e5ece-114">Wenn Sie nur für langfristige-Eintragsbezeichner überprüfen möchten, übergeben Sie NULL für den Parameter _LpSPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="e5ece-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="e5ece-115">Angenommen Sie, dass Sie mit fünf Empfänger arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e5ece-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="e5ece-116">Alle fünf Empfänger in der **ADRLIST** -Struktur mit den folgenden Eigenschaften in der folgenden Reihenfolge angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="e5ece-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="e5ece-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5ece-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="e5ece-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5ece-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="e5ece-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5ece-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="e5ece-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5ece-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="e5ece-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5ece-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="e5ece-122">In der Struktur **ADRLIST** sind drei weitere Eigenschaften für die ersten beiden Empfänger enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5ece-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="e5ece-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5ece-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="e5ece-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5ece-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="e5ece-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5ece-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="e5ece-126">Da alle Empfänger benötigen, als die ersten drei Eigenschaften **PR_ADDRTYPE** **PR_ENTRYID**und **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), ein Tag-Array-Eigenschaft mit folgenden Eigenschaften erstellen und übergeben Sie und die zu **PrepareRecips** **ADRLIST** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e5ece-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="e5ece-127">**PrepareRecips** ruft jeden Empfänger **IMAPIProp::GetProps** -Methode, um **PR_HOME_TELEPHONE_NUMBER** abzurufen, da es nicht Teil der Struktur **ADRLIST** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e5ece-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="e5ece-128">Wenn **PrepareRecips** zurückgegeben wird, stellt die Empfängerliste eine Liste von Empfängern mit den Eigenschaften der **ADRLIST** -Struktur wie folgt aussehen für jeden Empfänger enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5ece-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="e5ece-129">Die Empfängerliste für Empfänger 1 und 2 enthält die Eigenschaften in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="e5ece-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="e5ece-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="e5ece-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="e5ece-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="e5ece-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="e5ece-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="e5ece-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="e5ece-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="e5ece-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="e5ece-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="e5ece-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="e5ece-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="e5ece-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="e5ece-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="e5ece-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="e5ece-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="e5ece-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="e5ece-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="e5ece-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="e5ece-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="e5ece-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="e5ece-140">Die Empfängerliste für Empfänger 3, 4 und 5 enthält die Eigenschaften in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="e5ece-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="e5ece-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="e5ece-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="e5ece-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="e5ece-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="e5ece-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="e5ece-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="e5ece-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="e5ece-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="e5ece-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="e5ece-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="e5ece-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="e5ece-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="e5ece-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="e5ece-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="e5ece-148">Rufen Sie als Alternative zum Aufrufen von **IAddrBook::PrepareRecips** arbeiten mit Eigenschaften des Empfängers [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode und, falls erforderlich, dessen [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e5ece-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="e5ece-149">Wenn nur ein Empfänger beteiligt ist, ist ein der Verfahren Standardkontingente.</span><span class="sxs-lookup"><span data-stu-id="e5ece-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="e5ece-150">Jedoch, wenn mehrere Empfänger beteiligt sind, **PrepareRecips** statt der **IMAPIProp** Methoden Aufrufen der Beschleunigung und, falls Sie viele Remoteprozeduraufrufe remote ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e5ece-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="e5ece-151">**PrepareRecips** verarbeitet alle Empfänger in einem einzigen Aufruf während **GetProps** und **SetProps** tätigen Sie einen Anruf für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="e5ece-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

