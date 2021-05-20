---
title: Empfängertabellen
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
# <a name="recipient-tables"></a><span data-ttu-id="0587d-103">Empfängertabellen</span><span class="sxs-lookup"><span data-stu-id="0587d-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="0587d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0587d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0587d-105">Die Empfängertabelle enthält Informationen zu allen Empfängern für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0587d-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="0587d-106">Nachrichtenspeicheranbieter implementieren Empfängertabellen, und Clientanwendungen verwenden sie.</span><span class="sxs-lookup"><span data-stu-id="0587d-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="0587d-107">Clients greifen auf eine Empfängertabelle zu, indem sie die [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) aufrufen oder die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) aufrufen, wenn sie vom Nachrichtenspeicheranbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="0587d-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="0587d-108">Clients greifen mit **OpenProperty** auf Empfängertabellen zu, indem **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) für das Eigenschaftstag und IID_IMAPITable für den Schnittstellenbezeichner angeben.</span><span class="sxs-lookup"><span data-stu-id="0587d-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="0587d-109">Änderungen an einer Empfängertabelle können durch Aufrufen der [IMessage::ModifyRecipients-Methode vorgenommen](imessage-modifyrecipients.md) werden.</span><span class="sxs-lookup"><span data-stu-id="0587d-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="0587d-110">Empfängertabellen haben einen anderen Spaltensatz, je nachdem, ob die Nachricht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="0587d-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="0587d-111">Die folgenden Eigenschaften stellen den erforderlichen Spaltensatz in Empfängertabellen zusammen:</span><span class="sxs-lookup"><span data-stu-id="0587d-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="0587d-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0587d-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="0587d-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0587d-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="0587d-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0587d-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="0587d-115">Die optionalen Eigenschaften sind:</span><span class="sxs-lookup"><span data-stu-id="0587d-115">The optional properties are:</span></span>
  
- <span data-ttu-id="0587d-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0587d-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="0587d-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0587d-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="0587d-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0587d-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="0587d-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0587d-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="0587d-120">Übermittelte Nachrichten sollten die folgenden zusätzlichen Eigenschaften in ihren erforderlichen Spaltensatz enthalten:</span><span class="sxs-lookup"><span data-stu-id="0587d-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="0587d-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0587d-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="0587d-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0587d-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="0587d-123">Abhängig von der Implementierung eines Anbieters können zusätzliche Spalten wie **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) und [ENTRYID](entryid.md)in der Tabelle enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="0587d-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="0587d-124">Jeder Nachrichtenspeicheranbieter, der die Nachrichtenübertragung unterstützt – wie durch das **STORE_SUBMIT_OK-Bit** angegeben, das in der PR_STORE_SUPPORT_MASK ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Anbieters festgelegt ist – sollte Unterstützung für bestimmte Einschränkungen in einer Empfängertabelle bieten.</span><span class="sxs-lookup"><span data-stu-id="0587d-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="0587d-125">And , **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span><span class="sxs-lookup"><span data-stu-id="0587d-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="0587d-126">Nur die Operatoren equal und not equal müssen für die Eigenschaftseinschränkung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0587d-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="0587d-127">Diese Einschränkungen müssen mit den folgenden Eigenschaften funktionieren:</span><span class="sxs-lookup"><span data-stu-id="0587d-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="0587d-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="0587d-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="0587d-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0587d-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="0587d-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="0587d-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="0587d-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="0587d-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="0587d-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="0587d-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0587d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0587d-133">See also</span></span>



[<span data-ttu-id="0587d-134">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="0587d-134">MAPI Tables</span></span>](mapi-tables.md)

