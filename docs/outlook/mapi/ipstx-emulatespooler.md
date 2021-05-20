---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 024583926b5d0be638b33b1b60c5d4c5dc74d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438953"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="e448c-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="e448c-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="e448c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e448c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e448c-105">Legt einen lokalen Speicher fest, um den Outlook Protokoll-Manager zu emulieren, um ausgehende Nachrichten mit einem Server zu spoolen.</span><span class="sxs-lookup"><span data-stu-id="e448c-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="e448c-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="e448c-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="e448c-107">[in] Legen Sie diesen Parameter auf True, wenn der lokale Speicher den Spooler emulieren soll. legen Sie ihn auf False, falls nicht.</span><span class="sxs-lookup"><span data-stu-id="e448c-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e448c-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e448c-108">Remarks</span></span>

<span data-ttu-id="e448c-109">Ein lokaler Speicher ruft **IPSTX::EmulateSpooler** auf, um als Outlook-Protokoll-Manager zu fungieren und Nachrichten in der ausgehenden Warteschlange zur Verarbeitung an den Back-End-Server (z. B. MSN-Server oder AOL-Server) zu spoolen.</span><span class="sxs-lookup"><span data-stu-id="e448c-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="e448c-110">Beim Emulieren eines Spoolers während der Synchronisierung ruft der Speicher dann die folgenden beiden Methoden auf:</span><span class="sxs-lookup"><span data-stu-id="e448c-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="e448c-111">**[IMsgStore::GetOutgoingQueue,](imsgstore-getoutgoingqueue.md)** um die ausgehende Warteschlange mit Nachrichten im Store zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e448c-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="e448c-112">Diese Methode ist nur erfolgreich, wenn der Speicher den Outlook simuliert.</span><span class="sxs-lookup"><span data-stu-id="e448c-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="e448c-113">**[IMsgStore::SetLockState,](imsgstore-setlockstate.md)** um den alleinigen Zugriff auf eine Nachricht in der ausgehenden Warteschlange zu sichern, kurz bevor sie an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e448c-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="e448c-114">Diese Methode ist nur erfolgreich, wenn der Speicher den Outlook simuliert.</span><span class="sxs-lookup"><span data-stu-id="e448c-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="e448c-115">Nach dem Senden der Nachricht ruft der Store diese Methode erneut auf, um den alleinigen Zugriff darauf frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="e448c-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="e448c-116">Seit Outlook 2002 ersetzte der Outlook-Protokoll-Manager den MAPI-Spooler und wurde für das Spooling ausgehender Nachrichten an Back-End-Server verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="e448c-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e448c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e448c-117">See also</span></span>



[<span data-ttu-id="e448c-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e448c-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="e448c-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="e448c-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

