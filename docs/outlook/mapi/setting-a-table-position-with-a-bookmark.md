---
title: Festlegen einer Tabellenposition mit einem Lesezeichen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422460"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="e544c-103">Festlegen einer Tabellenposition mit einem Lesezeichen</span><span class="sxs-lookup"><span data-stu-id="e544c-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="e544c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e544c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e544c-105">Eine Textmarke ist eine Ressource, die einen bestimmten Speicherort in einer Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="e544c-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="e544c-106">Das Festlegen einer Textmarke ermöglicht es, zu einem späteren Zeitpunkt an eine Position zurückzukehren, ein Feature, das die Leistung von Tabellenvorgängen erheblich verbessern kann.</span><span class="sxs-lookup"><span data-stu-id="e544c-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="e544c-107">MAPI definiert drei Standardmarken:</span><span class="sxs-lookup"><span data-stu-id="e544c-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e544c-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="e544c-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="e544c-109">Zeigt auf die aktuelle Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e544c-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="e544c-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="e544c-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="e544c-111">Zeigt auf die erste Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e544c-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="e544c-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="e544c-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="e544c-113">Zeigt auf die letzte Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e544c-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="e544c-114">Tabellen implementierer sind erforderlich, um diese Standardmarken zu unterstützen und können auch andere unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e544c-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="e544c-115">Da Lesezeichen jedoch Ressourcen sind und Ressourcen begrenzt sind, sollten Lesezeichenbenutzer sie so bald wie möglich frei geben.</span><span class="sxs-lookup"><span data-stu-id="e544c-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="e544c-116">**So legen Sie eine Textmarke an der aktuellen Tabellenposition**</span><span class="sxs-lookup"><span data-stu-id="e544c-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="e544c-117">Rufen [Sie IMAPITable::CreateBookmark auf.](imapitable-createbookmark.md)</span><span class="sxs-lookup"><span data-stu-id="e544c-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="e544c-118">Gelegentlich ist nicht genügend Arbeitsspeicher verfügbar, um die neue Textmarke zuzuordnen, wodurch **CreateBookmark** den Fehlerwert MAPI_E_UNABLE_TO_COMPLETE zurück.</span><span class="sxs-lookup"><span data-stu-id="e544c-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="e544c-119">**So können Sie ein Lesezeichen frei**</span><span class="sxs-lookup"><span data-stu-id="e544c-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="e544c-120">Rufen [Sie IMAPITable::FreeBookmark auf.](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="e544c-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="e544c-121">**So verschieben Sie den Cursor an eine Position mit Textmarken**</span><span class="sxs-lookup"><span data-stu-id="e544c-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="e544c-122">Rufen [Sie IMAPITable::SeekRow auf.](imapitable-seekrow.md)</span><span class="sxs-lookup"><span data-stu-id="e544c-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="e544c-123">**SeekRow** richtet einen neuen Wert für die BOOKMARK_CURRENT ein.</span><span class="sxs-lookup"><span data-stu-id="e544c-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="e544c-124">**SeekRow** kann z. B. verwendet werden, um eine Tabelle zehn Zeilen von der aktuellen Position zu positionieren oder um am Anfang zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e544c-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="e544c-125">Clients oder Dienstanbieter können zum aktuellen, Beginnenden oder Ende einer Tabelle oder zu einer beliebigen anderen Position suchen, die einem vordefinierten Lesezeichen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e544c-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="e544c-126">Sie können sich vorwärts oder rückwärts bewegen und den Vorgang auf eine angegebene Anzahl von Zeilen beschränken.</span><span class="sxs-lookup"><span data-stu-id="e544c-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="e544c-127">In der Regel sollten Anrufer mit SeekRow nicht mehr als 50 **Zeilen durchsuchen.** [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) sollte mit einer größeren Anzahl von Zeilen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e544c-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e544c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e544c-128">See also</span></span>



[<span data-ttu-id="e544c-129">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="e544c-129">MAPI Tables</span></span>](mapi-tables.md)

