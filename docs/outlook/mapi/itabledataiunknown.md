---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430595"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="a2694-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2694-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="a2694-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2694-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2694-105">Stellt Hilfsmethoden für die Arbeit mit Tabellen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a2694-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="a2694-106">MAPI stellt Tabellendatenobjekte oder -objekte zur Verfügung, die **ITableData** implementieren, um Dienstanbietern bei der Durchführung der Tabellenwartung zu helfen.</span><span class="sxs-lookup"><span data-stu-id="a2694-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="a2694-107">Zum Abrufen eines Tabellendatenobjekts rufen Dienstanbieter die [CreateTable-Funktion](createtable.md) auf.</span><span class="sxs-lookup"><span data-stu-id="a2694-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2694-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a2694-108">Header file:</span></span>  <br/> |<span data-ttu-id="a2694-109">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a2694-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a2694-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="a2694-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="a2694-111">Tabellendatenobjekte</span><span class="sxs-lookup"><span data-stu-id="a2694-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="a2694-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a2694-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="a2694-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="a2694-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="a2694-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a2694-114">Called by:</span></span>  <br/> |<span data-ttu-id="a2694-115">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a2694-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="a2694-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="a2694-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a2694-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="a2694-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="a2694-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="a2694-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="a2694-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="a2694-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a2694-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="a2694-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a2694-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="a2694-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="a2694-122">Erstellt eine Tabellenansicht und gibt einen Zeiger auf eine [IMAPITable-Implementierung](imapitableiunknown.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="a2694-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="a2694-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="a2694-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="a2694-124">Fügt eine neue Tabellenzeile ein und ersetzt möglicherweise eine vorhandene Zeile.</span><span class="sxs-lookup"><span data-stu-id="a2694-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="a2694-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="a2694-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="a2694-126">Löscht eine Tabellenzeile.</span><span class="sxs-lookup"><span data-stu-id="a2694-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="a2694-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="a2694-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="a2694-128">Ruft eine Tabellenzeile ab.</span><span class="sxs-lookup"><span data-stu-id="a2694-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="a2694-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="a2694-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="a2694-130">Ruft eine Zeile basierend auf ihrer Position in der Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="a2694-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="a2694-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="a2694-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="a2694-132">Sendet eine Benachrichtigung für eine Tabellenzeile.</span><span class="sxs-lookup"><span data-stu-id="a2694-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="a2694-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="a2694-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="a2694-134">Fügt eine Tabellenzeile ein.</span><span class="sxs-lookup"><span data-stu-id="a2694-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="a2694-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="a2694-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="a2694-136">Fügt mehrere Tabellenzeilen ein und ersetzt möglicherweise vorhandene Zeilen.</span><span class="sxs-lookup"><span data-stu-id="a2694-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="a2694-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="a2694-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="a2694-138">Löscht mehrere Tabellenzeilen.</span><span class="sxs-lookup"><span data-stu-id="a2694-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2694-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a2694-139">Remarks</span></span>

<span data-ttu-id="a2694-140">Die MAPI-Implementierung von **ITableData** funktioniert mit Tabellen, indem alle Daten und alle zugehörigen Einschränkungen im Arbeitsspeicher gespeichert werden, wodurch sie für die Verwendung mit sehr großen Tabellen ungeeignet ist.</span><span class="sxs-lookup"><span data-stu-id="a2694-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="a2694-141">Große Einschränkungen und komplexe Vorgänge wie kategorisierung werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a2694-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="a2694-142">Tabellendatenobjekte identifizieren Zeilen mithilfe einer Indexspalte, einer Eigenschaft, die garantiert einen eindeutigen Wert für jede Zeile hat.</span><span class="sxs-lookup"><span data-stu-id="a2694-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="a2694-143">Die meisten Dienstanbieter **verwenden die PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaft als Indexspalte.</span><span class="sxs-lookup"><span data-stu-id="a2694-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="a2694-144">Eigenschaften mit mehreren Werten können nicht als Indexspalte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2694-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="a2694-145">Tabellendatenobjekte generieren unabhängig von der Anzahl der Zeilen, die von einer Änderung oder Löschung betroffen sind, eine einzelne Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a2694-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="a2694-146">Wenn eine Zielzeile in einem Vorgang nicht vorhanden ist, wird eine Zeile hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2694-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2694-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2694-147">See also</span></span>



[<span data-ttu-id="a2694-148">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a2694-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

