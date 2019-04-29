---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427654"
---
# <a name="attowner"></a><span data-ttu-id="e1b19-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="e1b19-103">attOwner</span></span>

  
  
<span data-ttu-id="e1b19-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1b19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1b19-105">Das **attOwner** -Attribut wird als gezählte Zeichenfolge mit End-to-End-Codierung codiert.</span><span class="sxs-lookup"><span data-stu-id="e1b19-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="e1b19-106">Das Format für **attOwner** lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e1b19-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="e1b19-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="e1b19-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="e1b19-108">Anzeigename-length-Anzeigename-Adresslänge- _e-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="e1b19-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="e1b19-109">_e-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="e1b19-109">_email-address_</span></span>
  
> <span data-ttu-id="e1b19-110">Typ **:** Address</span><span class="sxs-lookup"><span data-stu-id="e1b19-110">type **:** address</span></span> 
    
<span data-ttu-id="e1b19-111">Im Gegensatz zu anderen Längenwerten sind die Anzeigename-length und die Address-length nicht signierte lange ganze Zahlen, 16-Bit-Werte ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="e1b19-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="e1b19-112">Sie enthalten jedoch weiterhin NULL-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e1b19-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="e1b19-113">Die Typ-und Adress Zeichenfolgen im _e-Mail-Adress_ Eintrag werden durch einen Literalwert (:) Zeichen, wie "SMTP:Joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="e1b19-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="e1b19-114">Nur der kombinierte Typ **:** Address String is null-terminated.</span><span class="sxs-lookup"><span data-stu-id="e1b19-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="e1b19-115">Die Zuordnung von MAPI-Eigenschaften zum **attOwner** -Attribut hängt von der Nachrichtenklasse der zu codierenden Nachricht ab.</span><span class="sxs-lookup"><span data-stu-id="e1b19-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

