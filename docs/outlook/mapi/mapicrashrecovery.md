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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407214"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="b07a0-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="b07a0-103">MAPICrashRecovery</span></span>

<span data-ttu-id="b07a0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b07a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b07a0-105">Die **MAPICrashRecovery-Funktion** überprüft den Status des freigegebenen Speichers für persönliche Ordner (PST) oder Offlineordnerdatei (OST).</span><span class="sxs-lookup"><span data-stu-id="b07a0-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="b07a0-106">Wenn sich der Arbeitsspeicher in einem konsistenten Zustand befindet, verschiebt die **MAPICrashRecovery-Funktion** die Daten auf den Datenträger und verhindert weiteren Lese- oder Schreibzugriff, bis der Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b07a0-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b07a0-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b07a0-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b07a0-108">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="b07a0-108">Exported by:</span></span>  <br/> |<span data-ttu-id="b07a0-109">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="b07a0-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="b07a0-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b07a0-110">Called by:</span></span>  <br/> |<span data-ttu-id="b07a0-111">Client</span><span class="sxs-lookup"><span data-stu-id="b07a0-111">Client</span></span>  <br/> |
|<span data-ttu-id="b07a0-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b07a0-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="b07a0-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="b07a0-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="b07a0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b07a0-114">Parameters</span></span>

<span data-ttu-id="b07a0-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b07a0-115">_ulFlags_</span></span>
  
> <span data-ttu-id="b07a0-116">[in] Kennzeichen, die zum Steuern der Wiederherstellung der MAPI-Absturzwiederherstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b07a0-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="b07a0-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b07a0-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="b07a0-118">**MAPICRASH \_ RECOVER**: Wenn sich die PSTs oder OSTs in einem konsistenten Zustand befinden, verschieben Sie die Daten auf den Datenträger, und sperren Sie die PSTs oder OSTs, um den Lese- oder Schreibzugriff zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="b07a0-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="b07a0-119">**MAPICRASH \_ CONTINUE**: Entsperren der PSTs oder OSTs zum Debuggen.</span><span class="sxs-lookup"><span data-stu-id="b07a0-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="b07a0-120">Rufen Sie nach einem erfolgreichen Aufruf von **MAPICrashRecovery** mit dem **flag MAPICRASH_RECOVER** **MAPICrashRecovery** mit dem **MAPICRASH \_ CONTINUE-Flag** auf, um das Debuggen weiter zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b07a0-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="b07a0-121">**MAPICRASH \_ SYSTEM_SHUTDOWN**: Wenn sich psTs oder OSTs in einem konsistenten Zustand befinden, verschieben Sie die Daten auf den Datenträger, und sperren Sie die PSTs oder OSTs, um den Lese- oder Schreibzugriff zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="b07a0-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="b07a0-122">Die PSTs oder OSTs können nicht mit **MAPICRASH CONTINUE entsperrt \_ werden.**</span><span class="sxs-lookup"><span data-stu-id="b07a0-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="b07a0-123">Muss in Kombination mit **MAPICRASH \_ RECOVER verwendet werden.**</span><span class="sxs-lookup"><span data-stu-id="b07a0-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b07a0-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b07a0-124">Remarks</span></span>

<span data-ttu-id="b07a0-125">Das obere Byte (0xFF000000) ist für anbieterspezifische Absturzwiederherstellungsflags reserviert.</span><span class="sxs-lookup"><span data-stu-id="b07a0-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="b07a0-126">Rufen **Sie MAPICrashRecovery** mit der **MAPICRASH \_ RECOVER** auf, **und MAPICRASH_SYSTEM_SHUTDOWN** als Antwort auf die WM_ENDSESSION werden. </span><span class="sxs-lookup"><span data-stu-id="b07a0-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b07a0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b07a0-127">See also</span></span>

- [<span data-ttu-id="b07a0-128">Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="b07a0-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="b07a0-129">Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="b07a0-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

