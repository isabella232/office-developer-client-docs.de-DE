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
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="0dccd-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="0dccd-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="0dccd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dccd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dccd-105">Legt einen neuen Suchpfad im Profil fest, der für den Namensauflösungsprozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0dccd-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="0dccd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dccd-106">Parameters</span></span>

 <span data-ttu-id="0dccd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0dccd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0dccd-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="0dccd-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0dccd-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="0dccd-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="0dccd-110">[in] Ein Zeiger auf die [SRowSet-Struktur,](srowset.md) die zum Halten des Suchpfads verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0dccd-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="0dccd-111">Die erste Eigenschaft für jedes **aRow-Element** in **SRowSet** muss **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) sein.</span><span class="sxs-lookup"><span data-stu-id="0dccd-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0dccd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0dccd-112">Return value</span></span>

<span data-ttu-id="0dccd-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="0dccd-113">S_OK</span></span> 
  
> <span data-ttu-id="0dccd-114">Der Suchpfad wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0dccd-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="0dccd-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="0dccd-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="0dccd-116">Einer der in der **SRowSet-Struktur** beschriebenen Container hat seine PR_ENTRYID **enthalten.**</span><span class="sxs-lookup"><span data-stu-id="0dccd-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0dccd-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0dccd-117">Remarks</span></span>

<span data-ttu-id="0dccd-118">Clients und Dienstanbieter rufen die **SetSearchPath-Methode** auf, um Änderungen an der Containersuchreihenfolge zu speichern, die zum Auflösen von Namen mit der [IAddrBook::ResolveName-Methode](iaddrbook-resolvename.md) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0dccd-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="0dccd-119">Der Suchpfad wird zwischen Instanzen einer Sitzung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0dccd-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="0dccd-120">Clients und Anbieter müssen die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) nicht aufrufen, um die Änderungen des Suchpfads dauerhaft vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="0dccd-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0dccd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dccd-121">See also</span></span>



[<span data-ttu-id="0dccd-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="0dccd-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="0dccd-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="0dccd-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="0dccd-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="0dccd-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="0dccd-125">PidTagContainerFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0dccd-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="0dccd-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0dccd-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

