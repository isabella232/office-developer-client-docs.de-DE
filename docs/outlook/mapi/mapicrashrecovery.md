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
ms.openlocfilehash: 22f17df9347b4744dfe6598e7007469ffb9e5251
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793143"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="6aef8-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="6aef8-103">MAPICrashRecovery</span></span>

<span data-ttu-id="6aef8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6aef8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6aef8-105">Die Funktion **MAPICrashRecovery** überprüft, ob der Zustand des Persönliche Ordner-Datei (PST) oder Offlineordnerdatei (OST) Arbeitsspeicher freigegeben.</span><span class="sxs-lookup"><span data-stu-id="6aef8-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="6aef8-106">Wenn der Arbeitsspeicher in einen konsistenten Status befindet, wird die **MAPICrashRecovery** -Funktion verschiebt die Daten auf dem Datenträger und verhindert, dass weitere Lese- oder Schreibzugriff, bis der Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="6aef8-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="6aef8-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="6aef8-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6aef8-108">Vom exportiert werden:</span><span class="sxs-lookup"><span data-stu-id="6aef8-108">Exported by:</span></span>  <br/> |<span data-ttu-id="6aef8-109">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="6aef8-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="6aef8-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6aef8-110">Called by:</span></span>  <br/> |<span data-ttu-id="6aef8-111">Client</span><span class="sxs-lookup"><span data-stu-id="6aef8-111">Client</span></span>  <br/> |
|<span data-ttu-id="6aef8-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6aef8-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="6aef8-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="6aef8-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="6aef8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6aef8-114">Parameters</span></span>

<span data-ttu-id="6aef8-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6aef8-115">_ulFlags_</span></span>
  
> <span data-ttu-id="6aef8-116">[in] Kennzeichen, die steuern, wie die MAPI-Wiederherstellung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6aef8-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="6aef8-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6aef8-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="6aef8-118">**MAPICRASH\_wiederherstellen**: Wenn die PST-Dateien oder OSTs in einen konsistenten Status befinden, verschieben Sie die Daten auf dem Datenträger und die PST-Dateien oder OSTs, um zu verhindern, dass Lese- oder Schreibzugriff sperren.</span><span class="sxs-lookup"><span data-stu-id="6aef8-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="6aef8-119">**MAPICRASH\_weiter**: entsperren Sie die PST-Dateien oder OSTs für das debugging.</span><span class="sxs-lookup"><span data-stu-id="6aef8-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="6aef8-120">Rufen Sie nach einem erfolgreichen Aufruf von **MAPICrashRecovery** mit dem **MAPICRASH_RECOVER** -Flag, **MAPICrashRecovery** mit der **MAPICRASH\_weiter** Kennzeichnung, damit das Debuggen, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="6aef8-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="6aef8-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: Wenn die PST-Dateien oder OSTs in einen konsistenten Status befinden, verschieben Sie die Daten auf dem Datenträger und die PST-Dateien oder OSTs, um zu verhindern, dass Lese- oder Schreibzugriff sperren.</span><span class="sxs-lookup"><span data-stu-id="6aef8-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="6aef8-122">Die PST-Dateien oder OSTs kann nicht entsperrt mit werden **MAPICRASH\_weiter**.</span><span class="sxs-lookup"><span data-stu-id="6aef8-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="6aef8-123">Muss verwendet werden, in Kombination mit **MAPICRASH\_wiederherstellen**.</span><span class="sxs-lookup"><span data-stu-id="6aef8-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6aef8-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6aef8-124">Remarks</span></span>

<span data-ttu-id="6aef8-125">Das obere Byte (0xFF000000) ist für Anbieter für bestimmte Absturz Recovery Flags reserviert.</span><span class="sxs-lookup"><span data-stu-id="6aef8-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="6aef8-126">Rufen Sie **MAPICrashRecovery** mit der **MAPICRASH\_wiederherstellen** und **MAPICRASH_SYSTEM_SHUTDOWN** Flags als Antwort auf die Nachricht **WM_ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="6aef8-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6aef8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6aef8-127">See also</span></span>

- [<span data-ttu-id="6aef8-128">Über die Wiederherstellung von MAPI-API</span><span class="sxs-lookup"><span data-stu-id="6aef8-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="6aef8-129">Verwenden Sie die Wiederherstellung von MAPI-API</span><span class="sxs-lookup"><span data-stu-id="6aef8-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

