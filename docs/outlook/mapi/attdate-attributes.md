---
title: attDate-Attribute
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ff0cc6b1c17b2ed83d7b0ec0921904763da8624b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567013"
---
# <a name="attdate-attributes"></a><span data-ttu-id="bb030-103">attDate-Attribute</span><span class="sxs-lookup"><span data-stu-id="bb030-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="bb030-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb030-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb030-105">Alle MAPI-Eigenschaften, die sich auf die Datums- und Zeitangaben beziehen sind TNEF-Attributen zugeordnet, die das Präfix **AttDate** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bb030-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="bb030-106">Diese werden alle als **DTR** Strukturen codiert.</span><span class="sxs-lookup"><span data-stu-id="bb030-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="bb030-107">Die Datums- und Zeitangaben für Anlagenattribute werden als auch Strukturen **DTR** codiert.</span><span class="sxs-lookup"><span data-stu-id="bb030-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="bb030-108">Alle MAPI-Eigenschaften, die sich auf die Datums- und Zeitangaben beziehen sind TNEF-Attributen zugeordnet, die das Präfix **AttDate** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bb030-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="bb030-109">Diese werden alle als **DTR** Strukturen codiert.</span><span class="sxs-lookup"><span data-stu-id="bb030-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="bb030-110">Die Datums- und Zeitangaben für Anlagenattribute werden als auch Strukturen **DTR** codiert.</span><span class="sxs-lookup"><span data-stu-id="bb030-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="bb030-111">Eine Struktur **DTR** ähnelt der **SYSTEMTIME** -Struktur, die in den Win32-Headerdateien definiert.</span><span class="sxs-lookup"><span data-stu-id="bb030-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="bb030-112">Die Struktur **DTR** wird als **sizeof(DTR)** Bytes, beginnend mit dem ersten Element der Struktur in der TNEF-Stream codiert.</span><span class="sxs-lookup"><span data-stu-id="bb030-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="bb030-113">Die **DTR** -Struktur ist in der TNEF definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="bb030-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

