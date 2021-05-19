---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420115"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="59fb0-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="59fb0-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="59fb0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59fb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59fb0-105">Bietet eine schreibgeschützte Ansicht einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="59fb0-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="59fb0-106">**IMAPITable** wird von Clients und Dienstanbietern verwendet, um die Art und Weise zu ändern, wie eine Tabelle angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="59fb0-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59fb0-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="59fb0-107">Header file:</span></span>  <br/> |<span data-ttu-id="59fb0-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59fb0-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="59fb0-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="59fb0-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="59fb0-110">Tabellenobjekte</span><span class="sxs-lookup"><span data-stu-id="59fb0-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="59fb0-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="59fb0-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="59fb0-112">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="59fb0-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="59fb0-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="59fb0-113">Called by:</span></span>  <br/> |<span data-ttu-id="59fb0-114">Clientanwendungen, Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="59fb0-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="59fb0-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="59fb0-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="59fb0-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="59fb0-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="59fb0-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="59fb0-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="59fb0-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="59fb0-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="59fb0-119">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="59fb0-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="59fb0-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="59fb0-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="59fb0-121">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler in der Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="59fb0-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-122">Raten</span><span class="sxs-lookup"><span data-stu-id="59fb0-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="59fb0-123">Registriert, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Tabelle ausdingen.</span><span class="sxs-lookup"><span data-stu-id="59fb0-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="59fb0-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="59fb0-125">Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **IMAPITable::Advise-Methode eingerichtet** wurden.</span><span class="sxs-lookup"><span data-stu-id="59fb0-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="59fb0-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="59fb0-127">Gibt den Status und Typ der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="59fb0-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="59fb0-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="59fb0-129">Definiert die bestimmten Eigenschaften und die Reihenfolge der Eigenschaften, die in der Tabelle als Spalten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59fb0-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="59fb0-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="59fb0-131">Gibt eine Liste der Spalten für die Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="59fb0-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="59fb0-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="59fb0-133">Gibt die Gesamtanzahl der Zeilen in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="59fb0-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="59fb0-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="59fb0-135">Verschiebt den Cursor an eine bestimmte Position in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="59fb0-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="59fb0-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="59fb0-137">Verschiebt den Cursor an eine ungefähre Bruchposition in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="59fb0-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="59fb0-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="59fb0-139">Ruft die aktuelle Tabellenzeile des Cursors basierend auf einem Bruchwert ab.</span><span class="sxs-lookup"><span data-stu-id="59fb0-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="59fb0-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="59fb0-141">Sucht die nächste Zeile in einer Tabelle, die bestimmten Suchkriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="59fb0-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-142">Restrict</span><span class="sxs-lookup"><span data-stu-id="59fb0-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="59fb0-143">Wendet einen Filter auf eine Tabelle an, wodurch der Zeilensatz auf nur die Zeilen reduziert wird, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="59fb0-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="59fb0-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="59fb0-145">Markiert die aktuelle Position der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="59fb0-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="59fb0-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="59fb0-147">Gibt den Speicher frei, der einer Textmarke zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="59fb0-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="59fb0-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="59fb0-149">Ordnet die Zeilen der Tabelle basierend auf Sortierkriterien an.</span><span class="sxs-lookup"><span data-stu-id="59fb0-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="59fb0-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="59fb0-151">Ruft die aktuelle Sortierreihenfolge für eine Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="59fb0-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="59fb0-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="59fb0-153">Gibt eine oder mehrere Zeilen aus einer Tabelle zurück, beginnend an der aktuellen Cursorposition.</span><span class="sxs-lookup"><span data-stu-id="59fb0-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-154">Abbruch</span><span class="sxs-lookup"><span data-stu-id="59fb0-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="59fb0-155">Beendet alle asynchronen Vorgänge, die derzeit für die Tabelle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="59fb0-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="59fb0-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="59fb0-157">Erweitert eine reduzierte Tabellenkategorie und fügt der Tabellenansicht die Blattzeilen hinzu, die zu der Kategorie gehören.</span><span class="sxs-lookup"><span data-stu-id="59fb0-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="59fb0-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="59fb0-159">Reduziert eine erweiterte Tabellenkategorie und entfernt die Blattzeilen, die zur Kategorie gehören, aus der Tabellenansicht.</span><span class="sxs-lookup"><span data-stu-id="59fb0-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="59fb0-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="59fb0-161">Die Verarbeitung wird angehalten, bis ein oder mehrere asynchrone Vorgänge in der Tabelle abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="59fb0-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="59fb0-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="59fb0-163">Gibt die Daten zurück, die zum Neuerstellen des aktuellen reduzierten oder erweiterten Zustands einer kategorisierten Tabelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="59fb0-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="59fb0-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="59fb0-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="59fb0-165">Erstellt den aktuellen erweiterten oder reduzierten Zustand einer kategorisierten Tabelle mithilfe von Daten, die durch einen vorherigen Aufruf der **IMAPITable::GetCollapseState-Methode gespeichert** wurden.</span><span class="sxs-lookup"><span data-stu-id="59fb0-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59fb0-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59fb0-166">See also</span></span>



[<span data-ttu-id="59fb0-167">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="59fb0-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

