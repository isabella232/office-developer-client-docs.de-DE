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
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287014"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="579b5-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="579b5-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="579b5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="579b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="579b5-105">Legt einen bestimmten Container als persönliches Adressbuch (PAB) fest.</span><span class="sxs-lookup"><span data-stu-id="579b5-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="579b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="579b5-106">Parameters</span></span>

 <span data-ttu-id="579b5-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="579b5-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="579b5-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="579b5-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="579b5-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="579b5-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="579b5-110">in Ein Zeiger auf die Eintrags-ID des Containers, der als PAB festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="579b5-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="579b5-111">Der _lpEntryID_ -Parameter darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="579b5-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="579b5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="579b5-112">Return value</span></span>

<span data-ttu-id="579b5-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="579b5-113">S_OK</span></span> 
  
> <span data-ttu-id="579b5-114">Der angegebene Container wurde als PAB eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="579b5-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="579b5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="579b5-115">Remarks</span></span>

<span data-ttu-id="579b5-116">Clients und Dienstanbieter rufen die **SetPAB** -Methode auf, um einen bestimmten Container als PAB festzulegen.</span><span class="sxs-lookup"><span data-stu-id="579b5-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="579b5-117">Das PAB ist ein Container, der aus Einträgen aus anderen Containern sowie neuen Einträgen besteht.</span><span class="sxs-lookup"><span data-stu-id="579b5-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="579b5-118">Ein Aufruf von **SetPAB** richtet einen Container als PAB ein, bis dieser Container nicht verfügbar gemacht wird oder ein neuer Container durch einen nachfolgenden Aufruf von **SetPAB**zum PAB wird.</span><span class="sxs-lookup"><span data-stu-id="579b5-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="579b5-119">Clients und Anbieter müssen nicht die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode aufrufen, um das PAB permanent zu ändern.</span><span class="sxs-lookup"><span data-stu-id="579b5-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="579b5-120">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="579b5-120">MFCMAPI reference</span></span>

<span data-ttu-id="579b5-121">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="579b5-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="579b5-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="579b5-122">**File**</span></span>|<span data-ttu-id="579b5-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="579b5-123">**Function**</span></span>|<span data-ttu-id="579b5-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="579b5-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="579b5-125">AbContDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="579b5-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="579b5-126">CAbContDlg:: OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="579b5-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="579b5-127">MFCMAPI verwendet die **SetPAB** -Methode, um den angegebenen Container als PAB zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="579b5-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="579b5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="579b5-128">See also</span></span>



[<span data-ttu-id="579b5-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="579b5-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="579b5-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="579b5-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="579b5-131">Kanonische Pidtagcontainerflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="579b5-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="579b5-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="579b5-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="579b5-133">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="579b5-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

