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
# <a name="ipstxemulatespooler"></a><span data-ttu-id="9e668-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="9e668-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="9e668-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e668-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e668-105">Legt einen lokalen Speicher für die Emulation des Outlook-Protokoll-Managers zum Spoolen ausgehender Nachrichten an einen Server fest.</span><span class="sxs-lookup"><span data-stu-id="9e668-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="9e668-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="9e668-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="9e668-107">in Legen Sie diesen Parameter auf true fest, wenn der lokale Speicher den Spooler emulieren soll; Legen Sie ihn auf false fest, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="9e668-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9e668-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e668-108">Remarks</span></span>

<span data-ttu-id="9e668-109">Ein lokaler Speicher ruft **IPSTX:: EmulateSpooler** auf, um als Outlook-Protokoll-Manager zu fungieren und Nachrichten in der ausgehenden Warteschlange auf dem Back-End-Server (beispielsweise MSN Server oder AOL Server) zur Verarbeitung zu spoolen.</span><span class="sxs-lookup"><span data-stu-id="9e668-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="9e668-110">Emulieren eines Spoolers während der Synchronisierung ruft der Speicher die folgenden beiden Methoden auf:</span><span class="sxs-lookup"><span data-stu-id="9e668-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="9e668-111">**[IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** zum Abrufen der ausgehenden Warteschlange von Nachrichten im Speicher.</span><span class="sxs-lookup"><span data-stu-id="9e668-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="9e668-112">Diese Methode ist nur erfolgreich, wenn der Speicher den Outlook-Protokoll-Manager emuliert.</span><span class="sxs-lookup"><span data-stu-id="9e668-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="9e668-113">**[IMsgStore:: SetLockState](imsgstore-setlockstate.md)** , um den alleinigen Zugriff auf eine Nachricht in der ausgehenden Warteschlange zu sichern, bevor Sie an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e668-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="9e668-114">Diese Methode ist nur erfolgreich, wenn der Speicher den Outlook-Protokoll-Manager emuliert.</span><span class="sxs-lookup"><span data-stu-id="9e668-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="9e668-115">Nach dem Senden der Nachricht ruft der Informationsspeicher diese Methode erneut auf, um den alleinigen Zugriff darauf zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="9e668-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="9e668-116">Seit Outlook 2002 hat der Outlook-Protokoll-Manager den MAPI-Spooler ersetzt und ist für das Spoolen ausgehender Nachrichten an Back-End-Server verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="9e668-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e668-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e668-117">See also</span></span>



[<span data-ttu-id="9e668-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9e668-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="9e668-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="9e668-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

