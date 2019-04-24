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
# <a name="upmov"></a><span data-ttu-id="4c565-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="4c565-103">UPMOV</span></span>
 
<span data-ttu-id="4c565-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c565-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c565-105">Informationen zum Hochladen von Elementen, die verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="4c565-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="4c565-106">Diese Informationen werden während des Status [](upload-delete-status-state.md) Status des Uploads und zum [Hochladen von Tabellen](upload-table-state.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c565-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4c565-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4c565-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="4c565-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="4c565-108">Members</span></span>

<span data-ttu-id="4c565-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c565-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4c565-110">in Flags zum Bestimmen des geeigneten Verhaltens während des Uploads.</span><span class="sxs-lookup"><span data-stu-id="4c565-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="4c565-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="4c565-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="4c565-112">in Problem beim Öffnen des Serverordners.</span><span class="sxs-lookup"><span data-stu-id="4c565-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="4c565-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="4c565-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="4c565-114">in Der Uploadstatus wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="4c565-114">[in] The upload state has changed.</span></span> <span data-ttu-id="4c565-115">Dies wird vom Client verwendet, um die Zustandsänderung für den lokalen Speicher nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="4c565-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="4c565-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="4c565-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="4c565-117">in Commit-Uploadstatus.</span><span class="sxs-lookup"><span data-stu-id="4c565-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="4c565-118">_Beibehalten_</span><span class="sxs-lookup"><span data-stu-id="4c565-118">_pReserved_</span></span>
  
>  <span data-ttu-id="4c565-119">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c565-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4c565-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="4c565-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="4c565-121">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c565-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4c565-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="4c565-122">_pszName_</span></span>
  
>  <span data-ttu-id="4c565-123">Out Name des Zielordners.</span><span class="sxs-lookup"><span data-stu-id="4c565-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="4c565-124">Dieser Member unterstützt UNICODE nicht.</span><span class="sxs-lookup"><span data-stu-id="4c565-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="4c565-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="4c565-125">_feid_</span></span>
  
>  <span data-ttu-id="4c565-126">Out Eintrags-ID des Zielordners.</span><span class="sxs-lookup"><span data-stu-id="4c565-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="4c565-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="4c565-127">_pfld_</span></span>
  
>  <span data-ttu-id="4c565-128">in Zeiger auf Serverordner.</span><span class="sxs-lookup"><span data-stu-id="4c565-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="4c565-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="4c565-129">_pxicc_</span></span>
  
>  <span data-ttu-id="4c565-130">in Zeiger auf die **IExchangeImportContentsChanges** -Inhalts Oberfläche, die das Hochladen von Inhaltsänderungen unterstützt, wenn die inkrementelle Änderungs Synchronisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c565-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="4c565-131">Weitere Informationen zu **IExchangeImportContentsChanges** und ICS finden Sie unter [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c565-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="4c565-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="4c565-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="4c565-133">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c565-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4c565-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="4c565-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="4c565-135">Out Nächster Verschiebungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="4c565-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="4c565-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="4c565-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="4c565-137">in Die Anzahl der Elemente, die hierhin verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="4c565-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4c565-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c565-138">See also</span></span>

- [<span data-ttu-id="4c565-139">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="4c565-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="4c565-140">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="4c565-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="4c565-141">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4c565-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="4c565-142">FEID</span><span class="sxs-lookup"><span data-stu-id="4c565-142">FEID</span></span>](feid.md)

