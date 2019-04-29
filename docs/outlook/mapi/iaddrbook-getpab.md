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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419898"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="534aa-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="534aa-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="534aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="534aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="534aa-105">Gibt den Eintragsbezeichner des Containers zurück, der als persönliches Adressbuch (PAB) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="534aa-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="534aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="534aa-106">Parameters</span></span>

 <span data-ttu-id="534aa-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="534aa-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="534aa-108">Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="534aa-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="534aa-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="534aa-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="534aa-110">Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID des PAB.</span><span class="sxs-lookup"><span data-stu-id="534aa-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="534aa-111">Der Parameter _lppEntryID_ enthält 0 (null), wenn kein Container als PAB festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="534aa-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="534aa-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="534aa-112">Return value</span></span>

<span data-ttu-id="534aa-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="534aa-113">S_OK</span></span> 
  
> <span data-ttu-id="534aa-114">Die Eintrags-ID des PAB wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="534aa-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="534aa-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="534aa-115">Remarks</span></span>

<span data-ttu-id="534aa-116">Clients rufen die **GetPAB** -Methode auf, um den Eintragsbezeichner des Containers abzurufen, der als PAB festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="534aa-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="534aa-117">Wenn kein PAB im Profil eingerichtet wurde, wählt MAPI als PAB den ersten Container in der Adressbuchhierarchie aus, der Änderungen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="534aa-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="534aa-118">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="534aa-118">MFCMAPI reference</span></span>

<span data-ttu-id="534aa-119">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="534aa-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="534aa-120">**Datei**</span><span class="sxs-lookup"><span data-stu-id="534aa-120">**File**</span></span>|<span data-ttu-id="534aa-121">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="534aa-121">**Function**</span></span>|<span data-ttu-id="534aa-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="534aa-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="534aa-123">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="534aa-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="534aa-124">CMainDlg:: OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="534aa-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="534aa-125">MFCMAPI verwendet die **GetPAB** -Methode, um die ID des persönlichen Adressbuchs des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="534aa-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="534aa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="534aa-126">See also</span></span>



[<span data-ttu-id="534aa-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="534aa-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="534aa-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="534aa-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="534aa-129">Kanonische Pidtagcontainerflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="534aa-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="534aa-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="534aa-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="534aa-131">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="534aa-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

