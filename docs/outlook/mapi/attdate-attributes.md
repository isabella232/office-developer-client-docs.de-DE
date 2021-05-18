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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408278"
---
# <a name="attdate-attributes"></a><span data-ttu-id="d77ec-103">attDate-Attribute</span><span class="sxs-lookup"><span data-stu-id="d77ec-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="d77ec-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d77ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d77ec-105">Alle MAPI-Eigenschaften in Bezug auf Datums- und Zeitangaben werden TNEF-Attributen zugeordnet, die das **AttDate-Präfix** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d77ec-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="d77ec-106">Diese werden alle als **DTR-Strukturen** codiert.</span><span class="sxs-lookup"><span data-stu-id="d77ec-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="d77ec-107">Die Datums- und Zeitangaben für Anlagenattribute werden ebenfalls als **DTR-Strukturen** codiert.</span><span class="sxs-lookup"><span data-stu-id="d77ec-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="d77ec-108">Alle MAPI-Eigenschaften in Bezug auf Datums- und Zeitangaben werden TNEF-Attributen zugeordnet, die das **AttDate-Präfix** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d77ec-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="d77ec-109">Diese werden alle als **DTR-Strukturen** codiert.</span><span class="sxs-lookup"><span data-stu-id="d77ec-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="d77ec-110">Die Datums- und Zeitangaben für Anlagenattribute werden ebenfalls als **DTR-Strukturen** codiert.</span><span class="sxs-lookup"><span data-stu-id="d77ec-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="d77ec-111">Eine **DTR-Struktur** ähnelt der **SYSTEMTIME-Struktur,** die in den Win32-Headerdateien definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d77ec-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="d77ec-112">Die **DTR-Struktur** wird im TNEF-Stream als **Sizeof(DTR)-Bytes** codiert, beginnend mit dem ersten Element der Struktur.</span><span class="sxs-lookup"><span data-stu-id="d77ec-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="d77ec-113">Die **DTR-Struktur** ist im TNEF definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="d77ec-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

