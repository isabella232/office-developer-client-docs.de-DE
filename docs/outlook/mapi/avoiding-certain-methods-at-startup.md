---
title: Vermeiden bestimmter Methoden beim Start
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Zuletzt geändert: 07. Dezember 2015'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580635"
---
# <a name="avoiding-certain-methods-at-startup"></a><span data-ttu-id="cae9f-103">Vermeiden bestimmter Methoden beim Start</span><span class="sxs-lookup"><span data-stu-id="cae9f-103">Avoiding Certain Methods at Startup</span></span>

 
  
<span data-ttu-id="cae9f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cae9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cae9f-105">Zur Verbesserung der Leistung beim Starte vermeiden Sie die folgenden Aufrufe:</span><span class="sxs-lookup"><span data-stu-id="cae9f-105">To improve performance at startup time, avoid making the following calls:</span></span>
  
- [<span data-ttu-id="cae9f-106">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="cae9f-106">IMAPISession::EnumAdrTypes</span></span>](imapisession-enumadrtypes.md)
    
- [<span data-ttu-id="cae9f-107">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="cae9f-107">IMAPISession::GetStatusTable</span></span>](imapisession-getstatustable.md)
    
- [<span data-ttu-id="cae9f-108">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="cae9f-108">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
    
- [<span data-ttu-id="cae9f-109">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="cae9f-109">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
    
- [<span data-ttu-id="cae9f-110">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="cae9f-110">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
    
<span data-ttu-id="cae9f-111">Der Aufruf von **IMAPIStatus::ValidateState** wirkt sich nur dann auf die Leistung aus, wenn er entweder im MAPI-Spooler oder im MAPI-Untersystem vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="cae9f-111">The call to **IMAPIStatus::ValidateState** affects performance only when made on either the MAPI spooler or the MAPI subsystem.</span></span> <span data-ttu-id="cae9f-112">Der Grund dafür, warum diese Methoden den Systemstartvorgang verlangsamen, liegt darin, dass sie erst abgeschlossen werden können, wenn der MAPI-Spooler seine Startaufgaben abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="cae9f-112">The reason that these methods slow startup processing is because they cannot complete until the MAPI spooler has finished its startup tasks.</span></span> 
  
<span data-ttu-id="cae9f-113">Sie sollten beim Systemstart auch nicht den Nachrichtenspeicher durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="cae9f-113">You should also avoid searching the message store at startup time.</span></span> <span data-ttu-id="cae9f-114">Tätigen Sie den [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)-Aufruf, wenn der Startvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cae9f-114">Make your [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) call when startup processing has finished.</span></span> 
  

