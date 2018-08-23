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
ms.openlocfilehash: 865d929f3348710b7786f4182670f3304a3a9244
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578038"
---
# <a name="attowner"></a><span data-ttu-id="54d70-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="54d70-103">attOwner</span></span>

  
  
<span data-ttu-id="54d70-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54d70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54d70-105">Gezählte Zeichenfolgen End-to-End-festgelegten, wird das Attribut **AttOwner** codiert.</span><span class="sxs-lookup"><span data-stu-id="54d70-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="54d70-106">Das Format für **AttOwner** lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="54d70-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="54d70-107">**AttOwner**:</span><span class="sxs-lookup"><span data-stu-id="54d70-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="54d70-108">Display Name Länge Anzeigename Adresse Länge- _e-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="54d70-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="54d70-109">_e-Mail-Adresse_</span><span class="sxs-lookup"><span data-stu-id="54d70-109">_email-address_</span></span>
  
> <span data-ttu-id="54d70-110">Adresse vom Typ **:**</span><span class="sxs-lookup"><span data-stu-id="54d70-110">type **:** address</span></span> 
    
<span data-ttu-id="54d70-111">Im Gegensatz zu anderen Länge sind Werte, die Anzeige-Namen- und Adresse Länge 16-Bit-Werte ohne Vorzeichen, anstatt lange ganze Zahlen ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="54d70-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="54d70-112">Dazu gehören weiterhin Null-Zeichen jedoch beendet.</span><span class="sxs-lookup"><span data-stu-id="54d70-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="54d70-113">Die Typ und die Adresse Zeichenfolgen in den Eintrag _e-Mail-Adresse_ werden durch einen Doppelpunkt (:)) Literalzeichen wie "smtp:joe@nowhere.com" getrennt.</span><span class="sxs-lookup"><span data-stu-id="54d70-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="54d70-114">Nur die kombinierten Typ **:** Adresszeichenfolge ist Null endende.</span><span class="sxs-lookup"><span data-stu-id="54d70-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="54d70-115">Die Zuordnung der MAPI-Eigenschaften in das Attribut **AttOwner** ist abhängig von der Nachrichtenklasse der Nachricht codiert.</span><span class="sxs-lookup"><span data-stu-id="54d70-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

