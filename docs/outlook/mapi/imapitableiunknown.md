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
ms.openlocfilehash: a5504711bdeac4ef94cbe47395ceb8163b60ad68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584331"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="5a017-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a017-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="5a017-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a017-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a017-105">Stellt eine schreibgeschützte Ansicht einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5a017-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="5a017-106">**IMAPITable** wird von Clients und -Dienstanbieter verwendet, um die Möglichkeit zu bearbeiten, die eine Tabelle angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5a017-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a017-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5a017-107">Header file:</span></span>  <br/> |<span data-ttu-id="5a017-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a017-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5a017-109">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="5a017-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="5a017-110">Table-Objekte</span><span class="sxs-lookup"><span data-stu-id="5a017-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="5a017-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5a017-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5a017-112">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="5a017-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="5a017-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5a017-113">Called by:</span></span>  <br/> |<span data-ttu-id="5a017-114">Dienstanbieter-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="5a017-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="5a017-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="5a017-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5a017-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="5a017-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="5a017-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="5a017-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="5a017-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="5a017-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5a017-119">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="5a017-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5a017-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="5a017-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="5a017-121">Gibt eine [MAPIERROR](mapierror.md) -Struktur mit Informationen über den vorherigen Fehler in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="5a017-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="5a017-122">Beraten</span><span class="sxs-lookup"><span data-stu-id="5a017-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="5a017-123">Um die Benachrichtigung der Auswirkungen auf die Tabelle angegebenen Ereignisse registriert.</span><span class="sxs-lookup"><span data-stu-id="5a017-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="5a017-124">Heben Sie diesen Vorgang</span><span class="sxs-lookup"><span data-stu-id="5a017-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="5a017-125">Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode **IMAPITable::Advise** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="5a017-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="5a017-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="5a017-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="5a017-127">Status und Typ der Tabelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5a017-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="5a017-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="5a017-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="5a017-129">Definiert die jeweiligen Eigenschaften und die Reihenfolge der Eigenschaften als Spalten in der Tabelle angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5a017-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="5a017-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="5a017-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="5a017-131">Gibt eine Liste mit Spalten für die Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="5a017-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="5a017-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="5a017-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="5a017-133">Gibt die Gesamtzahl der Zeilen in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="5a017-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="5a017-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="5a017-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="5a017-135">Verschiebt den Cursor an eine bestimmte Position in der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="5a017-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="5a017-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="5a017-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="5a017-137">Verschiebt den Cursor an eine ungefähre Bruch Position in der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="5a017-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="5a017-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="5a017-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="5a017-139">Ruft die aktuelle Tabelle Zeilenposition des Cursors, basierend auf einem Bruch Wert.</span><span class="sxs-lookup"><span data-stu-id="5a017-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="5a017-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="5a017-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="5a017-141">Findet die nächste Zeile in einer Tabelle, die bestimmte Suchkriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="5a017-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="5a017-142">Einschränken</span><span class="sxs-lookup"><span data-stu-id="5a017-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="5a017-143">Wendet einen Filter auf eine Tabelle, reduzieren die Zeile festgelegt, um nur die Zeilen, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5a017-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="5a017-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="5a017-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="5a017-145">Markiert die aktuelle Position der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5a017-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="5a017-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="5a017-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="5a017-147">Gibt ein Lesezeichen zugeordneten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="5a017-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="5a017-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="5a017-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="5a017-149">Sortiert die Zeilen der Tabelle basierend auf Sortierkriterien.</span><span class="sxs-lookup"><span data-stu-id="5a017-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="5a017-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="5a017-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="5a017-151">Ruft die aktuelle Sortierreihenfolge für eine Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="5a017-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="5a017-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="5a017-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="5a017-153">Gibt eine oder mehrere Zeilen aus einer Tabelle, beginnend bei der aktuellen Cursorposition zurück.</span><span class="sxs-lookup"><span data-stu-id="5a017-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="5a017-154">Abbruch</span><span class="sxs-lookup"><span data-stu-id="5a017-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="5a017-155">Beendet die asynchrone Vorgänge derzeit in Arbeit für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5a017-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="5a017-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="5a017-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="5a017-157">Erweitert eine reduzierte Tabellenkategorie, der Kategorie zur Tabellenansicht Endknoten Zeilen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5a017-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="5a017-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="5a017-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="5a017-159">Blendet eine Tabellenkategorie für erweiterte, entfernen die Endknoten Zeilen aus der Tabellenansicht für die Kategorie gehören.</span><span class="sxs-lookup"><span data-stu-id="5a017-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="5a017-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5a017-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="5a017-161">Unterbricht die Verarbeitung, bis eine oder mehrere asynchrone Vorgänge in Bearbeitung in der Tabelle abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="5a017-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="5a017-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="5a017-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="5a017-163">Gibt die Daten, die erforderlich sind, um die aktuelle neu erstellen erweitert oder reduziert Zustand einer kategorisierten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5a017-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="5a017-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="5a017-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="5a017-165">Erstellt den aktuellen erweiterten oder reduzierten den Status einer kategorisierten Tabelle mit Daten, die durch einen vorherigen Aufruf der **IMAPITable::GetCollapseState** -Methode gespeichert wurde neu.</span><span class="sxs-lookup"><span data-stu-id="5a017-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a017-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a017-166">See also</span></span>



[<span data-ttu-id="5a017-167">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5a017-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

