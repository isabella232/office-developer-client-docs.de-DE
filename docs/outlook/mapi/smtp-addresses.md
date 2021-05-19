---
title: SMTP-Adressen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419625"
---
# <a name="smtp-addresses"></a><span data-ttu-id="1166d-103">SMTP-Adressen</span><span class="sxs-lookup"><span data-stu-id="1166d-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="1166d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1166d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1166d-105">Das Format von SMTP-E-Mail-Adressen ist in RFC 822 definiert.</span><span class="sxs-lookup"><span data-stu-id="1166d-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="1166d-106">MAPI-Komponenten sollten alle Adressen behandeln, die diesem Standard entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1166d-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="1166d-107">Es gibt jedoch eine bestimmte Form von RFC 822-Adresse, die MAPI-Adressen am besten codiert:</span><span class="sxs-lookup"><span data-stu-id="1166d-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="1166d-108">_Anzeigename_ **\<** _E-Mail-Adresse_**\>**</span><span class="sxs-lookup"><span data-stu-id="1166d-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="1166d-109">Die eckigen Klammern sind als Literale enthalten.</span><span class="sxs-lookup"><span data-stu-id="1166d-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="1166d-110">Leerstellen werden häufig in Anzeigenamen verwendet. sie müssen nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1166d-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="1166d-111">Eine typische Adresse kann wie diese aussehen, die zu einem der Mitautoren von RFC 1521 gehört:</span><span class="sxs-lookup"><span data-stu-id="1166d-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="1166d-112">Nataniel Borenstein \< nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="1166d-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="1166d-113">Wenn der Anzeigename Zeichen enthält, die in SMTP-Adressen eine besondere Bedeutung haben, z. B. oder @, sollte der gesamte Anzeigename in doppelte \< Anführungszeichen gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1166d-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="1166d-114">Wenn die Gesamtlänge der E-Mail-Adresse plus Anzeigename bei ausgehenden E-Mails 255 Zeichen überschreitet, sollte der Anzeigename gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1166d-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="1166d-115">Die Teile einer SMTP-Adresszuordnung werden den MAPI-Eigenschaften wie folgt gegliedert:</span><span class="sxs-lookup"><span data-stu-id="1166d-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="1166d-116">**SMTP-Adresskomponente**</span><span class="sxs-lookup"><span data-stu-id="1166d-116">**SMTP address component**</span></span>|<span data-ttu-id="1166d-117">**MAPI-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="1166d-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1166d-118">_Anzeigename_ für alle Empfänger</span><span class="sxs-lookup"><span data-stu-id="1166d-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="1166d-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1166d-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="1166d-120">_Anzeigename für_ Feld "Von"</span><span class="sxs-lookup"><span data-stu-id="1166d-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="1166d-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1166d-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="1166d-122">_Anzeigename für_ das Feld "Sender"</span><span class="sxs-lookup"><span data-stu-id="1166d-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="1166d-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1166d-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="1166d-124">_E-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="1166d-124">_email-address_</span></span> <br/> |<span data-ttu-id="1166d-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1166d-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="1166d-126">implizit, immer "SMTP"</span><span class="sxs-lookup"><span data-stu-id="1166d-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="1166d-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1166d-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="1166d-128">Wenn für eine Adresse in eingehenden E-Mails kein Anzeigename vorhanden ist, sollte stattdessen die gesamte E-Mail-Adresse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1166d-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="1166d-129">Der Adresstyp ist immer SMTP.</span><span class="sxs-lookup"><span data-stu-id="1166d-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="1166d-130">Empfängereigenschaften werden aus der Empfängertabelle der #A0 übernommen. Absendereigenschaften werden aus der Nachricht selbst übernommen.</span><span class="sxs-lookup"><span data-stu-id="1166d-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

