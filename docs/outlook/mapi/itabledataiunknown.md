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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 968768fe75286b93bf12e349a4845fdfaa1923e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792855"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="66f29-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66f29-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="66f29-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="66f29-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="66f29-105">Bietet Methoden zum Arbeiten mit Tabellen.</span><span class="sxs-lookup"><span data-stu-id="66f29-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="66f29-106">MAPI bietet Datenobjekte Tabelle oder Objekte, die **ITableData** , mit denen Dienstanbieter Tabelle Wartungen implementieren.</span><span class="sxs-lookup"><span data-stu-id="66f29-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="66f29-107">Um ein Table-Datenobjekt zu erhalten, rufen Sie Dienstanbieter [CreateTable](createtable.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="66f29-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66f29-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="66f29-108">Header file:</span></span>  <br/> |<span data-ttu-id="66f29-109">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="66f29-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="66f29-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="66f29-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="66f29-111">Tabelle Datenobjekte</span><span class="sxs-lookup"><span data-stu-id="66f29-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="66f29-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="66f29-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="66f29-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="66f29-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="66f29-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="66f29-114">Called by:</span></span>  <br/> |<span data-ttu-id="66f29-115">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="66f29-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="66f29-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="66f29-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="66f29-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="66f29-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="66f29-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="66f29-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="66f29-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="66f29-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="66f29-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="66f29-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="66f29-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="66f29-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="66f29-122">Erstellt eine Tabellenansicht, einen Zeiger auf eine Implementierung [IMAPITable](imapitableiunknown.md) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="66f29-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="66f29-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="66f29-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="66f29-124">Fügt eine neue Tabellenzeile, die möglicherweise eine vorhandene Zeile ersetzen.</span><span class="sxs-lookup"><span data-stu-id="66f29-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="66f29-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="66f29-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="66f29-126">Löscht eine Tabellenzeile.</span><span class="sxs-lookup"><span data-stu-id="66f29-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="66f29-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="66f29-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="66f29-128">Ruft eine Tabellenzeile.</span><span class="sxs-lookup"><span data-stu-id="66f29-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="66f29-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="66f29-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="66f29-130">Ruft eine Zeile basierend auf seine Position in der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="66f29-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="66f29-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="66f29-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="66f29-132">Sendet eine Benachrichtigung für eine Tabellenzeile.</span><span class="sxs-lookup"><span data-stu-id="66f29-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="66f29-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="66f29-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="66f29-134">Eine Tabellenzeile eingefügt.</span><span class="sxs-lookup"><span data-stu-id="66f29-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="66f29-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="66f29-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="66f29-136">Mehrere Tabellenzeilen, möglicherweise Ersetzen der vorhandene Zeilen eingefügt.</span><span class="sxs-lookup"><span data-stu-id="66f29-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="66f29-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="66f29-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="66f29-138">Löscht mehrere Tabellenzeilen.</span><span class="sxs-lookup"><span data-stu-id="66f29-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66f29-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66f29-139">Remarks</span></span>

<span data-ttu-id="66f29-140">Die MAPI-Implementierung der **ITableData** arbeitet mit Tabellen halten Sie alle Daten und zugehörigen Einschränkungen im Arbeitsspeicher, leicht für die Verwendung mit sehr große Tabellen nicht geeignet.</span><span class="sxs-lookup"><span data-stu-id="66f29-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="66f29-141">Große Einschränkungen und komplexe Vorgänge wie Kategorisierung werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="66f29-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="66f29-142">Datenobjekte Tabelle identifizieren Zeilen mithilfe von einer Indexspalte, eine Eigenschaft, die in jedem Fall ist einen eindeutigen Wert für jede Zeile.</span><span class="sxs-lookup"><span data-stu-id="66f29-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="66f29-143">Die meisten Dienstanbieter verwenden Sie die Eigenschaft **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) als Index-Spalte.</span><span class="sxs-lookup"><span data-stu-id="66f29-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="66f29-144">Eigenschaften, die mehrere Werte aufweisen können nicht als eine Indexspalte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66f29-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="66f29-145">Tabelle Datenobjekte generieren eine einzelne Benachrichtigung unabhängig von der Anzahl der Zeilen, die von einer Änderung oder Löschung betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="66f29-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="66f29-146">Wenn eine Zielzeile in einem Vorgang nicht vorhanden ist, wird eine Zeile hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="66f29-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="66f29-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66f29-147">See also</span></span>



[<span data-ttu-id="66f29-148">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="66f29-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

