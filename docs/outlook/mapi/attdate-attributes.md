---
title: AttDate-Attribute
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f3319c9ae49fa97a6179b0ee800bd5dd594aefab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791333"
---
# <a name="attdate-attributes"></a><span data-ttu-id="167c9-103">AttDate-Attribute</span><span class="sxs-lookup"><span data-stu-id="167c9-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="167c9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="167c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="167c9-105">Alle MAPI-Eigenschaften, die sich auf die Datums- und Zeitangaben beziehen sind TNEF-Attributen zugeordnet, die das Präfix **AttDate** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="167c9-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="167c9-106">Diese werden alle als **DTR** Strukturen codiert.</span><span class="sxs-lookup"><span data-stu-id="167c9-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="167c9-107">Die Datums- und Zeitangaben für Anlagenattribute werden als auch Strukturen **DTR** codiert.</span><span class="sxs-lookup"><span data-stu-id="167c9-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="167c9-108">Alle MAPI-Eigenschaften, die sich auf die Datums- und Zeitangaben beziehen sind TNEF-Attributen zugeordnet, die das Präfix **AttDate** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="167c9-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="167c9-109">Diese werden alle als **DTR** Strukturen codiert.</span><span class="sxs-lookup"><span data-stu-id="167c9-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="167c9-110">Die Datums- und Zeitangaben für Anlagenattribute werden als auch Strukturen **DTR** codiert.</span><span class="sxs-lookup"><span data-stu-id="167c9-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="167c9-111">Eine Struktur **DTR** ähnelt der **SYSTEMTIME** -Struktur, die in den Win32-Headerdateien definiert.</span><span class="sxs-lookup"><span data-stu-id="167c9-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="167c9-112">Die Struktur **DTR** wird als **sizeof(DTR)** Bytes, beginnend mit dem ersten Element der Struktur in der TNEF-Stream codiert.</span><span class="sxs-lookup"><span data-stu-id="167c9-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="167c9-113">Die **DTR** -Struktur ist in der TNEF definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="167c9-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

