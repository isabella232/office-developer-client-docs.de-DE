---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411617"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="5b494-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="5b494-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="5b494-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b494-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b494-105">Legt die Standardsortierreihenfolge für die Inhaltstabelle eines Ordners fest.</span><span class="sxs-lookup"><span data-stu-id="5b494-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5b494-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b494-106">Parameters</span></span>

 <span data-ttu-id="5b494-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="5b494-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="5b494-108">in Ein Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die Standardsortierreihenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="5b494-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="5b494-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b494-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5b494-110">in Eine Bitmaske von Flags, die die Festlegung der Standardsortierreihenfolge steuert.</span><span class="sxs-lookup"><span data-stu-id="5b494-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="5b494-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5b494-111">The following flag can be set:</span></span>
    
<span data-ttu-id="5b494-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="5b494-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="5b494-113">Die Standardeinstellung für die Sortierreihenfolge gilt für den angegebenen Ordner und alle Unterordner.</span><span class="sxs-lookup"><span data-stu-id="5b494-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b494-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b494-114">Return value</span></span>

<span data-ttu-id="5b494-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b494-115">S_OK</span></span> 
  
> <span data-ttu-id="5b494-116">Die Sortierreihenfolge wurde erfolgreich gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5b494-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="5b494-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5b494-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5b494-118">Der Nachrichtenspeicher Anbieter unterstützt das Speichern einer Sortierreihenfolge für die Ordnerinhaltstabellen nicht.</span><span class="sxs-lookup"><span data-stu-id="5b494-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b494-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b494-119">Remarks</span></span>

<span data-ttu-id="5b494-120">Die **IMAPIFolder:: SaveContentsSort** -Methode richtet eine Standardsortierreihenfolge für die Inhaltstabelle eines Ordners ein.</span><span class="sxs-lookup"><span data-stu-id="5b494-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="5b494-121">Wenn ein Client die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode des Ordners aufruft, nachdem der Code **SaveContentsSort**aufgerufen hat, werden die Zeilen in der Tabelle zurückgegebene Inhalte in der von **SaveContentsSort**festgelegten Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b494-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="5b494-122">Nicht alle Nachrichtenspeicher Anbieter unterstützen **SaveContentsSort**; Es ist akzeptabel, dass Nachrichtenspeicher Anbieter MAPI_E_NO_SUPPORT von der **SaveContentsSort** -Methode zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5b494-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5b494-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b494-123">See also</span></span>



[<span data-ttu-id="5b494-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="5b494-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="5b494-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="5b494-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="5b494-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5b494-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

