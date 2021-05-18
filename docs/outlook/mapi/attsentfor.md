---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408838"
---
# <a name="attsentfor"></a><span data-ttu-id="518c0-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="518c0-103">attSentFor</span></span>

  
  
<span data-ttu-id="518c0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="518c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="518c0-105">Das **attSentFor-Attribut** wird als gezählte Zeichenfolgen codiert, die ende-zu-Ende gelegt werden.</span><span class="sxs-lookup"><span data-stu-id="518c0-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="518c0-106">Das Format für **attSentFor** lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="518c0-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="518c0-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="518c0-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="518c0-108">display-name-length display-name address-length  _email-address_</span><span class="sxs-lookup"><span data-stu-id="518c0-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="518c0-109">_E-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="518c0-109">_email-address_</span></span>
  
> <span data-ttu-id="518c0-110">typ **:** address</span><span class="sxs-lookup"><span data-stu-id="518c0-110">type **:** address</span></span> 
    
<span data-ttu-id="518c0-111">Im Gegensatz zu anderen Längenwerten sind die Anzeigenamelänge und die Adresslänge nicht signierte 16-Bit-Werte anstelle von nicht signierten langen Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="518c0-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="518c0-112">Sie enthalten jedoch weiterhin das Beenden von Nullzeichen.</span><span class="sxs-lookup"><span data-stu-id="518c0-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="518c0-113">Der Typ und die Adresszeichenfolgen im  _E-Mail-Adresseintrag_ werden durch einen literalen Doppelpunkt getrennt (:) zeichen, z. B. "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="518c0-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="518c0-114">Nur der kombinierte Typ **:** adresszeichenfolge ist null-terminated.</span><span class="sxs-lookup"><span data-stu-id="518c0-114">Only the combined type **:** address string is null-terminated.</span></span>
  

