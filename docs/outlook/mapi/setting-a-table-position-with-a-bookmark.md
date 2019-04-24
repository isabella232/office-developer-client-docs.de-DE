---
title: Festlegen einer Tabellen Position mit einer textMarke
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351233"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="36c49-103">Festlegen einer Tabellen Position mit einer textMarke</span><span class="sxs-lookup"><span data-stu-id="36c49-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="36c49-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36c49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36c49-105">Eine Textmarke ist eine Ressource, die eine bestimmte Position in einer Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="36c49-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="36c49-106">Durch das Festlegen einer Textmarke wird es möglich, zu einem späteren Zeitpunkt zu einer Position zurückzukehren, eine Funktion, die die Leistung von Tabellenoperationen erheblich verbessern kann.</span><span class="sxs-lookup"><span data-stu-id="36c49-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="36c49-107">MAPI definiert drei Standard Lesezeichen:</span><span class="sxs-lookup"><span data-stu-id="36c49-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36c49-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="36c49-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="36c49-109">Zeigt auf die aktuelle Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="36c49-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="36c49-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="36c49-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="36c49-111">Zeigt auf die erste Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="36c49-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="36c49-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="36c49-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="36c49-113">Zeigt auf die letzte Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="36c49-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="36c49-114">Tabellen Implementierer sind erforderlich, um diese Standard Lesezeichen zu unterstützen und andere zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="36c49-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="36c49-115">Da Lesezeichen jedoch Ressourcen sind und Ressourcen begrenzt sind, sollten Bookmark-Benutzer Sie so bald wie möglich freigeben.</span><span class="sxs-lookup"><span data-stu-id="36c49-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="36c49-116">**So legen Sie ein Lesezeichen an der aktuellen Tabellenposition fest**</span><span class="sxs-lookup"><span data-stu-id="36c49-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="36c49-117">Rufen Sie [IMAPITable:: CreateBookMark](imapitable-createbookmark.md)auf.</span><span class="sxs-lookup"><span data-stu-id="36c49-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="36c49-118">Gelegentlich ist nicht genügend Arbeitsspeicher verfügbar, um die neue Textmarke zu \*\*\*\* reservieren, wodurch CreateBookMark den MAPI_E_UNABLE_TO_COMPLETE-Fehlerwert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="36c49-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="36c49-119">**So geben Sie ein Lesezeichen frei**</span><span class="sxs-lookup"><span data-stu-id="36c49-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="36c49-120">Rufen Sie [IMAPITable:: FreeBookmark](imapitable-freebookmark.md)auf.</span><span class="sxs-lookup"><span data-stu-id="36c49-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="36c49-121">**So bewegen Sie den Cursor an eine Textmarke**</span><span class="sxs-lookup"><span data-stu-id="36c49-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="36c49-122">Rufen Sie [IMAPITable:: SeekRow](imapitable-seekrow.md)auf.</span><span class="sxs-lookup"><span data-stu-id="36c49-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="36c49-123">**SeekRow** legt einen neuen Wert für die BOOKMARK_CURRENT-Position fest.</span><span class="sxs-lookup"><span data-stu-id="36c49-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="36c49-124">**SeekRow** kann verwendet werden, um beispielsweise eine Tabelle mit zehn Zeilen von der aktuellen Position aus zu positionieren oder am Anfang zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="36c49-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="36c49-125">Clients oder Dienstanbieter können nach dem aktuellen, Anfang oder Ende einer Tabelle oder einer anderen Position suchen, die mit einer vordefinierten Textmarke verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="36c49-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="36c49-126">Sie können entweder vorwärts oder rückwärts navigieren und den Vorgang auf eine bestimmte Anzahl von Zeilen begrenzen.</span><span class="sxs-lookup"><span data-stu-id="36c49-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="36c49-127">In der Regel sollten Anrufer nicht mehr als 50 Zeilen mit **SeekRow**suchen; [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) sollte mit einer größeren Anzahl von Zeilen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36c49-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="36c49-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36c49-128">See also</span></span>



[<span data-ttu-id="36c49-129">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="36c49-129">MAPI Tables</span></span>](mapi-tables.md)

