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
ms.openlocfilehash: cc7635c474b99898d59589f33fcf06cf24697378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795345"
---
# <a name="recipient-tables"></a><span data-ttu-id="8efed-103">Empfängertabellen</span><span class="sxs-lookup"><span data-stu-id="8efed-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="8efed-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8efed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8efed-105">Die Empfänger Tabelle enthält Informationen zu allen Empfängern für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8efed-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="8efed-106">Nachricht Anbieter implementieren Empfänger Tabellen und Clientanwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8efed-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="8efed-107">Clients tätigen eines Anrufs an die [IMessage::GetRecipientTable](imessage-getrecipienttable.md) -Methode zum Öffnen einer Empfänger Tabelle oder unterstützt, wenn die Nachricht vom Anbieter Speichern der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8efed-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="8efed-108">Clients Zugriff auf Empfänger Tabellen mit **OpenProperty** angeben **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) für die Eigenschaftentag und IID_IMAPITable für den Schnittstellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="8efed-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="8efed-109">Änderungen, die einer Tabelle Empfänger können durch Aufrufen der Methode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="8efed-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="8efed-110">Empfänger Tabellen ist eine andere Spalte festlegen, je nachdem, ob die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8efed-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="8efed-111">Die folgenden Eigenschaften bilden die erforderliche Spalte in Empfänger Tabellen festzulegen:</span><span class="sxs-lookup"><span data-stu-id="8efed-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="8efed-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8efed-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="8efed-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8efed-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="8efed-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8efed-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="8efed-115">Die optionalen Eigenschaften sind:</span><span class="sxs-lookup"><span data-stu-id="8efed-115">The optional properties are:</span></span>
  
- <span data-ttu-id="8efed-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8efed-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="8efed-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8efed-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="8efed-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8efed-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="8efed-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8efed-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="8efed-120">Gesendete Nachrichten sollte diese zusätzlichen Eigenschaften in einen Satz erforderliche Spalte enthalten:</span><span class="sxs-lookup"><span data-stu-id="8efed-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="8efed-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8efed-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="8efed-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8efed-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="8efed-123">Je nach der Implementierung eines Anbieters möglicherweise zusätzliche Spalten, wie **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) und [ENTRYID](entryid.md), in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8efed-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="8efed-124">Eine beliebige Nachricht Speicher-Anbieter, der Nachrichtenübermittlung unterstützt – wie das STORE_SUBMIT_OK Bit festgelegt wird, in der Anbieter **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft angegeben – bieten Unterstützung für eine bestimmte Gruppe von Einschränkungen in einer Implementierung eines Empfängers Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8efed-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="8efed-125">**Und**, **oder**, vorhanden, und Suchkriterien in Eigenschaft gehören zu den Arten von Einschränkungen, die an Empfänger Tabelle Benutzer verfügbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="8efed-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="8efed-126">Nur die Operatoren gleich und ungleich müssen in der eigenschaftseinschränkung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8efed-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="8efed-127">Diese Einschränkung Zusammenarbeit müssen mit den folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8efed-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="8efed-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="8efed-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="8efed-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8efed-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="8efed-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="8efed-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="8efed-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="8efed-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="8efed-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="8efed-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8efed-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8efed-133">See also</span></span>



[<span data-ttu-id="8efed-134">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="8efed-134">MAPI Tables</span></span>](mapi-tables.md)

