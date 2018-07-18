---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c856dfd1d419fd7a4bf4f47852ffb69470f9281b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795690"
---
# <a name="sync"></a><span data-ttu-id="79845-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="79845-103">SYNC</span></span>

  
  
<span data-ttu-id="79845-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79845-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79845-105">Informationen für die Synchronisierung zwischen einer lokalen Speicher und einem Server gestartet.</span><span class="sxs-lookup"><span data-stu-id="79845-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="79845-106">Diese Informationen werden während der [Synchronisieren Zustand](synchronize-state.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="79845-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="79845-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="79845-107">Quick info</span></span>

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a><span data-ttu-id="79845-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="79845-108">Members</span></span>

 <span data-ttu-id="79845-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="79845-109">_ulFlags_</span></span>
  
- <span data-ttu-id="79845-110">[Out] / [in] eine Bitmaske der folgenden Werte, die das Verhalten während der Synchronisation ändert:</span><span class="sxs-lookup"><span data-stu-id="79845-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="79845-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="79845-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="79845-112">[in] Der Client wird nur Upload ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="79845-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="79845-113">Outlook gibt nur lokal geänderten Ordner zurück.</span><span class="sxs-lookup"><span data-stu-id="79845-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="79845-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="79845-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="79845-115">[in] Der Client wird nur Download ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="79845-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="79845-116">Outlook sollte nicht hochladen Bits für Ordner deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="79845-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="79845-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="79845-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="79845-118">[in] Der Client wird eine angegebene Gruppe von Ordnern mit der angegebenen Eintrags-IDs synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="79845-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="79845-119">Dieses Kennzeichen können mit der **UPS_UPLOAD_ONLY** oder eine **UPS_DNLOAD_ONLY** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="79845-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="79845-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="79845-120">UPS_OK</span></span>
    
  - <span data-ttu-id="79845-121">[out] Synchronisierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="79845-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="79845-122">Der Client legt dies fest, nach dem Hochladen, oder eine vollständige Synchronisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="79845-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="79845-123">Obwohl der Client kann entweder hochladen oder vollständig synchronisieren (hochladen und herunterladen) Ordner und Elemente mit der API Replikation der Client gibt *UlFlags* mit nur einer Richtung der Replikation zu einem Zeitpunkt – die **UPS_UPLOAD_ONLY** oder **UPS_DNLOAD_ONLY** -Flag.</span><span class="sxs-lookup"><span data-stu-id="79845-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="79845-124">Im Fall von eine vollständige Synchronisierung führt der Client zunächst Upload mit dem **UPS_UPLOAD_ONLY** -Flag, und klicken Sie dann einen Download mit dem **UPS_DNLOAD_ONLY** -Flag.</span><span class="sxs-lookup"><span data-stu-id="79845-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="79845-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="79845-125">_pwzPath_</span></span>
  
- <span data-ttu-id="79845-126">[out] Pfad zu dem lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="79845-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="79845-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="79845-127">_Reserved1_</span></span>
  
- <span data-ttu-id="79845-128">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79845-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="79845-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="79845-129">_Reserved2_</span></span>
  
- <span data-ttu-id="79845-130">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79845-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="79845-131">*PEL*</span><span class="sxs-lookup"><span data-stu-id="79845-131">*pel*</span></span> 
  
- <span data-ttu-id="79845-132">[in] Dies ist die Liste von Eintrags-IDs der Ordner synchronisieren, wenn **UPS_THESE_FOLDERS** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="79845-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="79845-133">Finden Sie unter mapidefs.h für die Definition des **LPENTRYLIST**Typs.</span><span class="sxs-lookup"><span data-stu-id="79845-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="79845-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="79845-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="79845-135">[in] Dies ist ein Array von Ordneroptionen für entsprechende Ordner im *Pel* , wenn **UPS_THESE_FOLDERS** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="79845-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="79845-136">Diese Ordneroptionen werden verwendet, wenn die während der [Ordner Zustand hochladen](upload-folder-state.md)in *Pel* aufgeführten Ordner hochladen.</span><span class="sxs-lookup"><span data-stu-id="79845-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="79845-137">Weitere Informationen zu Ordneroptionen finden Sie unter **[UPFLD](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="79845-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="79845-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79845-138">See also</span></span>



[<span data-ttu-id="79845-139">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="79845-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="79845-140">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="79845-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="79845-141">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="79845-141">MAPI Constants</span></span>](mapi-constants.md)

