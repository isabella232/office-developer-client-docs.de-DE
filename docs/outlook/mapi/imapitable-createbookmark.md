---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c251dacce0d4e1743a74f1ba45e395b6e1c05064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329008"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="27c3e-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="27c3e-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="27c3e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27c3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27c3e-105">Erstellt eine Textmarke an der aktuellen Position der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="27c3e-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="27c3e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="27c3e-106">Parameters</span></span>

 <span data-ttu-id="27c3e-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="27c3e-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="27c3e-108">Out Zeiger auf den zurückgegebenen 32-Bit-Lesezeichenwert.</span><span class="sxs-lookup"><span data-stu-id="27c3e-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="27c3e-109">Diese Textmarke kann später in einem Aufruf an die [IMAPITable:: SeekRow](imapitable-seekrow.md) -Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="27c3e-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="27c3e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27c3e-110">Return value</span></span>

<span data-ttu-id="27c3e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="27c3e-111">S_OK</span></span> 
  
> <span data-ttu-id="27c3e-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="27c3e-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="27c3e-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="27c3e-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="27c3e-114">Der angeforderte Vorgang konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="27c3e-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27c3e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27c3e-115">Remarks</span></span>

<span data-ttu-id="27c3e-116">Die **IMAPITable:: CreateBookMark** -Methode kennzeichnet eine Tabellenposition durch Erstellen eines Werts, der als Textmarke bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="27c3e-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="27c3e-117">Eine Textmarke kann verwendet werden, um zu der durch die Textmarke identifizierten Position zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="27c3e-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="27c3e-118">Die Lesezeichenposition ist dem Objekt in dieser Zeile in der Tabelle zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="27c3e-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="27c3e-119">Lesezeichen werden für Anlagen Tabellen und für Anlagen Tabellen Implementierungen von **CreateBookMark** Return MAPI_E_NO_SUPPORT nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27c3e-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="27c3e-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="27c3e-120">Notes to implementers</span></span>

<span data-ttu-id="27c3e-121">Aufgrund der Arbeitsspeicherkosten für die Verwaltung von Cursorpositionen mit Lesezeichen können Sie die Anzahl der zu erstellende Textmarken begrenzen.</span><span class="sxs-lookup"><span data-stu-id="27c3e-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="27c3e-122">Wenn Sie diese Nummer erreicht haben, geben Sie MAPI_E_UNABLE_TO_COMPLETE von allen nachfolg \*\*\*\* enden Aufrufen von CreateBookMark zurück.</span><span class="sxs-lookup"><span data-stu-id="27c3e-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="27c3e-123">Manchmal verweist eine Textmarke auf eine Zeile, die sich nicht mehr in der Tabellenansicht befindet.</span><span class="sxs-lookup"><span data-stu-id="27c3e-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="27c3e-124">Wenn ein Anrufer ein solches Lesezeichen verwendet, bewegen Sie den Cursor zur nächsten sichtbaren Zeile, und halten Sie dort an.</span><span class="sxs-lookup"><span data-stu-id="27c3e-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="27c3e-125">Wenn der Aufrufer versucht, ein Lesezeichen zu verwenden, das auf eine nicht sichtbare Zeile zeigt, da es reduziert wurde, geben Sie MAPI_W_POSITION_CHANGED nach dem Bewegen der Textmarke zurück.</span><span class="sxs-lookup"><span data-stu-id="27c3e-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="27c3e-126">Sie können die Textmarke entweder zu diesem Zeitpunkt oder in der **SetCollapseState** -Methode in die nächste sichtbare Zeile verschieben.</span><span class="sxs-lookup"><span data-stu-id="27c3e-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="27c3e-127">Wenn Sie die Textmarke zu dem Zeitpunkt verschieben, zu dem die Zeile reduziert wird, müssen Sie ein Bit in der Textmarke aufbewahren, die genau angibt, wann das Lesezeichen verschoben wurde: seit der letzten Verwendung oder wenn es nie seit seiner Erstellung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="27c3e-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="27c3e-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="27c3e-128">Notes to callers</span></span>

 <span data-ttu-id="27c3e-129">**CreateBookMark** reserviert Speicher für die erstellte Textmarke.</span><span class="sxs-lookup"><span data-stu-id="27c3e-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="27c3e-130">Geben Sie die Ressourcen für das Lesezeichen frei, indem Sie die [IMAPITable:: FreeBookmark](imapitable-freebookmark.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="27c3e-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="27c3e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27c3e-131">See also</span></span>



[<span data-ttu-id="27c3e-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="27c3e-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="27c3e-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="27c3e-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="27c3e-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="27c3e-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

