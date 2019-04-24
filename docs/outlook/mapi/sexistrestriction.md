---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339277"
---
# <a name="sexistrestriction"></a><span data-ttu-id="92c60-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="92c60-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="92c60-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92c60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92c60-105">Beschreibt eine exist-Einschränkung, die verwendet wird, um zu testen, ob eine bestimmte Eigenschaft als Spalte in der Tabelle vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="92c60-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92c60-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="92c60-106">Header file:</span></span>  <br/> |<span data-ttu-id="92c60-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="92c60-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="92c60-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="92c60-108">Members</span></span>

 <span data-ttu-id="92c60-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="92c60-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="92c60-110">Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="92c60-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="92c60-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="92c60-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="92c60-112">Property-Tag, der die zu testende Spalte identifiziert, die in jeder Zeile vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="92c60-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="92c60-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="92c60-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="92c60-114">Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="92c60-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="92c60-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92c60-115">Remarks</span></span>

<span data-ttu-id="92c60-116">Die exist-Einschränkung wird verwendet, um aussagekräftige Ergebnisse für andere Arten von Einschränkungen zu gewährleisten, die Eigenschaften wie Eigenschafts-und Inhaltseinschränkungen einschließen.</span><span class="sxs-lookup"><span data-stu-id="92c60-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="92c60-117">Wenn eine Einschränkung, die eine Eigenschaft umfasst, an [IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable:: FindRow](imapitable-findrow.md) übergeben wird und die Eigenschaft nicht vorhanden ist, sind die Ergebnisse der Einschränkung nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="92c60-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="92c60-118">Durch das Erstellen einer **and** -Einschränkung, die die Eigenschaftseinschränkung mit einer exist-Einschränkung verknüpft, kann ein Aufrufer exakte Ergebnisse garantieren.</span><span class="sxs-lookup"><span data-stu-id="92c60-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="92c60-119">Exist-Einschränkungen können nicht mit Unterobjekt Eigenschaften verwendet werden, die den Typ PT_OBJECT haben.</span><span class="sxs-lookup"><span data-stu-id="92c60-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="92c60-120">Weitere Informationen zur **SExistRestriction** -Struktur finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="92c60-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92c60-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92c60-121">See also</span></span>



[<span data-ttu-id="92c60-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="92c60-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="92c60-123">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="92c60-123">MAPI Structures</span></span>](mapi-structures.md)

