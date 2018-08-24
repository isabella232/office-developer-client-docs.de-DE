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
ms.openlocfilehash: 079b54757cfcd5c9b38365abc5a6d901e2b06724
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580719"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="c8e08-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="c8e08-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="c8e08-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8e08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8e08-105">Outlook-Protokoll-Manager, um ausgehende Nachrichten an einen Server Spoolen emulieren ein lokales Speichers festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c8e08-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="c8e08-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="c8e08-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="c8e08-107">[in] Legen Sie diesen Parameter auf true fest, wenn der lokale Speicher die Warteschlange emulieren soll; Legen Sie ihn auf False, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="c8e08-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c8e08-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8e08-108">Remarks</span></span>

<span data-ttu-id="c8e08-109">Ein lokales Speichers **IPSTX::EmulateSpooler** fungieren als ein Outlook Protokollmanager, Einreihen in die Warteschlange Nachrichten in der ausgehenden Warteschlange auf dem Back-End-Server (beispielsweise MSN-Server oder AOL-Server) für die Verarbeitung von Anrufen.</span><span class="sxs-lookup"><span data-stu-id="c8e08-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="c8e08-110">Emulieren einer Warteschlange während der Synchronisation, ruft der Speicher dann diese beiden Methoden:</span><span class="sxs-lookup"><span data-stu-id="c8e08-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="c8e08-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** zum Abrufen der ausgehenden Warteschlange von Nachrichten in den Speicher.</span><span class="sxs-lookup"><span data-stu-id="c8e08-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="c8e08-112">Diese Methode ist nur dann, wenn der Informationsspeicher die Outlook-Protokollmanager emulieren ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c8e08-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="c8e08-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** zum Sichern der alleinigen Zugriff auf eine Nachricht in der ausgehenden Warteschlange einfach, bevor sie an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8e08-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="c8e08-114">Diese Methode ist nur dann, wenn der Informationsspeicher die Outlook-Protokollmanager emulieren ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c8e08-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="c8e08-115">Nach dem Senden der Nachricht, ruft der Speicher diese Methode erneut aus, um die alleinige Zugriff darauf freigeben.</span><span class="sxs-lookup"><span data-stu-id="c8e08-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="c8e08-116">Seit Outlook 2002 die Outlook-Protokollmanager ersetzt die MAPI-Warteschlange und aus dem Back-End-Server für ausgehende Nachrichten in Warteschlange zuständig.</span><span class="sxs-lookup"><span data-stu-id="c8e08-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c8e08-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8e08-117">See also</span></span>



[<span data-ttu-id="c8e08-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c8e08-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="c8e08-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="c8e08-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

