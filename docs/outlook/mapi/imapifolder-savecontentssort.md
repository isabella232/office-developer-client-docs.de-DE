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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7c8ccada96b3e34372d488e16c85627e8b6b0cd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792115"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="84e5d-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="84e5d-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="84e5d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84e5d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84e5d-105">Legt die Standard-Sortierreihenfolge für einen Ordner Inhaltstabelle fest.</span><span class="sxs-lookup"><span data-stu-id="84e5d-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="84e5d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84e5d-106">Parameters</span></span>

 <span data-ttu-id="84e5d-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="84e5d-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="84e5d-108">[in] Ein Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die Sortierreihenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="84e5d-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="84e5d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="84e5d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="84e5d-110">[in] Eine Bitmaske aus Flags, die steuert, wie die Sortierreihenfolge festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="84e5d-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="84e5d-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="84e5d-111">The following flag can be set:</span></span>
    
<span data-ttu-id="84e5d-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="84e5d-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="84e5d-113">Der Sortierung Reihenfolge Standardsatz gilt für den angegebenen Ordner und für alle Unterordner.</span><span class="sxs-lookup"><span data-stu-id="84e5d-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84e5d-114">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="84e5d-114">Return value</span></span>

<span data-ttu-id="84e5d-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="84e5d-115">S_OK</span></span> 
  
> <span data-ttu-id="84e5d-116">Die Sortierreihenfolge wurde erfolgreich gespeichert.</span><span class="sxs-lookup"><span data-stu-id="84e5d-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="84e5d-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="84e5d-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="84e5d-118">Die Nachrichtenanbieter unterstützt keine Sortierreihenfolge für ihre Ordner Inhalt Tabellen speichern.</span><span class="sxs-lookup"><span data-stu-id="84e5d-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84e5d-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="84e5d-119">Remarks</span></span>

<span data-ttu-id="84e5d-120">Die **IMAPIFolder::SaveContentsSort** -Methode stellt eine standardmäßige Sortierreihenfolge für einen Ordner Inhaltstabelle her.</span><span class="sxs-lookup"><span data-stu-id="84e5d-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="84e5d-121">D. h., wenn ein Client nach der Code ruft **SaveContentsSort**den Ordner [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode aufruft, werden die Zeilen in der Inhaltstabelle zurückgegebene in der Reihenfolge von **SaveContentsSort**hergestellt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84e5d-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="84e5d-122">Nachricht nicht alle Anbieter unterstützen **SaveContentsSort**. Es ist akzeptabel für Nachricht Anbieter MAPI_E_NO_SUPPORT aus der **SaveContentsSort** -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="84e5d-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="84e5d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84e5d-123">See also</span></span>



[<span data-ttu-id="84e5d-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="84e5d-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="84e5d-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="84e5d-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="84e5d-126">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="84e5d-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

