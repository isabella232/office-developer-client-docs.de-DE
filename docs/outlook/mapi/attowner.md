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
# <a name="attowner"></a><span data-ttu-id="95762-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="95762-103">attOwner</span></span>

  
  
<span data-ttu-id="95762-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95762-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95762-105">Das **attOwner-Attribut** wird als gezählte Zeichenfolgen codiert, die ende-zu-Ende gelegt werden.</span><span class="sxs-lookup"><span data-stu-id="95762-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="95762-106">Das Format für **attOwner** lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="95762-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="95762-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="95762-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="95762-108">display-name-length display-name address-length  _email-address_</span><span class="sxs-lookup"><span data-stu-id="95762-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="95762-109">_E-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="95762-109">_email-address_</span></span>
  
> <span data-ttu-id="95762-110">typ **:** address</span><span class="sxs-lookup"><span data-stu-id="95762-110">type **:** address</span></span> 
    
<span data-ttu-id="95762-111">Im Gegensatz zu anderen Längenwerten sind die Anzeigenamelänge und die Adresslänge nicht signierte 16-Bit-Werte anstelle von nicht signierten langen Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="95762-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="95762-112">Sie enthalten jedoch weiterhin das Beenden von Nullzeichen.</span><span class="sxs-lookup"><span data-stu-id="95762-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="95762-113">Der Typ und die Adresszeichenfolgen im  _E-Mail-Adresseintrag_ werden durch einen literalen Doppelpunkt getrennt (:) zeichen, z. B. "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="95762-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="95762-114">Nur der kombinierte Typ **:** adresszeichenfolge ist null-terminated.</span><span class="sxs-lookup"><span data-stu-id="95762-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="95762-115">Die Zuordnung von MAPI-Eigenschaften zum **attOwner-Attribut** hängt von der Nachrichtenklasse der zu codierten Nachricht ab.</span><span class="sxs-lookup"><span data-stu-id="95762-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

