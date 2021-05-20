---
title: Erstellen einer Empfängerliste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428214"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="25d16-103">Erstellen einer Empfängerliste</span><span class="sxs-lookup"><span data-stu-id="25d16-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="25d16-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25d16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25d16-105">Eine Empfängerliste ist eine [ADRLIST-Struktur,](adrlist.md) die ein Array von Eigenschaftenwertstrukturen für jeden Nachrichtenempfänger enthält – Ziel für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="25d16-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="25d16-106">Ein Empfänger kann einen menschlichen Benutzer, einen Computer oder einen Ordner darstellen.</span><span class="sxs-lookup"><span data-stu-id="25d16-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="25d16-107">Für alle zu sendenden Nachrichten ist mindestens ein Empfänger erforderlich, der den Namenauflösungsprozess durchgef?nnen hat– ein Prozess, mit dem sichergestellt wird, dass die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft im Eigenschaftenwertarray des Empfängers enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="25d16-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="25d16-108">Die Eigenschaften eines Empfängers sind eine Kombination aus Adressbucheigenschaften und Nachrichteneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="25d16-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="25d16-109">Empfängereigenschaften können entweder auf alle Nachrichten für einen bestimmten Empfänger oder nur auf die aktuelle Nachricht angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="25d16-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="25d16-110">Sowohl Nachrichtenspeicher als auch Transportanbieter können Empfängereigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="25d16-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="25d16-111">Jeder Empfänger muss über einen Kernsatz von Eigenschaften in seinem Eigenschaftswertarray verfügen, bis die Nachricht gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="25d16-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="25d16-112">Zu den erforderlichen Empfängereigenschaften gehören:</span><span class="sxs-lookup"><span data-stu-id="25d16-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="25d16-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25d16-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25d16-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25d16-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25d16-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25d16-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25d16-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="25d16-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="25d16-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25d16-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="25d16-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="25d16-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="25d16-119">Diese Eigenschaften werden verwendet, um auf den Empfänger zu zugreifen, Nachrichten an ihn zu senden und ihn mit anderen zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="25d16-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="25d16-120">Nicht alle diese Eigenschaften müssen sofort verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="25d16-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="25d16-121">Sie können einen Empfänger zunächst hinzufügen, ohne dessen Eintrags-ID zu kennen, und diese Eigenschaft im Namenauflösungsprozess zuweisen.</span><span class="sxs-lookup"><span data-stu-id="25d16-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="25d16-122">Rufen Sie vor dem Senden einer Nachricht [IAddrBook::ResolveName](iaddrbook-resolvename.md) auf, um sicherzustellen, dass alle Empfänger in der Empfängerliste aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="25d16-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="25d16-123">Weitere Informationen finden Sie unter [Resolving a Recipient Name](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="25d16-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="25d16-124">Empfängerlisten können aus Nachrichtenbenutzern oder Verteilerlisteneinträgen in einem Adressbuchcontainer oder aus einmal erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="25d16-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="25d16-125">Einmalige Nachrichten sind Empfänger, die entweder als temporäre Einträge erstellt werden, die nur für die Adressierung einer einzelnen Nachricht oder als Einträge verwendet werden, die einem persönlichen Adressbuch hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="25d16-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="25d16-126">Das Format für eine eindeutige Eintrags-ID und -Adresse wird durch MAPI definiert.</span><span class="sxs-lookup"><span data-stu-id="25d16-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="25d16-127">Weitere Informationen zu diesen Formaten finden Sie unter [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="25d16-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="25d16-128">Sie können Benutzern das Erstellen ihrer Empfängerlisten ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="25d16-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="25d16-129">Nur mit Einträgen aus dem Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="25d16-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="25d16-130">Nur mit einmalen Einträgen.</span><span class="sxs-lookup"><span data-stu-id="25d16-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="25d16-131">Mit einer Kombination aus Adressbuchempfängern und Einmalempfängern.</span><span class="sxs-lookup"><span data-stu-id="25d16-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="25d16-132">**So erstellen Sie eine Empfängerliste mithilfe des Dialogfelds allgemeine Adresse**</span><span class="sxs-lookup"><span data-stu-id="25d16-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="25d16-133">Weisen Sie [einer ADRPARM-Struktur](adrparm.md) und einem Zeiger eine [ADRLIST-Struktur](adrlist.md) zu.</span><span class="sxs-lookup"><span data-stu-id="25d16-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="25d16-134">Null des Arbeitsspeichers in der **ADRPARM-Struktur,** und legen Sie den **ADRLIST-Zeiger** auf NULL.</span><span class="sxs-lookup"><span data-stu-id="25d16-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="25d16-135">Rufen [Sie IAddrBook::Address auf,](iaddrbook-address.md) um das Adressdialogfeld anzuzeigen und die **ADRPARM-Struktur** auffüllen.</span><span class="sxs-lookup"><span data-stu-id="25d16-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="25d16-136">Rufen [Sie IMessage::ModifyRecipients auf,](imessage-modifyrecipients.md)und übergeben Sie den **ADRLIST-Zeiger.**</span><span class="sxs-lookup"><span data-stu-id="25d16-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="25d16-137">Diese Struktur enthält die Eigenschaften der einzelnen vom Benutzer ausgewählten Empfänger.</span><span class="sxs-lookup"><span data-stu-id="25d16-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="25d16-138">**So erstellen Sie eine Empfängerliste programmgesteuert**</span><span class="sxs-lookup"><span data-stu-id="25d16-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="25d16-139">Weisen Sie **eine ADRLIST-Struktur** zu, die eine [ADRENTRY-Struktur](adrentry.md) für jeden empfänger enthält, der in die Liste aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="25d16-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="25d16-140">Machen Sie **jede ADRENTRY-Struktur** so groß, dass jede der erforderlichen Eigenschaften und PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="25d16-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="25d16-141">Legen Sie für jeden Empfänger das Eigenschaftswertarray für das **Element aEntries** in der **ADRLIST-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="25d16-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="25d16-142">Rufen [Sie IMessage::ModifyRecipients](imessage-modifyrecipients.md) mit dem MODRECIP_ADD auf.</span><span class="sxs-lookup"><span data-stu-id="25d16-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

