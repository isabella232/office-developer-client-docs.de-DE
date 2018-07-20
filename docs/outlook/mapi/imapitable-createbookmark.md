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
ms.openlocfilehash: 34bd6de95f731c03466f19e0bc4fd6e2c9910900
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792445"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="779cb-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="779cb-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="779cb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="779cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="779cb-105">Erstellt eine Textmarke an der aktuellen Position der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="779cb-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="779cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="779cb-106">Parameters</span></span>

 <span data-ttu-id="779cb-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="779cb-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="779cb-108">[out] Zeiger auf den zurückgegebenen Textmarke für 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="779cb-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="779cb-109">Dieses Lesezeichen kann später in einem Aufruf der [IMAPITable::SeekRow](imapitable-seekrow.md) -Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="779cb-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="779cb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="779cb-110">Return value</span></span>

<span data-ttu-id="779cb-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="779cb-111">S_OK</span></span> 
  
> <span data-ttu-id="779cb-112">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="779cb-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="779cb-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="779cb-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="779cb-114">Der angeforderte Vorgang konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="779cb-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="779cb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="779cb-115">Remarks</span></span>

<span data-ttu-id="779cb-116">Die **IMAPITable::CreateBookmark** -Methode markiert die Position einer Tabelle, indem Sie einen Wert eine Textmarke namens erstellen.</span><span class="sxs-lookup"><span data-stu-id="779cb-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="779cb-117">Eine Textmarke kann verwendet werden, um an der Position der Textmarke identifizierten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="779cb-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="779cb-118">Die mit einer Textmarke versehenen Position ist das Row-Objekts in der Tabelle-Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="779cb-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="779cb-119">Lesezeichen auf Anlagentabellen nicht unterstützt werden, und Anlage Tabelle Implementierungen von **CreateBookmark** MAPI_E_NO_SUPPORT zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="779cb-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="779cb-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="779cb-120">Notes to implementers</span></span>

<span data-ttu-id="779cb-121">Aufgrund der Arbeitsspeicher Ausgaben Cursorpositionen mit Lesezeichen zu verwalten die Anzahl der Textmarken, die Sie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="779cb-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="779cb-122">Wenn diese Nummer erreicht ist, geben alle nachfolgenden Aufrufe **CreateBookmark**MAPI_E_UNABLE_TO_COMPLETE zurück.</span><span class="sxs-lookup"><span data-stu-id="779cb-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="779cb-123">In einigen Fällen zeigt ein Lesezeichen auf eine Zeile, die nicht mehr in der Tabellenansicht ist ein.</span><span class="sxs-lookup"><span data-stu-id="779cb-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="779cb-124">Wenn ein Anrufer solche eine Textmarke verwendet wird, bewegen Sie den Cursor in die nächste Zeile sichtbar und noch mehr.</span><span class="sxs-lookup"><span data-stu-id="779cb-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="779cb-125">Wenn der Aufrufer versucht, ein Lesezeichen zu verwenden, die auf ein sichtbares Zeile verweist, da es reduziert wurde, geben Sie nach dem Verschieben der Textmarke MAPI_W_POSITION_CHANGED zurück.</span><span class="sxs-lookup"><span data-stu-id="779cb-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="779cb-126">Sie können die Textmarke in die nächste Zeile sichtbar zu diesem Zeitpunkt oder wenn tritt auf, in der **SetCollapseState** -Methode der reduzieren positionieren.</span><span class="sxs-lookup"><span data-stu-id="779cb-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="779cb-127">Wenn Sie die Textmarke Zeitpunkt die Zeile reduziert ist verschieben, Sie müssen beibehalten etwas in die Textmarke, der angibt, wann genau die Textmarke verschoben wurde: seit der letzten verwenden, oder wenn es seit seiner Erstellung nie verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="779cb-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="779cb-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="779cb-128">Notes to callers</span></span>

 <span data-ttu-id="779cb-129">**CreateBookmark** weist Speicher für die Textmarke erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="779cb-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="779cb-130">Geben Sie die Ressourcen für das Lesezeichen durch Aufrufen der [IMAPITable::FreeBookmark](imapitable-freebookmark.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="779cb-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="779cb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="779cb-131">See also</span></span>



[<span data-ttu-id="779cb-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="779cb-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="779cb-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="779cb-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="779cb-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="779cb-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

