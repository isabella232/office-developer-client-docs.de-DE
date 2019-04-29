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
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410434"
---
# <a name="srow"></a><span data-ttu-id="08bae-103">SRow</span><span class="sxs-lookup"><span data-stu-id="08bae-103">SRow</span></span>

<span data-ttu-id="08bae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08bae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08bae-105">Beschreibt eine Zeile aus einer Tabelle, die ausgewählte Eigenschaften für ein bestimmtes Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="08bae-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08bae-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="08bae-106">Header file:</span></span>  <br/> |<span data-ttu-id="08bae-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="08bae-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="08bae-108">Members</span><span class="sxs-lookup"><span data-stu-id="08bae-108">Members</span></span>

<span data-ttu-id="08bae-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="08bae-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="08bae-110">Padding Bytes, um die Eigenschaftswerte, auf die durch das **lpProps** -Element verwiesen wird, ordnungsgemäß auszurichten.</span><span class="sxs-lookup"><span data-stu-id="08bae-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="08bae-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="08bae-111">**cValues**</span></span>
  
> <span data-ttu-id="08bae-112">Die Anzahl der Eigenschaftswerte, auf die von **lpProps**verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="08bae-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="08bae-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="08bae-113">**lpProps**</span></span>
  
> <span data-ttu-id="08bae-114">Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die die Eigenschaftswerte für die Spalten in der Zeile beschreiben.</span><span class="sxs-lookup"><span data-stu-id="08bae-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="08bae-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08bae-115">Remarks</span></span>

<span data-ttu-id="08bae-116">Eine **SRow** -Struktur beschreibt eine Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="08bae-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="08bae-117">Sie ist in der [TABLE_NOTIFICATION](table_notification.md) -Struktur enthalten, die einer Tabellenbenachrichtigung beigefügt ist.</span><span class="sxs-lookup"><span data-stu-id="08bae-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="08bae-118">**SRow** -Strukturen werden in den folgenden Methoden verwendet:</span><span class="sxs-lookup"><span data-stu-id="08bae-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="08bae-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="08bae-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="08bae-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="08bae-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="08bae-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="08bae-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="08bae-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="08bae-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="08bae-123">[ITableData: IUnknown](itabledataiunknown.md) (viele Methoden)</span><span class="sxs-lookup"><span data-stu-id="08bae-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="08bae-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="08bae-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="08bae-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="08bae-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="08bae-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="08bae-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="08bae-127">Wenn mehr als eine Zeile beschrieben werden muss, wird eine [SRowSet](srowset.md) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="08bae-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="08bae-128">Eine **SRowSet** -Struktur enthält ein Array von **SRow** -Strukturen und die Anzahl der Strukturen im Array.</span><span class="sxs-lookup"><span data-stu-id="08bae-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="08bae-129">Die folgende Abbildung zeigt die Beziehung zwischen einer **SRow** und einer **SRowSet** -Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="08bae-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="08bae-130">**Beziehung zwischen SRow und SRowSet**</span><span class="sxs-lookup"><span data-stu-id="08bae-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="08bae-131">![Beziehung zwischen SRow und SRowSet] (media/amapi_17.gif "Beziehung zwischen SRow und SRowSet")</span><span class="sxs-lookup"><span data-stu-id="08bae-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="08bae-132">**SRow** -Strukturen sind identisch mit den [Miet](adrentry.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="08bae-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="08bae-133">Daher kann eine Zeile einer Empfängertabelle und ein Eintrag in einer Adressliste gleich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="08bae-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="08bae-134">Informationen dazu, wie der Speicher für **SRow** -Strukturen zugeordnet werden sollte, finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="08bae-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08bae-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08bae-135">See also</span></span>

- [<span data-ttu-id="08bae-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="08bae-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="08bae-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="08bae-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="08bae-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="08bae-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="08bae-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="08bae-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="08bae-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="08bae-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="08bae-141">Verwalten von Speicher für ADRLIST-und SRowSet-Strukturen</span><span class="sxs-lookup"><span data-stu-id="08bae-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

