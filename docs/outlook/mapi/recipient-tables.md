---
title: Empfänger Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437287"
---
# <a name="recipient-tables"></a><span data-ttu-id="36091-103">Empfänger Tabellen</span><span class="sxs-lookup"><span data-stu-id="36091-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="36091-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36091-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36091-105">Die Empfängertabelle enthält Informationen zu allen Empfängern einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="36091-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="36091-106">Nachrichtenspeicher Anbieter implementieren Empfänger Tabellen und Clientanwendungen verwenden Sie.</span><span class="sxs-lookup"><span data-stu-id="36091-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="36091-107">Clients greifen auf eine Empfängertabelle zu, indem Sie die [IMessage::](imessage-getrecipienttable.md) getrecipientable-Methode aufrufen oder wenn der Nachrichtenspeicher Anbieter Sie unterstützt, an die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="36091-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="36091-108">Clients greifen auf Empfänger Tabellen \*\*\*\* mit OpenProperty zu, indem Sie **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md)) für das Property-Tag und IID_IMAPITable für den Schnittstellenbezeichner angeben.</span><span class="sxs-lookup"><span data-stu-id="36091-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="36091-109">Änderungen an einer Empfängertabelle können durch Aufrufen der [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode erfolgen.</span><span class="sxs-lookup"><span data-stu-id="36091-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="36091-110">Empfänger Tabellen haben unterschiedliche Spaltensätze, je nachdem, ob die Nachricht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="36091-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="36091-111">Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in Empfänger Tabellen:</span><span class="sxs-lookup"><span data-stu-id="36091-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="36091-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36091-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="36091-113">**PR_RECIPIENT_TYPE** ([Pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36091-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="36091-114">**PR_ROWID** ([Pidtagrowid (](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36091-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="36091-115">Die optionalen Eigenschaften sind:</span><span class="sxs-lookup"><span data-stu-id="36091-115">The optional properties are:</span></span>
  
- <span data-ttu-id="36091-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36091-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="36091-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36091-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="36091-118">**PR_SPOOLER_STATUS** ([Pidtagspoolerstatus (](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36091-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="36091-119">**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36091-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="36091-120">ÜberMittelte Nachrichten sollten diese zusätzlichen Eigenschaften in den erforderlichen Spaltensatz aufnehmen:</span><span class="sxs-lookup"><span data-stu-id="36091-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="36091-121">**PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36091-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="36091-122">**PR_RESPONSIBILITY** ([Pidtagresponsibility (](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36091-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="36091-123">Abhängig von der Implementierung eines Anbieters können zusätzliche Spalten wie **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) und [Entry](entryid.md)-out in der Tabelle enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="36091-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="36091-124">Jeder Nachrichtenspeicher Anbieter, der die Nachrichtenübertragung unterstützt, wie in dem STORE_SUBMIT_OK-Bit angegeben, das in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Anbieters festgelegt ist, sollte Unterstützung für eine bestimmte Gruppe von Einschränkungen in einer Empfänger Tabellen Implementierung.</span><span class="sxs-lookup"><span data-stu-id="36091-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="36091-125">Die **and**-, **or**-, exist-und Property-Einschränkungen gehören zu den Arten von Einschränkungen, die für Empfänger Tabellen Benutzer verfügbar sein sollten.</span><span class="sxs-lookup"><span data-stu-id="36091-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="36091-126">Nur die Operatoren EQUAL und ungleich werden für die Eigenschaftseinschränkung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36091-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="36091-127">Diese Einschränkungen müssen mit den folgenden Eigenschaften funktionieren:</span><span class="sxs-lookup"><span data-stu-id="36091-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="36091-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="36091-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="36091-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36091-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="36091-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="36091-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="36091-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="36091-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="36091-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="36091-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36091-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36091-133">See also</span></span>



[<span data-ttu-id="36091-134">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="36091-134">MAPI Tables</span></span>](mapi-tables.md)

