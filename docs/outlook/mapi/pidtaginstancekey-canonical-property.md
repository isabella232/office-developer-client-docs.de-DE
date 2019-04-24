---
title: Kanonische Pidtaginstancekey (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358511"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="5de7f-103">Kanonische Pidtaginstancekey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5de7f-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="5de7f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5de7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5de7f-105">Enthält einen Wert, der eine Zeile in einer Tabelle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5de7f-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5de7f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5de7f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5de7f-107">PR_INSTANCE_KEY</span><span class="sxs-lookup"><span data-stu-id="5de7f-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="5de7f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5de7f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5de7f-109">0x0FF6</span><span class="sxs-lookup"><span data-stu-id="5de7f-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="5de7f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5de7f-110">Data type:</span></span>  <br/> |<span data-ttu-id="5de7f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5de7f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5de7f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5de7f-112">Area:</span></span>  <br/> |<span data-ttu-id="5de7f-113">Tabelle</span><span class="sxs-lookup"><span data-stu-id="5de7f-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5de7f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5de7f-114">Remarks</span></span>

<span data-ttu-id="5de7f-115">Diese Eigenschaft ist ein Binärwert, der eine Zeile in einer Tabellenansicht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5de7f-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="5de7f-116">In den meisten Tabellen ist es eine erforderliche Spalte.</span><span class="sxs-lookup"><span data-stu-id="5de7f-116">It is a required column in most tables.</span></span> <span data-ttu-id="5de7f-117">Wenn eine Zeile in zwei Ansichten enthalten ist, gibt es zwei verschiedene Instanzenschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5de7f-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="5de7f-118">Der Instanzschlüssel einer Zeile kann sich bei jedem Öffnen der Tabelle unterscheiden, bleibt jedoch konstant, während die Tabelle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="5de7f-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="5de7f-119">Zeilen, die hinzugefügt werden, während eine Tabelle verwendet wird, verwenden Sie keinen zuvor verwendeten Instanzschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5de7f-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="5de7f-120">Verwenden Sie die Eigenschaften **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_RECORD_KEY** ([pidtagrecordkey (](pidtagrecordkey-canonical-property.md)), um alle Zeilen einer Erweiterung zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="5de7f-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="5de7f-121">Verwenden Sie **PR_INSTANCE_KEY** , um eine bestimmte Instanz innerhalb der Erweiterung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="5de7f-122">Wenn eine mehrwertige Eigenschaft in einer Tabelle erweitert wird, wird für jede Erweiterungs Instanz, also für jeden Wert dieser Eigenschaft, eine Zeile erstellt.</span><span class="sxs-lookup"><span data-stu-id="5de7f-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="5de7f-123">Jede Zeile hat einen eindeutigen Wert für die **PR_INSTANCE_KEY** -Eigenschaft, während alle anderen Spalten ihre ursprünglichen Werte während der Erweiterung behalten.</span><span class="sxs-lookup"><span data-stu-id="5de7f-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="5de7f-124">In einer kategorisierten Sortierung einer Tabelle können Zeilen, die nicht den tatsächlichen Daten entsprechen, dem Ergebnis der Sortierung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5de7f-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="5de7f-125">Jede solche Zeile hat, wie alle Zeilen in allen Tabellen, ihren eigenen eindeutigen Instanzschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5de7f-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="5de7f-126">**PR_INSTANCE_KEY** wird auch in Tabellenereignis Benachrichtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5de7f-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="5de7f-127">Die **propIndex** -und **propPrior** -Elemente der [TABLE_NOTIFICATION](table_notification.md) -Struktur sind [SPropValue](spropvalue.md) -Strukturen mit **PR_INSTANCE_KEY** -Werten.</span><span class="sxs-lookup"><span data-stu-id="5de7f-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="5de7f-128">Das **propIndex** -Element gibt die Zeile an, die hinzugefügt oder geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5de7f-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="5de7f-129">Das **propPrior** -Element gibt die Zeile vor der hinzugefügten oder geänderten Zeile an (**PR_NULL** gibt eine Änderung der ersten Zeile an).</span><span class="sxs-lookup"><span data-stu-id="5de7f-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="5de7f-130">Dieser Wert wird nicht als Teil der Anzeigetabelle kopiert.</span><span class="sxs-lookup"><span data-stu-id="5de7f-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="5de7f-131">**PR_INSTANCE_KEY** ist eine [MAPIUID](mapiuid.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5de7f-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="5de7f-132">Alle Instanzenschlüssel können direkt als Binärwerte verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="5de7f-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5de7f-133">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5de7f-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5de7f-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5de7f-134">Protocol specifications</span></span>

<span data-ttu-id="5de7f-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5de7f-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5de7f-136">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5de7f-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5de7f-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5de7f-138">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="5de7f-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5de7f-139">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5de7f-139">Header files</span></span>

<span data-ttu-id="5de7f-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5de7f-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="5de7f-141">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5de7f-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="5de7f-142">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5de7f-142">Mapitags.h</span></span>
  
> <span data-ttu-id="5de7f-143">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5de7f-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5de7f-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5de7f-144">See also</span></span>



[<span data-ttu-id="5de7f-145">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5de7f-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5de7f-146">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5de7f-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5de7f-147">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5de7f-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5de7f-148">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5de7f-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

