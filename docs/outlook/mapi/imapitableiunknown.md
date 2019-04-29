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
# <a name="imapitable--iunknown"></a><span data-ttu-id="c0e93-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0e93-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="c0e93-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0e93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0e93-105">Stellt eine schreibgeschützte Ansicht einer Tabelle bereit.</span><span class="sxs-lookup"><span data-stu-id="c0e93-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="c0e93-106">**IMAPITable** wird von Clients und Dienstanbietern verwendet, um die Art und Weise zu manipulieren, in der eine Tabelle angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c0e93-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0e93-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c0e93-107">Header file:</span></span>  <br/> |<span data-ttu-id="c0e93-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c0e93-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c0e93-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="c0e93-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="c0e93-110">Tabellenobjekte</span><span class="sxs-lookup"><span data-stu-id="c0e93-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="c0e93-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c0e93-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="c0e93-112">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="c0e93-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="c0e93-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c0e93-113">Called by:</span></span>  <br/> |<span data-ttu-id="c0e93-114">Client Anwendungen, Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c0e93-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="c0e93-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="c0e93-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c0e93-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="c0e93-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="c0e93-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="c0e93-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="c0e93-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="c0e93-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c0e93-119">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="c0e93-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c0e93-120">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="c0e93-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="c0e93-121">Gibt eine [MAPIERROR](mapierror.md) -Struktur mit Informationen über den vorherigen Fehler in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="c0e93-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-122">Beraten</span><span class="sxs-lookup"><span data-stu-id="c0e93-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="c0e93-123">Registriert die Benachrichtigung über angegebene Ereignisse, die sich auf die Tabelle auswirken.</span><span class="sxs-lookup"><span data-stu-id="c0e93-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="c0e93-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="c0e93-125">Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **IMAPITable:: Advise** -Methode eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="c0e93-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="c0e93-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="c0e93-127">Gibt den Status und den Typ der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="c0e93-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="c0e93-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="c0e93-129">Definiert die Eigenschaften und die Reihenfolge der Eigenschaften, die als Spalten in der Tabelle angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c0e93-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="c0e93-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="c0e93-131">Gibt eine Liste der Spalten für die Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="c0e93-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="c0e93-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="c0e93-133">Gibt die Gesamtanzahl der Zeilen in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="c0e93-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="c0e93-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="c0e93-135">Verschiebt den Cursor an eine bestimmte Position in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c0e93-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="c0e93-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="c0e93-137">Verschiebt den Cursor an eine ungefähre Bruchposition in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c0e93-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="c0e93-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="c0e93-139">Ruft die aktuelle Tabellenzeilen Position des Cursors basierend auf einem Dezimalwert ab.</span><span class="sxs-lookup"><span data-stu-id="c0e93-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="c0e93-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="c0e93-141">Sucht die nächste Zeile in einer Tabelle, die bestimmten Suchkriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="c0e93-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-142">Restrict</span><span class="sxs-lookup"><span data-stu-id="c0e93-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="c0e93-143">Wendet einen Filter auf eine Tabelle an, wobei der Zeilensatz nur auf die Zeilen reduziert wird, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c0e93-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="c0e93-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="c0e93-145">Markiert die aktuelle Position der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c0e93-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="c0e93-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="c0e93-147">Gibt den mit einer Textmarke verknüpften Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="c0e93-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="c0e93-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="c0e93-149">Sortiert die Zeilen der Tabelle basierend auf Sortierkriterien.</span><span class="sxs-lookup"><span data-stu-id="c0e93-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="c0e93-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="c0e93-151">Ruft die aktuelle Sortierreihenfolge für eine Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="c0e93-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="c0e93-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="c0e93-153">Gibt eine oder mehrere Zeilen aus einer Tabelle zurück, die an der aktuellen Cursorposition beginnen.</span><span class="sxs-lookup"><span data-stu-id="c0e93-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-154">Abbruch</span><span class="sxs-lookup"><span data-stu-id="c0e93-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="c0e93-155">Beendet alle asynchronen Vorgänge, die derzeit für die Tabelle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c0e93-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="c0e93-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="c0e93-157">Erweitert eine reduzierte Tabellen Kategorie, indem Sie der Tabellenansicht die Blattzeilen hinzufügt, die der Kategorie angehören.</span><span class="sxs-lookup"><span data-stu-id="c0e93-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="c0e93-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="c0e93-159">Reduziert eine erweiterte Tabellen Kategorie und entfernt die Blattzeilen der Kategorie aus der Tabellenansicht.</span><span class="sxs-lookup"><span data-stu-id="c0e93-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="c0e93-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="c0e93-161">Hält die Verarbeitung an, bis mindestens ein asynchroner Vorgang abgeschlossen ist, der in der Tabelle ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="c0e93-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="c0e93-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="c0e93-163">Gibt die Daten zurück, die zum Neuaufbau des aktuellen reduzierten oder erweiterten Status einer kategorisierten Tabelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c0e93-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="c0e93-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="c0e93-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="c0e93-165">Erstellt den aktuellen erweiterten oder reduzierten Status einer kategorisierten Tabelle mithilfe von Daten, die durch einen vorherigen Aufruf der **IMAPITable:: GetCollapseState** -Methode gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="c0e93-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0e93-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0e93-166">See also</span></span>



[<span data-ttu-id="c0e93-167">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c0e93-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

