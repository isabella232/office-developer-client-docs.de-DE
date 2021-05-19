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
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419877"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="8a8f8-103">Vorbereiten eines Empfängers</span><span class="sxs-lookup"><span data-stu-id="8a8f8-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="8a8f8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a8f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a8f8-105">Eine Clientanwendung bereitet Empfänger vor, indem sie ihre kurzfristigen Eintragsbezeichner in langfristige Eintragsbezeichner konvertieren und möglicherweise Eigenschaften hinzufügen, ändern oder neu anordnen.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="8a8f8-106">Sie können Empfänger vorbereiten, die Teil einer Empfängerliste sind, für eine Nachricht oder Empfänger, die nicht mit einer Nachricht in Zusammenhang stehen.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="8a8f8-107">In der Regel rufen Clients [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) direkt auf, um bezeichner für kurzfristige Eingaben in langfristige Eintragsbezeichner für Empfänger zu übersetzen, die im Dialogfeld allgemeine Adresse enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="8a8f8-108">Bei Empfängern, die einer ausgehenden Nachricht zugeordnet sind, wird die Empfängervorbereitung durch den Namensauflösungsprozess behandelt.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="8a8f8-109">Um eine Liste der Empfänger vorzubereiten, rufen Sie **IAddrBook::P repareRecips auf.**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="8a8f8-110">**PrepareRecips** akzeptiert eine [ADRLIST-Struktur](adrlist.md) und eine Liste von Eigenschaftstags.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="8a8f8-111">Die **ADRLIST-Struktur** enthält die empfänger, die vorbereitet werden sollen, während die Eigenschaftstagliste Eigenschaften darstellt, die von jedem Empfänger unterstützt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="8a8f8-112">**PrepareRecips** versucht, die Eigenschaften, die in der Eigenschaftstagliste enthalten sind, am Anfang der **ADRLIST-Struktur zu** platzieren.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="8a8f8-113">Wenn eine der Eigenschaften in der Liste in der **ADRLIST-Struktur** fehlt, ruft MAPI den Adressbuchanbieter auf, diese zu liefern.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="8a8f8-114">Wenn Sie nur nach langfristigen Eintragsbezeichnern suchen müssen, übergeben Sie NULL für den _lpSPropTagArray-Parameter._</span><span class="sxs-lookup"><span data-stu-id="8a8f8-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="8a8f8-115">Angenommen, Sie arbeiten mit fünf Empfängern.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="8a8f8-116">Alle fünf Empfänger werden in der **ADRLIST-Struktur** mit den folgenden Eigenschaften in der folgenden Reihenfolge angezeigt:</span><span class="sxs-lookup"><span data-stu-id="8a8f8-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="8a8f8-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8a8f8-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="8a8f8-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8a8f8-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="8a8f8-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8a8f8-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="8a8f8-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8a8f8-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="8a8f8-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8a8f8-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="8a8f8-122">Drei weitere Eigenschaften sind in der **ADRLIST-Struktur** für die ersten beiden Empfänger enthalten.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="8a8f8-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8a8f8-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="8a8f8-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8a8f8-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="8a8f8-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8a8f8-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="8a8f8-126">Da alle Empfänger als erste drei Eigenschaften **PR_ADDRTYPE**, **PR_ENTRYID** und **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)) verfügen müssen, erstellen Sie ein Eigenschaftentagarray mit diesen Eigenschaften und übergeben es und die **ADRLIST-Struktur** an **PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="8a8f8-127">**PrepareRecips** ruft die **IMAPIProp::GetProps-Methode** jedes Empfängers auf, um PR_HOME_TELEPHONE_NUMBER **abzurufen,** da sie derzeit nicht Teil der **ADRLIST-Struktur** ist.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="8a8f8-128">Wenn **PrepareRecips** zurückgegeben wird, stellt die Empfängerliste eine zusammengeführte Liste von Empfängern dar, deren Eigenschaften in der **ADRLIST-Struktur** für jeden Empfänger zuerst angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="8a8f8-129">Die Empfängerliste für empfänger 1 und 2 enthält Eigenschaften in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="8a8f8-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="8a8f8-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="8a8f8-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="8a8f8-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="8a8f8-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="8a8f8-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="8a8f8-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="8a8f8-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="8a8f8-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="8a8f8-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="8a8f8-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="8a8f8-140">Die Empfängerliste für empfänger 3, 4 und 5 enthält Eigenschaften in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="8a8f8-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="8a8f8-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="8a8f8-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="8a8f8-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="8a8f8-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="8a8f8-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="8a8f8-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="8a8f8-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="8a8f8-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="8a8f8-148">Rufen Sie als Alternative zum Aufrufen von **IAddrBook::P repareRecips** für die Arbeit mit Eigenschaften die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) und gegebenenfalls die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) jedes Empfängers auf.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="8a8f8-149">Wenn nur ein Empfänger beteiligt ist, ist beide Technik zufriedenstellend.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="8a8f8-150">Wenn jedoch mehrere Empfänger beteiligt sind, spart das Aufrufen von **PrepareRecips** anstelle der **IMAPIProp-Methoden** Zeit und, wenn Sie remote arbeiten, viele Remoteprozeduraufrufe.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="8a8f8-151">**PrepareRecips** verarbeitet alle Empfänger in einem einzigen Anruf, **während GetProps** und **SetProps** einen Aufruf für jeden Empfänger erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a8f8-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

