---
title: Erstellen einer Empfängerliste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa23377a8b080ae9dac3e31dfa137ca03a242c74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791501"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="132f9-103">Erstellen einer Empfängerliste</span><span class="sxs-lookup"><span data-stu-id="132f9-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="132f9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="132f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="132f9-105">Eine Empfängerliste ist eine [ADRLIST](adrlist.md) -Struktur, die ein Array der Eigenschaft Wert Strukturen für jeden Empfänger der Nachricht enthält – Ziel für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="132f9-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="132f9-106">Ein Empfänger kann ein human Benutzer, einen Computer oder einen Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="132f9-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="132f9-107">Alle Nachrichten gesendet werden erfordern mindestens einen Empfänger, die durch den Namen Lösung Prozess wurde – ein Prozess zum sicherstellen, dass die Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) Wert Array-Eigenschaft gehören des Empfängers enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="132f9-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="132f9-108">Die Eigenschaften eines Empfängers sind eine Kombination von Adressbucheigenschaften und Nachrichteneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="132f9-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="132f9-109">Empfängereigenschaften können auf alle Nachrichten für einen bestimmten Empfänger oder nur für die aktuelle Nachricht anwenden.</span><span class="sxs-lookup"><span data-stu-id="132f9-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="132f9-110">Beide Nachrichtenspeicher und Transportanbieter Empfängereigenschaften festlegen können.</span><span class="sxs-lookup"><span data-stu-id="132f9-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="132f9-111">Jeden Empfänger muss eine Kerngruppe von Eigenschaften des Arrays der Eigenschaft Wert durch die Zeit haben, die die Nachricht gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="132f9-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="132f9-112">Die erforderlichen Empfängereigenschaften beinhaltet:</span><span class="sxs-lookup"><span data-stu-id="132f9-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="132f9-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="132f9-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="132f9-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="132f9-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="132f9-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="132f9-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="132f9-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="132f9-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="132f9-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="132f9-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="132f9-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="132f9-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="132f9-119">Diese Eigenschaften werden verwendet, für den Zugriff auf den Empfänger senden von Nachrichten an diese, und es mit anderen Personen verglichen.</span><span class="sxs-lookup"><span data-stu-id="132f9-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="132f9-120">Nicht alle diese Eigenschaften müssen sofort verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="132f9-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="132f9-121">Sie können einen Empfänger zunächst hinzufügen ohne die Eintrags-ID auf Vorgang der Lösung, dieser Eigenschaft zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="132f9-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="132f9-122">Bevor Sie eine Nachricht senden, rufen Sie zu einem bestimmten Zeitpunkt [IAddrBook::ResolveName](iaddrbook-resolvename.md) , um sicherzustellen, dass alle Empfänger in der Empfängerliste aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="132f9-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="132f9-123">Weitere Informationen finden Sie unter [Auflösen von Namen Empfänger](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="132f9-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="132f9-124">Empfängerlisten können von Benutzern oder Verteilung Listeneinträge in einem Adressbuchcontainer messaging oder Fly erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="132f9-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="132f9-125">Fly sind Empfänger, die erstellt werden, entweder als temporäre Einträge aus, die nur zum Umgang mit einer Nachricht verwendet werden oder als Einträge, ein persönliches Adressbuch hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="132f9-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="132f9-126">Das Format für einen einmaligen Eintrags-ID und eine Adresse wird durch MAPI definiert.</span><span class="sxs-lookup"><span data-stu-id="132f9-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="132f9-127">Weitere Informationen zu diesen Formaten finden Sie unter [Einmal-Adressen](one-off-addresses.md) und [Einmaligen-Eintragsbezeichner](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="132f9-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="132f9-128">Sie können Benutzer ihre Empfängerlisten erstellen können:</span><span class="sxs-lookup"><span data-stu-id="132f9-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="132f9-129">Nur mit den Einträgen aus dem Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="132f9-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="132f9-130">Nur bei einmaligen Einträge.</span><span class="sxs-lookup"><span data-stu-id="132f9-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="132f9-131">Mit einer Kombination von Address Book Empfänger und Fly.</span><span class="sxs-lookup"><span data-stu-id="132f9-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="132f9-132">**Eine allgemeine Adresse im Dialogfeld Empfängerliste erstellen**</span><span class="sxs-lookup"><span data-stu-id="132f9-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="132f9-133">Weisen Sie eine [ADRPARM](adrparm.md) -Struktur und einen Zeiger auf eine [ADRLIST](adrlist.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="132f9-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="132f9-134">0 (null) in der Struktur **ADRPARM** Speicher und den **ADRLIST** Zeiger auf NULL festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="132f9-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="132f9-135">Rufen Sie [IAddrBook::Address](iaddrbook-address.md) , um das Dialogfeld Adresse anzeigen, und füllen Sie die **ADRPARM** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="132f9-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="132f9-136">Rufen Sie [IMessage::ModifyRecipients](imessage-modifyrecipients.md), übergeben den Zeiger **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="132f9-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="132f9-137">Diese Struktur enthält die Eigenschaften der einzelnen der vom Benutzer ausgewählten Empfänger.</span><span class="sxs-lookup"><span data-stu-id="132f9-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="132f9-138">**So erstellen Sie programmgesteuert eine Empfängerliste**</span><span class="sxs-lookup"><span data-stu-id="132f9-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="132f9-139">Reservieren Sie eine **ADRLIST** -Struktur, die enthält eine [ADRENTRY](adrentry.md) -Struktur für die einzelnen Empfänger an, die in der Liste enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="132f9-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="132f9-140">Stellen Sie jede **ADRENTRY** Struktur groß genug für alle erforderlichen Eigenschaften und **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="132f9-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="132f9-141">Legen Sie für jeden Empfänger des Arrays der Eigenschaft Wert für **aEntries** Mitglied in der **ADRLIST** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="132f9-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="132f9-142">Rufen Sie [IMessage::ModifyRecipients](imessage-modifyrecipients.md) mit der MODRECIP_ADD-Flag.</span><span class="sxs-lookup"><span data-stu-id="132f9-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

