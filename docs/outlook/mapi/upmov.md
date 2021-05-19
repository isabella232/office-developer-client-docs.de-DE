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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339186"
---
# <a name="upmov"></a><span data-ttu-id="ecb11-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="ecb11-103">UPMOV</span></span>
 
<span data-ttu-id="ecb11-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecb11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecb11-105">Informationen zum Hochladen von verschobenen Elementen.</span><span class="sxs-lookup"><span data-stu-id="ecb11-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="ecb11-106">Diese Informationen werden während des Statusstatus ["Upload delete" und](upload-delete-status-state.md) ["upload table" verwendet.](upload-table-state.md)</span><span class="sxs-lookup"><span data-stu-id="ecb11-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ecb11-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ecb11-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="ecb11-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="ecb11-108">Members</span></span>

<span data-ttu-id="ecb11-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ecb11-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ecb11-110">[in] Flags, um das entsprechende Verhalten während des Uploads zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="ecb11-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="ecb11-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="ecb11-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="ecb11-112">[in] Problem beim Öffnen des Serverordners.</span><span class="sxs-lookup"><span data-stu-id="ecb11-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="ecb11-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="ecb11-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="ecb11-114">[in] Der Uploadstatus hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="ecb11-114">[in] The upload state has changed.</span></span> <span data-ttu-id="ecb11-115">Dies wird vom Client verwendet, um die Statusänderung für den lokalen Speicher nachverfolgt zu werden.</span><span class="sxs-lookup"><span data-stu-id="ecb11-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="ecb11-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="ecb11-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="ecb11-117">[in] Commituploadstatus.</span><span class="sxs-lookup"><span data-stu-id="ecb11-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="ecb11-118">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="ecb11-118">_pReserved_</span></span>
  
>  <span data-ttu-id="ecb11-119">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ecb11-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="ecb11-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="ecb11-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="ecb11-121">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ecb11-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="ecb11-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="ecb11-122">_pszName_</span></span>
  
>  <span data-ttu-id="ecb11-123">[out] Name des Zielordners.</span><span class="sxs-lookup"><span data-stu-id="ecb11-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="ecb11-124">Dieses Mitglied unterstützt UNICODE nicht.</span><span class="sxs-lookup"><span data-stu-id="ecb11-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="ecb11-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="ecb11-125">_feid_</span></span>
  
>  <span data-ttu-id="ecb11-126">[out] Eintrags-ID des Zielordners.</span><span class="sxs-lookup"><span data-stu-id="ecb11-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="ecb11-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="ecb11-127">_pfld_</span></span>
  
>  <span data-ttu-id="ecb11-128">[in] Zeiger auf Serverordner.</span><span class="sxs-lookup"><span data-stu-id="ecb11-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="ecb11-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="ecb11-129">_pxicc_</span></span>
  
>  <span data-ttu-id="ecb11-130">[in] Zeiger auf die **IExchangeImportContentsChanges-Inhaltsschnittstelle,** die das Hochladen von Inhaltsänderungen bei Verwendung der inkrementellen Änderungssynchronisierung (Incremental Change Synchronization, ICS) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ecb11-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="ecb11-131">Weitere Informationen zu **IExchangeImportContentsChanges** und ICS finden Sie unter [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ecb11-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="ecb11-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="ecb11-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="ecb11-133">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ecb11-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="ecb11-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="ecb11-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="ecb11-135">[out] Nächster Verschiebekontext.</span><span class="sxs-lookup"><span data-stu-id="ecb11-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="ecb11-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="ecb11-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="ecb11-137">[in] Die Anzahl der hier verschobenen Elemente.</span><span class="sxs-lookup"><span data-stu-id="ecb11-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ecb11-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecb11-138">See also</span></span>

- [<span data-ttu-id="ecb11-139">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="ecb11-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="ecb11-140">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="ecb11-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="ecb11-141">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ecb11-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="ecb11-142">FEID</span><span class="sxs-lookup"><span data-stu-id="ecb11-142">FEID</span></span>](feid.md)

