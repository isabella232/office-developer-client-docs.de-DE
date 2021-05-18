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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408824"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="04e24-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="04e24-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="04e24-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04e24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04e24-105">Erstellt eine Textmarke an der aktuellen Position der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="04e24-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="04e24-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04e24-106">Parameters</span></span>

 <span data-ttu-id="04e24-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="04e24-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="04e24-108">[out] Zeiger auf den zurückgegebenen 32-Bit-Lesezeichenwert.</span><span class="sxs-lookup"><span data-stu-id="04e24-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="04e24-109">Diese Textmarke kann später in einem Aufruf der [IMAPITable::SeekRow-Methode übergeben](imapitable-seekrow.md) werden.</span><span class="sxs-lookup"><span data-stu-id="04e24-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="04e24-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04e24-110">Return value</span></span>

<span data-ttu-id="04e24-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="04e24-111">S_OK</span></span> 
  
> <span data-ttu-id="04e24-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="04e24-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="04e24-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="04e24-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="04e24-114">Der angeforderte Vorgang konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="04e24-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04e24-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04e24-115">Remarks</span></span>

<span data-ttu-id="04e24-116">Die **IMAPITable::CreateBookmark-Methode** markiert eine Tabellenposition, indem ein Wert erstellt wird, der als Lesezeichen bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="04e24-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="04e24-117">Eine Textmarke kann verwendet werden, um an die position zurückzukehren, die durch die Textmarke identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="04e24-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="04e24-118">Die Position mit Textmarken ist dem Objekt in dieser Zeile in der Tabelle zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="04e24-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="04e24-119">Lesezeichen werden in Anlagentabellen nicht unterstützt, und Anlagentabellenimplementierungen von **CreateBookmark** geben MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="04e24-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="04e24-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="04e24-120">Notes to implementers</span></span>

<span data-ttu-id="04e24-121">Beschränken Sie aufgrund der Speicherkosten für die Verwaltung von Cursorpositionen mit Textmarken die Anzahl der Lesezeichen, die Sie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="04e24-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="04e24-122">Wenn Sie diese Nummer erreichen, geben MAPI_E_UNABLE_TO_COMPLETE von allen nachfolgenden Aufrufen an **CreateBookmark zurück.**</span><span class="sxs-lookup"><span data-stu-id="04e24-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="04e24-123">Manchmal verweist eine Textmarke auf eine Zeile, die sich nicht mehr in der Tabellenansicht befindet.</span><span class="sxs-lookup"><span data-stu-id="04e24-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="04e24-124">Wenn ein Aufrufer ein solches Lesezeichen verwendet, verschieben Sie den Cursor zur nächsten sichtbaren Zeile, und halten Sie dort an.</span><span class="sxs-lookup"><span data-stu-id="04e24-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="04e24-125">Wenn der Aufrufer versucht, eine Textmarke zu verwenden, die auf eine nicht lesbare Zeile verweisen soll, da sie reduziert wurde, geben Sie MAPI_W_POSITION_CHANGED nach dem Verschieben der Textmarke zurück.</span><span class="sxs-lookup"><span data-stu-id="04e24-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="04e24-126">Sie können die Textmarke entweder zu diesem Zeitpunkt oder bei einem Kollaps in der **SetCollapseState-Methode** in der nächsten sichtbaren Zeile neu positionieren.</span><span class="sxs-lookup"><span data-stu-id="04e24-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="04e24-127">Wenn Sie die Textmarke zu dem Zeitpunkt verschieben, zu dem die Zeile reduziert wird, müssen Sie ein Bit in der Textmarke beibehalten, das genau angibt, wann die Textmarke verschoben wurde: seit der letzten Verwendung oder wenn sie seit der Erstellung nie verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="04e24-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="04e24-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="04e24-128">Notes to callers</span></span>

 <span data-ttu-id="04e24-129">**CreateBookmark weist** dem erstellten Lesezeichen Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="04e24-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="04e24-130">Geben Sie die Ressourcen für die Textmarke frei, indem Sie die [IMAPITable::FreeBookmark-Methode](imapitable-freebookmark.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="04e24-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04e24-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04e24-131">See also</span></span>



[<span data-ttu-id="04e24-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="04e24-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="04e24-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="04e24-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="04e24-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="04e24-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

