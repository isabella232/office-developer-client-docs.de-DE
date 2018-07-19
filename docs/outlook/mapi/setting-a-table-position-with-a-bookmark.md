---
title: Festlegen einer Tabellenposition mit einer Textmarke
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d53f15cb439494ae99ff45509ed14c0928756d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795510"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="2374b-103">Festlegen einer Tabellenposition mit einer Textmarke</span><span class="sxs-lookup"><span data-stu-id="2374b-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="2374b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2374b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2374b-105">Eine Textmarke ist eine Ressource, die einem bestimmten Standort in einer Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="2374b-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="2374b-106">Festlegen einer Textmarke ermöglicht die, die auf eine Position zu einem späteren Zeitpunkt, ein Feature zurückzugeben, die der Tabellenvorgänge die Leistung erheblich verbessert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2374b-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="2374b-107">MAPI sind drei standard Textmarken definiert:</span><span class="sxs-lookup"><span data-stu-id="2374b-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2374b-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="2374b-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="2374b-109">Verweist auf die aktuelle Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2374b-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="2374b-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="2374b-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="2374b-111">Verweist auf die erste Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2374b-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="2374b-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="2374b-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="2374b-113">Verweist auf die letzte Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2374b-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="2374b-114">Tabelle Implementierer sind erforderlich, um diese standard Textmarken unterstützt und können auch andere Benutzer unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2374b-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="2374b-115">Jedoch sollten, da Textmarken Ressourcen sind und Ressourcen beschränkt sind, Textmarke Benutzer sie so bald wie möglich frei.</span><span class="sxs-lookup"><span data-stu-id="2374b-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="2374b-116">**So legen Sie eine Textmarke an der aktuellen Position der Tabelle fest**</span><span class="sxs-lookup"><span data-stu-id="2374b-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="2374b-117">Rufen Sie [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span><span class="sxs-lookup"><span data-stu-id="2374b-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="2374b-118">Gelegentlich wird nicht genügend Speicher zum Zuweisen der neuen Textmarke verursacht **CreateBookmark** zurückzugebenden den Fehlerwert MAPI_E_UNABLE_TO_COMPLETE vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2374b-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="2374b-119">**Eine Textmarke frei**</span><span class="sxs-lookup"><span data-stu-id="2374b-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="2374b-120">Rufen Sie [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span><span class="sxs-lookup"><span data-stu-id="2374b-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="2374b-121">**So verschieben Sie den Cursor auf eine Position mit einer Textmarke versehenen**</span><span class="sxs-lookup"><span data-stu-id="2374b-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="2374b-122">Rufen Sie [IMAPITable::SeekRow](imapitable-seekrow.md).</span><span class="sxs-lookup"><span data-stu-id="2374b-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="2374b-123">**SeekRow** stellt einen neuen Wert für die Position BOOKMARK_CURRENT her.</span><span class="sxs-lookup"><span data-stu-id="2374b-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="2374b-124">**SeekRow** kann, beispielsweise, wenn eine zehn Tabellenzeilen von der aktuellen Position anordnen oder neu am Anfang beginnen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2374b-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="2374b-125">Clients oder Dienstanbieter suchen, um die aktuelle beginnen, oder Beenden einer Tabelle oder einer beliebigen anderen Position, die eine vordefinierte Textmarke zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2374b-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="2374b-126">Sie können auf eine angegebene Anzahl von Zeilen in einer entweder vorwärts oder rückwärts ausgeführt und Grenzwert der Vorgang verschoben.</span><span class="sxs-lookup"><span data-stu-id="2374b-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="2374b-127">In der Regel sollten Aufrufer über nicht mehr als 50 Zeilen mit **SeekRow**seek; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) sollte mit einer größeren Anzahl von Zeilen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2374b-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2374b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2374b-128">See also</span></span>



[<span data-ttu-id="2374b-129">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="2374b-129">MAPI Tables</span></span>](mapi-tables.md)

