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
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318067"
---
# <a name="attdate-attributes"></a><span data-ttu-id="efbcf-103">attDate-Attribute</span><span class="sxs-lookup"><span data-stu-id="efbcf-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="efbcf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efbcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efbcf-105">Alle MAPI-Eigenschaften, die sich auf Datums-und Uhrzeitangaben beziehen, werden TNEF-Attributen zugeordnet, die das **attDate** -Präfix aufweisen.</span><span class="sxs-lookup"><span data-stu-id="efbcf-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="efbcf-106">Diese sind alle als **DTR** -Strukturen codiert.</span><span class="sxs-lookup"><span data-stu-id="efbcf-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="efbcf-107">Die Datums-und Uhrzeitangaben für Anlagenattribute werden ebenfalls als **DTR** -Strukturen codiert.</span><span class="sxs-lookup"><span data-stu-id="efbcf-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="efbcf-108">Alle MAPI-Eigenschaften, die sich auf Datums-und Uhrzeitangaben beziehen, werden TNEF-Attributen zugeordnet, die das **attDate** -Präfix aufweisen.</span><span class="sxs-lookup"><span data-stu-id="efbcf-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="efbcf-109">Diese sind alle als **DTR** -Strukturen codiert.</span><span class="sxs-lookup"><span data-stu-id="efbcf-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="efbcf-110">Die Datums-und Uhrzeitangaben für Anlagenattribute werden ebenfalls als **DTR** -Strukturen codiert.</span><span class="sxs-lookup"><span data-stu-id="efbcf-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="efbcf-111">Eine **DTR** -Struktur ähnelt der in den Win32-Headerdateien definierten **System** Zeitstruktur.</span><span class="sxs-lookup"><span data-stu-id="efbcf-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="efbcf-112">Die **DTR** -Struktur wird im TNEF-Stream als **sizeof (DTR)-** Byte, beginnend mit dem ersten Element der Struktur, codiert.</span><span class="sxs-lookup"><span data-stu-id="efbcf-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="efbcf-113">Die **DTR** -Struktur ist im TNEF definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="efbcf-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

