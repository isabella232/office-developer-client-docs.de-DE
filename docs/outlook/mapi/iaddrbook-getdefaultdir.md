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
ms.openlocfilehash: 7309f65965fe3c88f927eeba0bbcccff97c479af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792006"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="a96f9-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="a96f9-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="a96f9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a96f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a96f9-105">Gibt die Eintrags-ID für die anfängliche Adressbuchcontainer zurück.</span><span class="sxs-lookup"><span data-stu-id="a96f9-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="a96f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a96f9-106">Parameters</span></span>

 <span data-ttu-id="a96f9-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a96f9-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="a96f9-108">[out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="a96f9-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a96f9-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="a96f9-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="a96f9-110">[out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID der Standardcontainer.</span><span class="sxs-lookup"><span data-stu-id="a96f9-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a96f9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a96f9-111">Return value</span></span>

<span data-ttu-id="a96f9-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a96f9-112">S_OK</span></span> 
  
> <span data-ttu-id="a96f9-113">Die Eintrags-ID der Standardcontainer wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a96f9-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a96f9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a96f9-114">Remarks</span></span>

<span data-ttu-id="a96f9-115">Clientanwendungen und Dienstanbieter rufen Sie die **GetDefaultDir** -Methode, um die Eintrags-ID der Standard-Adressbuchcontainer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a96f9-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="a96f9-116">Der standardmäßige Container ist, was der Benutzer erhält im Adressbuch angezeigt wird, wenn das Adressbuch zum ersten Mal geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a96f9-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="a96f9-117">Wenn ein Standardcontainer nicht durch einen Aufruf an die [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) -Methode festgelegt wurde, weist MAPI als Standardcontainer den ersten Container mit Namen, der nicht das persönliche Adressbuch (PAB) ist.</span><span class="sxs-lookup"><span data-stu-id="a96f9-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="a96f9-118">Wenn ein solcher Container nicht gefunden werden kann, wird die PAB Standardcontainer.</span><span class="sxs-lookup"><span data-stu-id="a96f9-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="a96f9-119">Wenn Sie die Standardeinstellung festlegen Directory, ein Client oder Anbieter die **SetDefaultDir** -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a96f9-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="a96f9-120">Clients und Anbieter müssen nicht die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufrufen. Da Änderungen an dem Adressbuch nicht durchgeführt werden, werden sofort permanent geändert.</span><span class="sxs-lookup"><span data-stu-id="a96f9-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a96f9-121">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="a96f9-121">MFCMAPI reference</span></span>

<span data-ttu-id="a96f9-122">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a96f9-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a96f9-123">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a96f9-123">**File**</span></span>|<span data-ttu-id="a96f9-124">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a96f9-124">**Function**</span></span>|<span data-ttu-id="a96f9-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a96f9-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a96f9-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a96f9-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="a96f9-127">CMainDlg::OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="a96f9-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="a96f9-128">MFCMAPI (engl.) verwendet die **GetDefaultDir** -Methode, um die ID für die Standard-Adressbuchcontainer erhalten.</span><span class="sxs-lookup"><span data-stu-id="a96f9-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a96f9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a96f9-129">See also</span></span>



[<span data-ttu-id="a96f9-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="a96f9-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="a96f9-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a96f9-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="a96f9-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a96f9-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a96f9-133">PidTagContainerFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a96f9-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="a96f9-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a96f9-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="a96f9-135">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a96f9-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

