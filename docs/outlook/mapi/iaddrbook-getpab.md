---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3d67d71effde87711e3be9aca1b979627acda37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792012"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="700ad-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="700ad-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="700ad-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="700ad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="700ad-105">Gibt die Eintrags-ID des Containers, die als das persönliche Adressbuch (PAB) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="700ad-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="700ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="700ad-106">Parameters</span></span>

 <span data-ttu-id="700ad-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="700ad-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="700ad-108">[out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="700ad-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="700ad-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="700ad-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="700ad-110">[out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID des PAB.</span><span class="sxs-lookup"><span data-stu-id="700ad-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="700ad-111">Der Parameter _LppEntryID_ enthält 0 (null), wenn kein Container als PAB festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="700ad-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="700ad-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="700ad-112">Return value</span></span>

<span data-ttu-id="700ad-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="700ad-113">S_OK</span></span> 
  
> <span data-ttu-id="700ad-114">Die Eintrags-ID des PAB wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="700ad-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="700ad-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="700ad-115">Remarks</span></span>

<span data-ttu-id="700ad-116">Clients rufen Sie die **GetPAB** -Methode, um die Eintrags-ID des Containers als PAB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="700ad-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="700ad-117">Wenn ein PAB nicht im Profil eingerichtet wurde, wählt MAPI als PAB den ersten Container in der Adressbuchhierarchie, die Änderungen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="700ad-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="700ad-118">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="700ad-118">MFCMAPI reference</span></span>

<span data-ttu-id="700ad-119">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="700ad-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="700ad-120">**Datei**</span><span class="sxs-lookup"><span data-stu-id="700ad-120">**File**</span></span>|<span data-ttu-id="700ad-121">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="700ad-121">**Function**</span></span>|<span data-ttu-id="700ad-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="700ad-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="700ad-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="700ad-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="700ad-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="700ad-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="700ad-125">MFCMAPI (engl.) wird die **GetPAB** -Methode verwendet, um die ID für das persönliche Adressbuch des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="700ad-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="700ad-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="700ad-126">See also</span></span>



[<span data-ttu-id="700ad-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="700ad-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="700ad-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="700ad-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="700ad-129">PidTagContainerFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="700ad-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="700ad-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="700ad-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="700ad-131">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="700ad-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

