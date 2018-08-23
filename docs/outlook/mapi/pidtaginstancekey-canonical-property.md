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
ms.openlocfilehash: 53772fca5e8137dfd602d4c7d6f5e6ad40f9c50f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573432"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="a721a-103">PidTagInstanceKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a721a-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="a721a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a721a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a721a-105">Enthält einen Wert, der eine Zeile in einer Tabelle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a721a-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a721a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a721a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a721a-107">PR_INSTANCE_KEY</span><span class="sxs-lookup"><span data-stu-id="a721a-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="a721a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a721a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a721a-109">0x0FF6</span><span class="sxs-lookup"><span data-stu-id="a721a-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="a721a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a721a-110">Data type:</span></span>  <br/> |<span data-ttu-id="a721a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a721a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a721a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a721a-112">Area:</span></span>  <br/> |<span data-ttu-id="a721a-113">Tabelle</span><span class="sxs-lookup"><span data-stu-id="a721a-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a721a-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a721a-114">Remarks</span></span>

<span data-ttu-id="a721a-115">Diese Eigenschaft ist ein binärer Wert, der eine Zeile in einer Tabellenansicht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a721a-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="a721a-116">Es ist eine erforderliche Spalte in den meisten Tabellen.</span><span class="sxs-lookup"><span data-stu-id="a721a-116">It is a required column in most tables.</span></span> <span data-ttu-id="a721a-117">Wenn eine Zeile in zwei Ansichten enthalten ist, sind zwei andere Instanzenschlüssel.</span><span class="sxs-lookup"><span data-stu-id="a721a-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="a721a-118">Der Instanzschlüssel einer Zeile abweichen jedes Mal, wenn die Tabelle geöffnet ist, aber konstant bleiben, während die Tabelle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="a721a-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="a721a-119">Zeilen hinzugefügt, während eine Tabelle verwendet wird wieder einen Instanzschlüssel nicht verwenden, der zuvor verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a721a-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="a721a-120">Verwenden Sie die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) Eigenschaften alle Zeilen der eine Erweiterung korrelieren.</span><span class="sxs-lookup"><span data-stu-id="a721a-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="a721a-121">Verwenden Sie **PR_INSTANCE_KEY** , um eine bestimmte Instanz innerhalb der Erweiterung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a721a-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="a721a-122">Wenn eine mehrwertige Eigenschaft in einer Tabelle erweitert wird, wird eine Zeile für jeden Wert dieser Eigenschaft d. h., für jede Instanz der Erweiterung, erstellt.</span><span class="sxs-lookup"><span data-stu-id="a721a-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="a721a-123">Jede Zeile enthält einen eindeutigen Wert für die Eigenschaft **PR_INSTANCE_KEY** , während die anderen Spalten die ursprünglichen Werte in der gesamten die Erweiterung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a721a-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="a721a-124">Zeilen nicht entsprechend der tatsächlichen Daten können in einer kategorisierten Sortierung einer Tabelle das Ergebnis der Sortierung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a721a-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="a721a-125">Jede Zeile eine solche wie alle Zeilen in allen Tabellen, verfügt über eine eigene eindeutige Instanz-Taste.</span><span class="sxs-lookup"><span data-stu-id="a721a-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="a721a-126">**PR_INSTANCE_KEY** ist auch in der Tabelle ereignisbenachrichtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a721a-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="a721a-127">Die **PropIndex** und **PropPrior** Member der Struktur [TABLE_NOTIFICATION](table_notification.md) sind [SPropValue](spropvalue.md) Strukturen **PR_INSTANCE_KEY** enthalten.</span><span class="sxs-lookup"><span data-stu-id="a721a-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="a721a-128">Das Element **PropIndex** gibt die Zeile, die hinzugefügt oder geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a721a-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="a721a-129">Das Element **PropPrior** gibt die Zeile vor der hinzugefügte oder geänderte Zeile (**PR_NULL** gibt eine Änderung an der ersten Zeile).</span><span class="sxs-lookup"><span data-stu-id="a721a-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="a721a-130">Dieser Wert wird nicht als Teil der Anzeige-Tabelle kopiert.</span><span class="sxs-lookup"><span data-stu-id="a721a-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="a721a-131">**PR_INSTANCE_KEY** ist eine [MAPIUID](mapiuid.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a721a-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="a721a-132">Alle Instanzenschlüssel können direkt als Binärwerte verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="a721a-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a721a-133">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a721a-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a721a-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a721a-134">Protocol specifications</span></span>

<span data-ttu-id="a721a-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a721a-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a721a-136">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a721a-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a721a-137">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a721a-137">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a721a-138">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a721a-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a721a-139">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a721a-139">Header files</span></span>

<span data-ttu-id="a721a-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a721a-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="a721a-141">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a721a-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="a721a-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a721a-142">Mapitags.h</span></span>
  
> <span data-ttu-id="a721a-143">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a721a-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a721a-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a721a-144">See also</span></span>



[<span data-ttu-id="a721a-145">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a721a-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a721a-146">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a721a-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a721a-147">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a721a-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a721a-148">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a721a-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

