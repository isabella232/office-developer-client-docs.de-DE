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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326292"
---
# <a name="mviprop"></a><span data-ttu-id="4e114-103">MVI_PROP</span><span class="sxs-lookup"><span data-stu-id="4e114-103">MVI_PROP</span></span>

  
  
<span data-ttu-id="4e114-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e114-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e114-105">Legt die MVI_FLAG für eine angegebene Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="4e114-105">Sets the MVI_FLAG for a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e114-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4e114-106">Header file:</span></span>  <br/> |<span data-ttu-id="4e114-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4e114-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4e114-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="4e114-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="4e114-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4e114-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a><span data-ttu-id="4e114-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e114-110">Parameters</span></span>

 <span data-ttu-id="4e114-111">_Tag_</span><span class="sxs-lookup"><span data-stu-id="4e114-111">_tag_</span></span>
  
> <span data-ttu-id="4e114-112">Das zu ändernde Property-Tag.</span><span class="sxs-lookup"><span data-stu-id="4e114-112">The property tag to be modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e114-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e114-113">Remarks</span></span>

<span data-ttu-id="4e114-114">Das MVI_FLAG kombiniert die Einstellung von MV_FLAG, identifiziert eine Eigenschaft als mehrwertige und MV_INSTANCE und fordert, dass eine mehrwertige Eigenschaft in einer Tabelle in mehreren Zeilen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4e114-114">The MVI_FLAG combines the setting of MV_FLAG, identifying a property as multi-valued, and MV_INSTANCE, requesting that a multi-valued property be displayed in a table in multiple rows.</span></span> <span data-ttu-id="4e114-115">Der Eigenschaftentyp der betroffenen Eigenschaft wird geändert, aber der Bezeichner bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="4e114-115">The property type of the affected property is modified, but the identifier remains unchanged.</span></span> 
  
<span data-ttu-id="4e114-116">Wenn beispielsweise das MVI_PROP-Makro auf eine Eigenschaft vom Typ PT_FLOAT angewendet wird, wird der Typ in PT_MV_FLOAT geändert.</span><span class="sxs-lookup"><span data-stu-id="4e114-116">For example, when the MVI_PROP macro is applied to a property of type PT_FLOAT, its type is changed to PT_MV_FLOAT.</span></span> <span data-ttu-id="4e114-117">Wenn Sie in einer Tabelle enthalten sind, werden mehrere Zeilen verwendet, um die Eigenschaft darzustellen, die eine Zeile für jeden Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="4e114-117">When included in a table, multiple rows are used to represent the property that has one row for each value.</span></span> <span data-ttu-id="4e114-118">Die Eigenschaften für die anderen Spalten werden wiederholt.</span><span class="sxs-lookup"><span data-stu-id="4e114-118">The properties for the other columns are repeated.</span></span> 
  
<span data-ttu-id="4e114-119">Weitere Informationen zu diesen Flags finden Sie unter [MAPI property Type Overview](mapi-property-type-overview.md) und [Working with mehrwertig Columns](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="4e114-119">For more information about these flags, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e114-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e114-120">See also</span></span>



[<span data-ttu-id="4e114-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4e114-121">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="4e114-122">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="4e114-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

