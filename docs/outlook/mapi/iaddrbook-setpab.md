---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3f13a4d278b85ffae33e8f44f3a15eb499fb11b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792023"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="ad247-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="ad247-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="ad247-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad247-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad247-105">Legt einen bestimmten Container als das persönliche Adressbuch (PAB) fest.</span><span class="sxs-lookup"><span data-stu-id="ad247-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="ad247-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad247-106">Parameters</span></span>

 <span data-ttu-id="ad247-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ad247-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ad247-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="ad247-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ad247-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ad247-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ad247-110">[in] Ein Zeiger auf die Eintrags-ID des Containers, als die PAB festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ad247-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="ad247-111">Der Parameter _LpEntryID_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ad247-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ad247-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ad247-112">Return value</span></span>

<span data-ttu-id="ad247-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad247-113">S_OK</span></span> 
  
> <span data-ttu-id="ad247-114">Der angegebene Container wurde als PAB eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="ad247-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad247-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad247-115">Remarks</span></span>

<span data-ttu-id="ad247-116">Clients und Dienstanbieter rufen Sie die **SetPAB** -Methode, um einen bestimmten Container als PAB festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ad247-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="ad247-117">Die PAB ist ein Container, der Einträge aus anderen Containern sowie neue Einträge kopiert besteht.</span><span class="sxs-lookup"><span data-stu-id="ad247-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="ad247-118">Ein Aufruf von **SetPAB** stellt einen Container als PAB her, bis Containers ist nicht verfügbar gemacht, oder ein neuer Container die PAB durch einen nachfolgenden Aufruf von **SetPAB wird**.</span><span class="sxs-lookup"><span data-stu-id="ad247-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="ad247-119">Clients und Anbieter müssen nicht Aufrufen der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, damit die Änderung PAB dauerhaft entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ad247-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ad247-120">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="ad247-120">MFCMAPI reference</span></span>

<span data-ttu-id="ad247-121">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ad247-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ad247-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ad247-122">**File**</span></span>|<span data-ttu-id="ad247-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ad247-123">**Function**</span></span>|<span data-ttu-id="ad247-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ad247-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ad247-125">AbContDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ad247-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="ad247-126">CAbContDlg::OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="ad247-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="ad247-127">MFCMAPI (engl.) verwendet die **SetPAB** -Methode, um dem angegebenen Container PAB stellen.</span><span class="sxs-lookup"><span data-stu-id="ad247-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad247-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad247-128">See also</span></span>



[<span data-ttu-id="ad247-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="ad247-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="ad247-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="ad247-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="ad247-131">Kanonische PidTagContainerFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ad247-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="ad247-132">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ad247-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="ad247-133">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ad247-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
