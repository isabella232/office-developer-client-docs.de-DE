---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8b4e090b3dd6bf8ecd2517dee57093106147e22d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795627"
---
# <a name="srow"></a><span data-ttu-id="7ea5b-103">SRow</span><span class="sxs-lookup"><span data-stu-id="7ea5b-103">SRow</span></span>

<span data-ttu-id="7ea5b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ea5b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ea5b-105">Beschreibt eine Zeile aus einer Tabelle, die ausgewählte Eigenschaften für ein bestimmtes Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ea5b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7ea5b-106">Header file:</span></span>  <br/> |<span data-ttu-id="7ea5b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ea5b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="7ea5b-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="7ea5b-108">Members</span></span>

<span data-ttu-id="7ea5b-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="7ea5b-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="7ea5b-110">Abstand Bytes, um die Eigenschaftswerte ordnungsgemäß ausrichten auf das durch die **LpProps** Mitglied.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="7ea5b-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7ea5b-111">**cValues**</span></span>
  
> <span data-ttu-id="7ea5b-112">Anzahl der Eigenschaftswerte, die auf die **LpProps**zeigt.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="7ea5b-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="7ea5b-113">**lpProps**</span></span>
  
> <span data-ttu-id="7ea5b-114">Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die die Eigenschaftswerte für die Spalten in der Zeile zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7ea5b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ea5b-115">Remarks</span></span>

<span data-ttu-id="7ea5b-116">Eine Struktur **SRow** beschreibt eine Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="7ea5b-117">Es ist in der Struktur [TABLE_NOTIFICATION](table_notification.md) enthalten, die eine Benachrichtigung über eine Tabelle begleitet.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="7ea5b-118">**SRow** Strukturen werden in den folgenden Methoden verwendet:</span><span class="sxs-lookup"><span data-stu-id="7ea5b-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="7ea5b-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="7ea5b-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="7ea5b-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="7ea5b-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="7ea5b-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="7ea5b-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="7ea5b-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="7ea5b-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="7ea5b-123">[ITableData: IUnknown](itabledataiunknown.md) (viele Methoden)</span><span class="sxs-lookup"><span data-stu-id="7ea5b-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="7ea5b-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="7ea5b-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="7ea5b-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="7ea5b-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="7ea5b-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="7ea5b-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="7ea5b-127">Wenn mehr als eine Zeile werden beschrieben muss, wird eine [SRowSet](srowset.md) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="7ea5b-128">Eine **SRowSet** -Struktur enthält ein Array von **SRow** Strukturen und Anzahl der Strukturen im Array.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="7ea5b-129">Die folgende Abbildung zeigt die Beziehung zwischen einem **SRow** und eine **SRowSet** -Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="7ea5b-130">**Beziehung zwischen SRow und SRowSet**</span><span class="sxs-lookup"><span data-stu-id="7ea5b-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="7ea5b-131">![Beziehung zwischen SRow und SRowSet] (media/amapi_17.gif "Beziehung zwischen SRow und SRowSet")</span><span class="sxs-lookup"><span data-stu-id="7ea5b-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="7ea5b-132">**SRow** Strukturen definiert sind identisch mit [ADRENTRY](adrentry.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="7ea5b-133">Aus diesem Grund kann eine Zeile mit einem Empfänger Tabelle und einen Eintrag in einer Adressliste die gleiche Weise behandelt.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="7ea5b-134">Informationen dazu, wie der Speicher für **SRow** Strukturen zugewiesen werden sollten finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="7ea5b-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ea5b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ea5b-135">See also</span></span>

- [<span data-ttu-id="7ea5b-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="7ea5b-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="7ea5b-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7ea5b-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="7ea5b-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="7ea5b-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="7ea5b-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7ea5b-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="7ea5b-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7ea5b-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="7ea5b-141">Verwalten von Speicher für ADRLIST- und SRowSet-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7ea5b-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

