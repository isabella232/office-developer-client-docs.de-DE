---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1d486344ab20ef49488dbb911f3dd7000d64942e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571759"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="27629-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="27629-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="27629-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27629-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27629-105">Legt einen neuen Pfad für die Suche in das Profil, das für den Vorgang der Lösung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27629-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="27629-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="27629-106">Parameters</span></span>

 <span data-ttu-id="27629-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="27629-107">_ulFlags_</span></span>
  
> <span data-ttu-id="27629-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="27629-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="27629-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="27629-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="27629-110">[in] Ein Zeiger auf die [SRowSet](srowset.md) -Struktur verwendet, um den Suchpfad aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="27629-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="27629-111">Die erste Eigenschaft für jedes Mitglied **aRow** in **' srowset '** muss **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="27629-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="27629-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="27629-112">Return value</span></span>

<span data-ttu-id="27629-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="27629-113">S_OK</span></span> 
  
> <span data-ttu-id="27629-114">Der Suchpfad wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="27629-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="27629-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="27629-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="27629-116">Eine der in der Struktur **SRowSet** beschriebenen Container haben dessen **PR_ENTRYID** -Eigenschaft nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="27629-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="27629-117">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="27629-117">Remarks</span></span>

<span data-ttu-id="27629-118">Rufen die **SetSearchPath** -Methode, um die Änderungen zu speichern, die an die Reihenfolge des Containers Suche vorgenommen wurden, die zum Auflösen von Namen mit der [IAddrBook::ResolveName](iaddrbook-resolvename.md) -Methode verwendet wird, Clients und -Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="27629-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="27629-119">Der Suchpfad wird zwischen Instanzen von einer Sitzung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="27629-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="27629-120">Clients und Anbieter müssen nicht Aufrufen der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um die Suche Pfad Änderungen dauerhaft entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="27629-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="27629-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27629-121">See also</span></span>



[<span data-ttu-id="27629-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="27629-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="27629-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="27629-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="27629-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="27629-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="27629-125">PidTagContainerFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="27629-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="27629-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="27629-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

