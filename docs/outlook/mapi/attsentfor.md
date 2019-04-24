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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318116"
---
# <a name="attsentfor"></a><span data-ttu-id="fa644-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="fa644-103">attSentFor</span></span>

  
  
<span data-ttu-id="fa644-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa644-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa644-105">Das **attSentFor** -Attribut wird als gezählte Zeichenfolge mit End-to-End-Codierung codiert.</span><span class="sxs-lookup"><span data-stu-id="fa644-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="fa644-106">Das Format für **attSentFor** lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fa644-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="fa644-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="fa644-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="fa644-108">Anzeigename-length-Anzeigename-Adresslänge- _e-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="fa644-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="fa644-109">_e-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="fa644-109">_email-address_</span></span>
  
> <span data-ttu-id="fa644-110">Typ **:** Address</span><span class="sxs-lookup"><span data-stu-id="fa644-110">type **:** address</span></span> 
    
<span data-ttu-id="fa644-111">Im Gegensatz zu anderen Längenwerten sind die Anzeigename-length und die Address-length nicht signierte lange ganze Zahlen, 16-Bit-Werte ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="fa644-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="fa644-112">Sie enthalten jedoch weiterhin NULL-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fa644-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="fa644-113">Die Typ-und Adress Zeichenfolgen im _e-Mail-Adress_ Eintrag werden durch einen Literalwert (:) Zeichen, wie "SMTP:Joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="fa644-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="fa644-114">Nur der kombinierte Typ **:** Address String is null-terminated.</span><span class="sxs-lookup"><span data-stu-id="fa644-114">Only the combined type **:** address string is null-terminated.</span></span>
  

