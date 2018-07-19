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
ms.openlocfilehash: 9bc77e3226066dc88bbaf4f4efc324825add8919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795593"
---
# <a name="smtp-addresses"></a><span data-ttu-id="0db2d-103">SMTP-Adressen</span><span class="sxs-lookup"><span data-stu-id="0db2d-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="0db2d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0db2d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0db2d-105">Das Format der SMTP-e-Mail-Adressen ist in RFC 822 definiert.</span><span class="sxs-lookup"><span data-stu-id="0db2d-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="0db2d-106">MAPI-Komponenten sollte eine beliebige Adresse behandeln, die mit diesem Standard entspricht.</span><span class="sxs-lookup"><span data-stu-id="0db2d-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="0db2d-107">Es ist jedoch eine bestimmte Form des RFC 822-Adresse, die am besten MAPI-Adressen codiert:</span><span class="sxs-lookup"><span data-stu-id="0db2d-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="0db2d-108">_Anzeigename_ **\<** _e-Mail-Adresse_**\>**</span><span class="sxs-lookup"><span data-stu-id="0db2d-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="0db2d-109">Die spitzen Klammern sind als Literale enthalten.</span><span class="sxs-lookup"><span data-stu-id="0db2d-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="0db2d-110">Leerzeichen sind häufig in Anzeigenamen. Sie müssen nicht in Anführungszeichen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="0db2d-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="0db2d-111">Eine typische Adresse sieht aus wie dieser, der eines der Coauthors der RFC 1521 gehört:</span><span class="sxs-lookup"><span data-stu-id="0db2d-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="0db2d-112">Nathaniel Borenstein \<nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="0db2d-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="0db2d-113">Wenn der angezeigte Name Zeichen enthält, die in der SMTP-Adressen, z. B. besondere Bedeutung haben \< oder @, sollte der gesamte Anzeigename in doppelte Anführungszeichen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="0db2d-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="0db2d-114">Ausgehende Nachrichten Wenn die Gesamtlänge des plus die e-Mail-Adresse anzuzeigen Name länger als 255 Zeichen klicken Sie auf der Anzeigenamen gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="0db2d-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="0db2d-115">Die Teile der SMTP-Adresse wie folgt in MAPI-Eigenschaften zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="0db2d-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="0db2d-116">**SMTP-Adresse-Komponente**</span><span class="sxs-lookup"><span data-stu-id="0db2d-116">**SMTP address component**</span></span>|<span data-ttu-id="0db2d-117">**MAPI-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="0db2d-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0db2d-118">_Anzeigename_ für alle Empfänger</span><span class="sxs-lookup"><span data-stu-id="0db2d-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="0db2d-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0db2d-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="0db2d-120">_Anzeigename_ für Feld</span><span class="sxs-lookup"><span data-stu-id="0db2d-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="0db2d-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0db2d-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="0db2d-122">_Anzeigename_ für Feld Absender</span><span class="sxs-lookup"><span data-stu-id="0db2d-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="0db2d-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0db2d-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="0db2d-124">_e-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="0db2d-124">_email-address_</span></span> <br/> |<span data-ttu-id="0db2d-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0db2d-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="0db2d-126">implizite, immer "SMTP"</span><span class="sxs-lookup"><span data-stu-id="0db2d-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="0db2d-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0db2d-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="0db2d-128">Wenn kein Anzeigename für eine eingehende e-Mail-Adresse vorhanden ist, sollte die gesamte e-Mail-Adresse stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0db2d-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="0db2d-129">Der Adresstyp ist immer SMTP.</span><span class="sxs-lookup"><span data-stu-id="0db2d-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="0db2d-130">Empfängereigenschaften getroffen werden aus der MAPI-Nachricht Empfänger Tabelle; Absender Eigenschaften werden aus der Nachricht selbst übernommen.</span><span class="sxs-lookup"><span data-stu-id="0db2d-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

