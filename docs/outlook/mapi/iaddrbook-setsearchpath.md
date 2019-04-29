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
ms.openlocfilehash: 8611249207811446ae47f056486ec498bf1e7eab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426205"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="6940c-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="6940c-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="6940c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6940c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6940c-105">Legt einen neuen Suchpfad im Profil fest, der für den Prozess der Namensauflösung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6940c-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="6940c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6940c-106">Parameters</span></span>

 <span data-ttu-id="6940c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6940c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6940c-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="6940c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6940c-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="6940c-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="6940c-110">in Ein Zeiger auf die [SRowSet](srowset.md) -Struktur, die zum Speichern des Suchpfads verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6940c-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="6940c-111">Die erste Eigenschaft für jedes **aRow** -Element in **SRowSet** muss **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) sein.</span><span class="sxs-lookup"><span data-stu-id="6940c-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6940c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6940c-112">Return value</span></span>

<span data-ttu-id="6940c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="6940c-113">S_OK</span></span> 
  
> <span data-ttu-id="6940c-114">Der Suchpfad wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6940c-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="6940c-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="6940c-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="6940c-116">Einer der in der **SRowSet** -Struktur beschriebenen Container enthielt nicht die zugehörige **PR_ENTRYID** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6940c-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6940c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6940c-117">Remarks</span></span>

<span data-ttu-id="6940c-118">Clients und Dienstanbieter rufen die **SetSearchPath** -Methode auf, um Änderungen an der Container Suchreihenfolge zu speichern, die zum Auflösen von Namen mithilfe der [IAddrBook::](iaddrbook-resolvename.md) ResolveName-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6940c-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="6940c-119">Der Suchpfad wird zwischen den Instanzen einer Sitzung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6940c-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="6940c-120">Clients und Anbieter müssen nicht die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode aufrufen, um den Suchpfad dauerhaft zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6940c-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6940c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6940c-121">See also</span></span>



[<span data-ttu-id="6940c-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="6940c-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="6940c-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="6940c-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="6940c-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="6940c-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="6940c-125">Kanonische Pidtagcontainerflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6940c-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="6940c-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6940c-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

