---
title: PidTagInstanceKey (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358511"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="dcd51-103">PidTagInstanceKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dcd51-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="dcd51-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcd51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcd51-105">Enthält einen Wert, der eine Zeile in einer Tabelle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dcd51-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcd51-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dcd51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dcd51-107">PR_INSTANCE_KEY</span><span class="sxs-lookup"><span data-stu-id="dcd51-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="dcd51-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="dcd51-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dcd51-109">0x0FF6</span><span class="sxs-lookup"><span data-stu-id="dcd51-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="dcd51-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dcd51-110">Data type:</span></span>  <br/> |<span data-ttu-id="dcd51-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dcd51-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dcd51-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dcd51-112">Area:</span></span>  <br/> |<span data-ttu-id="dcd51-113">Tabelle</span><span class="sxs-lookup"><span data-stu-id="dcd51-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcd51-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dcd51-114">Remarks</span></span>

<span data-ttu-id="dcd51-115">Diese Eigenschaft ist ein binärer Wert, der eine Zeile in einer Tabellenansicht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dcd51-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="dcd51-116">Es handelt sich um eine erforderliche Spalte in den meisten Tabellen.</span><span class="sxs-lookup"><span data-stu-id="dcd51-116">It is a required column in most tables.</span></span> <span data-ttu-id="dcd51-117">Wenn eine Zeile in zwei Ansichten enthalten ist, gibt es zwei verschiedene Instanzschlüssel.</span><span class="sxs-lookup"><span data-stu-id="dcd51-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="dcd51-118">Der Instanzschlüssel einer Zeile kann sich jedes Mal unterscheiden, wenn die Tabelle geöffnet wird, bleibt jedoch konstant, während die Tabelle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="dcd51-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="dcd51-119">Zeilen, die hinzugefügt werden, während eine Tabelle verwendet wird, verwenden keinen Instanzschlüssel, der zuvor verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="dcd51-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="dcd51-120">Verwenden Sie **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) Eigenschaften, um alle Zeilen einer Erweiterung zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="dcd51-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="dcd51-121">Verwenden **PR_INSTANCE_KEY,** um eine bestimmte Instanz innerhalb der Erweiterung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="dcd51-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="dcd51-122">Wenn eine mehrwertige Eigenschaft in einer Tabelle erweitert wird, wird für jede Instanz der Erweiterung, d. h. für jeden Wert dieser Eigenschaft, eine Zeile erstellt.</span><span class="sxs-lookup"><span data-stu-id="dcd51-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="dcd51-123">Jede Zeile hat einen eindeutigen Wert für **die PR_INSTANCE_KEY-Eigenschaft,** während alle anderen Spalten während der gesamten Erweiterung ihre ursprünglichen Werte beibehalten.</span><span class="sxs-lookup"><span data-stu-id="dcd51-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="dcd51-124">In einer kategorisierten Art einer Tabelle können dem Ergebnis der Sortierung Zeilen hinzugefügt werden, die nicht den tatsächlichen Daten entspricht.</span><span class="sxs-lookup"><span data-stu-id="dcd51-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="dcd51-125">Jede solche Zeile verfügt wie alle Zeilen in allen Tabellen über einen eigenen eindeutigen Instanzschlüssel.</span><span class="sxs-lookup"><span data-stu-id="dcd51-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="dcd51-126">**PR_INSTANCE_KEY** wird auch in Tabellenereignisbenachrichtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="dcd51-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="dcd51-127">Die **propIndex-** **und propPrior-Elemente** der TABLE_NOTIFICATION sind [SPropValue-Strukturen,](spropvalue.md) die **PR_INSTANCE_KEY** enthalten. [](table_notification.md)</span><span class="sxs-lookup"><span data-stu-id="dcd51-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="dcd51-128">Das **propIndex-Element** gibt die Zeile an, die hinzugefügt oder geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="dcd51-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="dcd51-129">Das **propPrior-Element** gibt die Zeile vor der hinzugefügten oder geänderten Zeile an (**PR_NULL** gibt eine Änderung an der ersten Zeile an).</span><span class="sxs-lookup"><span data-stu-id="dcd51-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="dcd51-130">Dieser Wert wird nicht als Teil der Anzeigetabelle kopiert.</span><span class="sxs-lookup"><span data-stu-id="dcd51-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="dcd51-131">**PR_INSTANCE_KEY** ist eine [MAPIUID-Struktur.](mapiuid.md)</span><span class="sxs-lookup"><span data-stu-id="dcd51-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="dcd51-132">Alle Instanzschlüssel können direkt als Binärwerte verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="dcd51-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dcd51-133">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dcd51-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dcd51-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dcd51-134">Protocol specifications</span></span>

<span data-ttu-id="dcd51-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcd51-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcd51-136">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="dcd51-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dcd51-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcd51-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcd51-138">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="dcd51-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dcd51-139">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="dcd51-139">Header files</span></span>

<span data-ttu-id="dcd51-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dcd51-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="dcd51-141">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="dcd51-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="dcd51-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dcd51-142">Mapitags.h</span></span>
  
> <span data-ttu-id="dcd51-143">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="dcd51-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dcd51-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcd51-144">See also</span></span>



[<span data-ttu-id="dcd51-145">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dcd51-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dcd51-146">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="dcd51-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dcd51-147">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dcd51-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dcd51-148">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dcd51-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

