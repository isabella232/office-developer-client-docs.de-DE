---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393383"
---
# <a name="upmov"></a><span data-ttu-id="cbb5a-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="cbb5a-103">UPMOV</span></span>
 
<span data-ttu-id="cbb5a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbb5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbb5a-105">Informationen zum Hochladen von Elementen, die verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="cbb5a-106">Diese Informationen werden während der [Upload löschen Status Zustand](upload-delete-status-state.md) und [Status Tabelle hochladen](upload-table-state.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cbb5a-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="cbb5a-107">Quick info</span></span>

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a><span data-ttu-id="cbb5a-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="cbb5a-108">Members</span></span>

<span data-ttu-id="cbb5a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cbb5a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="cbb5a-110">[in] Kennzeichen, die um das entsprechende Verhalten beim Hochladen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="cbb5a-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="cbb5a-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="cbb5a-112">[in] Problem beim Öffnen von Serverordner.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="cbb5a-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="cbb5a-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="cbb5a-114">[in] Der Upload-Status hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-114">[in] The upload state has changed.</span></span> <span data-ttu-id="cbb5a-115">Dies wird vom Client verwendet, um die Änderung im Zustand für den lokalen Speicher zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="cbb5a-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="cbb5a-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="cbb5a-117">[in] Commit Upload Zustand.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="cbb5a-118">_Beibehalten_</span><span class="sxs-lookup"><span data-stu-id="cbb5a-118">_pReserved_</span></span>
  
>  <span data-ttu-id="cbb5a-119">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="cbb5a-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="cbb5a-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="cbb5a-121">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="cbb5a-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="cbb5a-122">_pszName_</span></span>
  
>  <span data-ttu-id="cbb5a-123">[out] Name des Zielordners.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="cbb5a-124">Dieser Member wird UNICODE nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="cbb5a-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="cbb5a-125">_feid_</span></span>
  
>  <span data-ttu-id="cbb5a-126">[out] Eintrags-ID der Zielordner.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="cbb5a-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="cbb5a-127">_pfld_</span></span>
  
>  <span data-ttu-id="cbb5a-128">[in] Zeiger auf den Ordner auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="cbb5a-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="cbb5a-129">_pxicc_</span></span>
  
>  <span data-ttu-id="cbb5a-130">[in] Zeiger auf die Schnittstelle der **IExchangeImportContentsChanges** -Inhalt, die Hochladen von Änderungen bei Verwendung von inkrementelle Änderung Synchronisierung (ICS) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="cbb5a-131">Weitere Informationen zu **IExchangeImportContentsChanges** und ICS finden Sie unter [ICS Bewertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cbb5a-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="cbb5a-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="cbb5a-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="cbb5a-133">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="cbb5a-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="cbb5a-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="cbb5a-135">[out] Als Nächstes Kontext zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="cbb5a-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="cbb5a-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="cbb5a-137">[in] Anzahl der Elemente hier verschoben.</span><span class="sxs-lookup"><span data-stu-id="cbb5a-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="cbb5a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbb5a-138">See also</span></span>

- [<span data-ttu-id="cbb5a-139">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="cbb5a-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="cbb5a-140">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="cbb5a-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="cbb5a-141">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="cbb5a-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="cbb5a-142">FEID</span><span class="sxs-lookup"><span data-stu-id="cbb5a-142">FEID</span></span>](feid.md)

