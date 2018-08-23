---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6a3d0d79d190b318d36fd9be8a3ec39d6aa7ad29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593977"
---
# <a name="mviprop"></a><span data-ttu-id="28a75-103">MVI_PROP</span><span class="sxs-lookup"><span data-stu-id="28a75-103">MVI_PROP</span></span>

  
  
<span data-ttu-id="28a75-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28a75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28a75-105">Legt die MVI_FLAG für eine angegebene Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="28a75-105">Sets the MVI_FLAG for a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28a75-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="28a75-106">Header file:</span></span>  <br/> |<span data-ttu-id="28a75-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28a75-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="28a75-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="28a75-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="28a75-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="28a75-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a><span data-ttu-id="28a75-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="28a75-110">Parameters</span></span>

 <span data-ttu-id="28a75-111">_Tag_</span><span class="sxs-lookup"><span data-stu-id="28a75-111">_tag_</span></span>
  
> <span data-ttu-id="28a75-112">Die Eigenschaftentag geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="28a75-112">The property tag to be modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="28a75-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="28a75-113">Remarks</span></span>

<span data-ttu-id="28a75-114">Die MVI_FLAG kombiniert die Einstellung der MV_FLAG, Identifizieren einer Eigenschaft als mehrwertige, und MV_INSTANCE vorhanden, anfordern, dass eine mehrwertige Eigenschaft in einer Tabelle in mehrere Zeilen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="28a75-114">The MVI_FLAG combines the setting of MV_FLAG, identifying a property as multi-valued, and MV_INSTANCE, requesting that a multi-valued property be displayed in a table in multiple rows.</span></span> <span data-ttu-id="28a75-115">Der Eigenschaftentyp der betroffenen-Eigenschaft wird so geändert, aber der Bezeichner bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="28a75-115">The property type of the affected property is modified, but the identifier remains unchanged.</span></span> 
  
<span data-ttu-id="28a75-116">Wenn das Makro MVI_PROP auf eine Eigenschaft vom Typ PT_FLOAT angewendet wird, wird dieses Typs PT_MV_FLOAT geändert.</span><span class="sxs-lookup"><span data-stu-id="28a75-116">For example, when the MVI_PROP macro is applied to a property of type PT_FLOAT, its type is changed to PT_MV_FLOAT.</span></span> <span data-ttu-id="28a75-117">Wenn in einer Tabelle enthalten, werden mehrere Zeilen verwendet, um die Eigenschaft darstellen, die eine Zeile für jeden Wert hat.</span><span class="sxs-lookup"><span data-stu-id="28a75-117">When included in a table, multiple rows are used to represent the property that has one row for each value.</span></span> <span data-ttu-id="28a75-118">Die Eigenschaften für die anderen Spalten werden wiederholt.</span><span class="sxs-lookup"><span data-stu-id="28a75-118">The properties for the other columns are repeated.</span></span> 
  
<span data-ttu-id="28a75-119">Weitere Informationen zu diesen Flags finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md) und [Arbeiten mit Spalten mit mehreren Werten](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="28a75-119">For more information about these flags, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="28a75-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28a75-120">See also</span></span>



[<span data-ttu-id="28a75-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="28a75-121">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="28a75-122">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="28a75-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

