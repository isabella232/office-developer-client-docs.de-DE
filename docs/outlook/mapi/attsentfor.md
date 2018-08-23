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
ms.openlocfilehash: b292e65ddabcbe052832687a3dcf01658de5e379
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567475"
---
# <a name="attsentfor"></a><span data-ttu-id="51dae-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="51dae-103">attSentFor</span></span>

  
  
<span data-ttu-id="51dae-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51dae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51dae-105">Gezählte Zeichenfolgen End-to-End-festgelegten, wird das Attribut **AttSentFor** codiert.</span><span class="sxs-lookup"><span data-stu-id="51dae-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="51dae-106">Das Format für **AttSentFor** lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="51dae-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="51dae-107">**AttSentFor**:</span><span class="sxs-lookup"><span data-stu-id="51dae-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="51dae-108">Display Name Länge Anzeigename Adresse Länge- _e-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="51dae-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="51dae-109">_e-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="51dae-109">_email-address_</span></span>
  
> <span data-ttu-id="51dae-110">Adresse vom Typ **:**</span><span class="sxs-lookup"><span data-stu-id="51dae-110">type **:** address</span></span> 
    
<span data-ttu-id="51dae-111">Im Gegensatz zu anderen Länge sind Werte, die Anzeige-Namen- und Adresse Länge 16-Bit-Werte ohne Vorzeichen, anstatt lange ganze Zahlen ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="51dae-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="51dae-112">Dazu gehören weiterhin Null-Zeichen jedoch beendet.</span><span class="sxs-lookup"><span data-stu-id="51dae-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="51dae-113">Die Typ und die Adresse Zeichenfolgen in den Eintrag _e-Mail-Adresse_ werden durch einen Doppelpunkt (:)) Literalzeichen wie "smtp:joe@nowhere.com" getrennt.</span><span class="sxs-lookup"><span data-stu-id="51dae-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="51dae-114">Nur die kombinierten Typ **:** Adresszeichenfolge ist Null endende.</span><span class="sxs-lookup"><span data-stu-id="51dae-114">Only the combined type **:** address string is null-terminated.</span></span>
  

