---
title: Vermeiden bestimmter Methoden beim Start
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580635"
---
# <a name="avoiding-certain-methods-at-startup"></a><span data-ttu-id="07678-103">Vermeiden bestimmter Methoden beim Start</span><span class="sxs-lookup"><span data-stu-id="07678-103">Avoiding Certain Methods at Startup</span></span>

 
  
<span data-ttu-id="07678-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07678-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07678-105">Zum Verbessern der Leistung beim Starten von vermeiden Sie die folgenden Anrufe:</span><span class="sxs-lookup"><span data-stu-id="07678-105">To improve performance at startup time, avoid making the following calls:</span></span>
  
- [<span data-ttu-id="07678-106">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="07678-106">IMAPISession::EnumAdrTypes</span></span>](imapisession-enumadrtypes.md)
    
- [<span data-ttu-id="07678-107">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="07678-107">IMAPISession::GetStatusTable</span></span>](imapisession-getstatustable.md)
    
- [<span data-ttu-id="07678-108">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="07678-108">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
    
- [<span data-ttu-id="07678-109">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="07678-109">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
    
- [<span data-ttu-id="07678-110">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="07678-110">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
    
<span data-ttu-id="07678-111">Der Aufruf von **IMAPIStatus::ValidateState** wirkt sich auf die Leistung nur, wenn für die MAPI-Warteschlange oder des MAPI-Subsystems vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="07678-111">The call to **IMAPIStatus::ValidateState** affects performance only when made on either the MAPI spooler or the MAPI subsystem.</span></span> <span data-ttu-id="07678-112">Der Grund dafür, dass diese Methoden zum Starten des Verarbeitung verlangsamen besteht, da sie nicht erfüllen können, bis die MAPI-Warteschlange ihrer Aufgaben zum Starten des beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="07678-112">The reason that these methods slow startup processing is because they cannot complete until the MAPI spooler has finished its startup tasks.</span></span> 
  
<span data-ttu-id="07678-113">Zudem sollten Sie Suchen des Nachrichtenspeichers beim Starten.</span><span class="sxs-lookup"><span data-stu-id="07678-113">You should also avoid searching the message store at startup time.</span></span> <span data-ttu-id="07678-114">Stellen Sie den Anruf [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) beim Start Verarbeitung beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="07678-114">Make your [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) call when startup processing has finished.</span></span> 
  

