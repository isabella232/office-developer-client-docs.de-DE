---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357302"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="2579e-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="2579e-103">MAPICrashRecovery</span></span>

<span data-ttu-id="2579e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2579e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2579e-105">Die **MAPICrashRecovery** -Funktion überprüft den Status des freigegebenen Speichers (PST) oder der Offline Ordner Datei (Ost).</span><span class="sxs-lookup"><span data-stu-id="2579e-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="2579e-106">Wenn sich der Speicher in einem konsistenten Zustand befindet, verschiebt die **MAPICrashRecovery** -Funktion die Daten auf den Datenträger und verhindert den weiteren Lese-oder Schreibzugriff, bis der Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="2579e-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2579e-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="2579e-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2579e-108">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="2579e-108">Exported by:</span></span>  <br/> |<span data-ttu-id="2579e-109">olmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="2579e-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="2579e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2579e-110">Called by:</span></span>  <br/> |<span data-ttu-id="2579e-111">Client</span><span class="sxs-lookup"><span data-stu-id="2579e-111">Client</span></span>  <br/> |
|<span data-ttu-id="2579e-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2579e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="2579e-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="2579e-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="2579e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2579e-114">Parameters</span></span>

<span data-ttu-id="2579e-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2579e-115">_ulFlags_</span></span>
  
> <span data-ttu-id="2579e-116">in Flags, die verwendet werden, um zu steuern, wie die MAPI-Crash Wiederherstellung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2579e-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="2579e-117">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="2579e-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="2579e-118">**MAPICRASH\_Recover**: Wenn sich die PST oder Kosten in einem konsistenten Zustand befinden, verschieben Sie die Daten auf den Datenträger, und Sperren Sie die PST oder Kosten, um Lese-oder Schreibzugriff zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="2579e-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="2579e-119">**MAPICRASH\_Continue**: entsperren Sie die PST-oder Kosten für das Debugging.</span><span class="sxs-lookup"><span data-stu-id="2579e-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="2579e-120">Rufen Sie nach einem erfolgreichen Aufruf von **MAPICrashRecovery** mit dem **MAPICRASH_RECOVER** -Flag **MAPICrashRecovery** mit dem Flag **MAPICRASH\_Continue** auf, um das Debuggen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2579e-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="2579e-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: Wenn die PST oder Kosten sich in einem konsistenten Zustand befinden, verschieben Sie die Daten auf den Datenträger, und Sperren Sie die PST oder Kosten, um Lese-oder Schreibzugriff zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="2579e-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="2579e-122">Die PST oder Kosten kann nicht mit **MAPICRASH\_Continue**entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="2579e-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="2579e-123">Muss in Kombination mit **MAPICRASH\_Recover**verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2579e-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2579e-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2579e-124">Remarks</span></span>

<span data-ttu-id="2579e-125">Das obere Byte (0xFF000000) ist für anbieterspezifische Absturz Wiederherstellungs Kennzeichen reserviert.</span><span class="sxs-lookup"><span data-stu-id="2579e-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="2579e-126">Aufrufen von **MAPICrashRecovery** mit **den\_MAPICRASH Recover** -und **MAPICRASH_SYSTEM_SHUTDOWN** -Flags als Reaktion auf die **WM_ENDSESSION** -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2579e-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2579e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2579e-127">See also</span></span>

- [<span data-ttu-id="2579e-128">Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="2579e-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="2579e-129">Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="2579e-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

