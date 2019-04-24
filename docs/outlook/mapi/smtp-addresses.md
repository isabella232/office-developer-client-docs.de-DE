---
title: SMTP-Adressen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344562"
---
# <a name="smtp-addresses"></a><span data-ttu-id="0a72e-103">SMTP-Adressen</span><span class="sxs-lookup"><span data-stu-id="0a72e-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="0a72e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a72e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a72e-105">Das Format der SMTP-e-Mail-Adressen ist in RFC 822 definiert.</span><span class="sxs-lookup"><span data-stu-id="0a72e-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="0a72e-106">MAPI-Komponenten sollten jede Adresse behandeln, die diesem Standard entspricht.</span><span class="sxs-lookup"><span data-stu-id="0a72e-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="0a72e-107">Es gibt jedoch eine bestimmte Form der RFC 822-Adresse, die die MAPI-Adressen am besten codiert:</span><span class="sxs-lookup"><span data-stu-id="0a72e-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="0a72e-108">_Anzeigename_ **\<** _e-Mail-Adresse_**\>**</span><span class="sxs-lookup"><span data-stu-id="0a72e-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="0a72e-109">Die eckigen Klammern sind als Literale enthalten.</span><span class="sxs-lookup"><span data-stu-id="0a72e-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="0a72e-110">Leerzeichen sind in Anzeige Namen gebräuchlich. Sie müssen nicht zitiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a72e-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="0a72e-111">Eine typische Adresse könnte wie diese aussehen, die zu einem der Mitverfasser von RFC 1521 gehört:</span><span class="sxs-lookup"><span data-stu-id="0a72e-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="0a72e-112">Nathaniel Borenstein \<NSB@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="0a72e-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="0a72e-113">Wenn der Anzeigename Zeichen enthält, die eine besondere Bedeutung in SMTP-Adressen wie \< oder @ haben, sollte der gesamte Anzeigename in doppelte Anführungszeichen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="0a72e-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="0a72e-114">Wenn die Gesamtlänge der e-Mail-Adresse und der Anzeigename bei ausgehenden e-Mails 255 Zeichen überschreitet, sollte der Anzeigename gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="0a72e-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="0a72e-115">Die Teile einer SMTP-Adresse werden wie folgt in MAPI-Eigenschaften zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="0a72e-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="0a72e-116">**SMTP-Adresskomponente**</span><span class="sxs-lookup"><span data-stu-id="0a72e-116">**SMTP address component**</span></span>|<span data-ttu-id="0a72e-117">**MAPI-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="0a72e-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0a72e-118">_Anzeigename_ für alle Empfänger</span><span class="sxs-lookup"><span data-stu-id="0a72e-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="0a72e-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72e-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="0a72e-120">_Anzeigename_ für vom-Feld</span><span class="sxs-lookup"><span data-stu-id="0a72e-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="0a72e-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72e-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="0a72e-122">_Anzeigename_ für Absenderfeld</span><span class="sxs-lookup"><span data-stu-id="0a72e-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="0a72e-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72e-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="0a72e-124">_e-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="0a72e-124">_email-address_</span></span> <br/> |<span data-ttu-id="0a72e-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72e-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="0a72e-126">implizit, immer "SMTP"</span><span class="sxs-lookup"><span data-stu-id="0a72e-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="0a72e-127">**PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72e-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="0a72e-128">Wenn kein Anzeigename für eine Adresse bei eingehenden e-Mails vorhanden ist, sollte stattdessen die gesamte e-Mail-Adresse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a72e-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="0a72e-129">Der Adresstyp ist immer SMTP.</span><span class="sxs-lookup"><span data-stu-id="0a72e-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="0a72e-130">Empfänger Eigenschaften werden aus der Empfängertabelle der MAPI-Nachricht entnommen. Absender Eigenschaften werden aus der Nachricht selbst entnommen.</span><span class="sxs-lookup"><span data-stu-id="0a72e-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

