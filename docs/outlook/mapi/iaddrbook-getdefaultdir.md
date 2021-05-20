---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436874"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="799ad-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="799ad-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="799ad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="799ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="799ad-105">Gibt den Eintragsbezeichner für den anfänglichen Adressbuchcontainer zurück.</span><span class="sxs-lookup"><span data-stu-id="799ad-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="799ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="799ad-106">Parameters</span></span>

 <span data-ttu-id="799ad-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="799ad-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="799ad-108">[out] Ein Zeiger auf die Byteanzahl in der Eintrags-ID, auf die der  _lppEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="799ad-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="799ad-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="799ad-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="799ad-110">[out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID des Standardcontainers.</span><span class="sxs-lookup"><span data-stu-id="799ad-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="799ad-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="799ad-111">Return value</span></span>

<span data-ttu-id="799ad-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="799ad-112">S_OK</span></span> 
  
> <span data-ttu-id="799ad-113">Der Eintragsbezeichner des Standardcontainers wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="799ad-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="799ad-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="799ad-114">Remarks</span></span>

<span data-ttu-id="799ad-115">Clientanwendungen und Dienstanbieter rufen die **GetDefaultDir-Methode** auf, um die Eintrags-ID des Standard-Adressbuchcontainers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="799ad-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="799ad-116">Der Standardcontainer wird dem Benutzer angezeigt, der beim ersten Öffnen des Adressbuchs im Adressbuch angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="799ad-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="799ad-117">Wenn ein Standardcontainer nicht durch einen Aufruf der [IAddrBook::SetDefaultDir-Methode](iaddrbook-setdefaultdir.md) festgelegt wurde, weist MAPI als Standardcontainer den ersten Container mit Namen zu, bei dem es sich nicht um das persönliche Adressbuch (PAB) handelt.</span><span class="sxs-lookup"><span data-stu-id="799ad-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="799ad-118">Wenn ein solcher Container nicht gefunden werden kann, wird das PAB zum Standardcontainer.</span><span class="sxs-lookup"><span data-stu-id="799ad-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="799ad-119">Zum Festlegen des Standardverzeichnisses ruft ein Client oder Anbieter die **SetDefaultDir-Methode** auf.</span><span class="sxs-lookup"><span data-stu-id="799ad-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="799ad-120">Clients und Anbieter müssen die [IMAPIProp::SaveChanges-Methode nicht](imapiprop-savechanges.md) aufrufen. Da Änderungen am Adressbuch nicht vorgenommen werden, werden Änderungen sofort dauerhaft vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="799ad-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="799ad-121">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="799ad-121">MFCMAPI reference</span></span>

<span data-ttu-id="799ad-122">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="799ad-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="799ad-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="799ad-123">**File**</span></span>|<span data-ttu-id="799ad-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="799ad-124">**Function**</span></span>|<span data-ttu-id="799ad-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="799ad-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="799ad-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="799ad-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="799ad-127">CMainDlg::OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="799ad-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="799ad-128">MFCMAPI verwendet die **GetDefaultDir-Methode,** um die ID für den Standard-Adressbuchcontainer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="799ad-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="799ad-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="799ad-129">See also</span></span>



[<span data-ttu-id="799ad-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="799ad-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="799ad-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="799ad-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="799ad-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="799ad-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="799ad-133">PidTagContainerFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="799ad-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="799ad-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="799ad-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="799ad-135">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="799ad-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

