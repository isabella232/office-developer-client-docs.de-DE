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
ms.openlocfilehash: 21aafebefcb7e10e6ba432f2eb3cc5dc04978c20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318088"
---
# <a name="avoiding-certain-methods-at-startup"></a><span data-ttu-id="bd8a6-103">Vermeiden bestimmter Methoden beim Start</span><span class="sxs-lookup"><span data-stu-id="bd8a6-103">Avoiding Certain Methods at Startup</span></span>

 
  
<span data-ttu-id="bd8a6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd8a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd8a6-105">Zur Verbesserung der Leistung beim Starte vermeiden Sie die folgenden Aufrufe:</span><span class="sxs-lookup"><span data-stu-id="bd8a6-105">To improve performance at startup time, avoid making the following calls:</span></span>
  
- [<span data-ttu-id="bd8a6-106">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="bd8a6-106">IMAPISession::EnumAdrTypes</span></span>](imapisession-enumadrtypes.md)
    
- [<span data-ttu-id="bd8a6-107">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="bd8a6-107">IMAPISession::GetStatusTable</span></span>](imapisession-getstatustable.md)
    
- [<span data-ttu-id="bd8a6-108">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="bd8a6-108">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
    
- [<span data-ttu-id="bd8a6-109">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="bd8a6-109">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
    
- [<span data-ttu-id="bd8a6-110">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="bd8a6-110">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
    
<span data-ttu-id="bd8a6-111">Der Aufruf von **IMAPIStatus::ValidateState** wirkt sich nur dann auf die Leistung aus, wenn er entweder im MAPI-Spooler oder im MAPI-Untersystem vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="bd8a6-111">The call to **IMAPIStatus::ValidateState** affects performance only when made on either the MAPI spooler or the MAPI subsystem.</span></span> <span data-ttu-id="bd8a6-112">Der Grund dafür, warum diese Methoden den Systemstartvorgang verlangsamen, liegt darin, dass sie erst abgeschlossen werden können, wenn der MAPI-Spooler seine Startaufgaben abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="bd8a6-112">The reason that these methods slow startup processing is because they cannot complete until the MAPI spooler has finished its startup tasks.</span></span> 
  
<span data-ttu-id="bd8a6-113">Sie sollten beim Systemstart auch nicht den Nachrichtenspeicher durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="bd8a6-113">You should also avoid searching the message store at startup time.</span></span> <span data-ttu-id="bd8a6-114">Tätigen Sie den [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)-Aufruf, wenn der Startvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bd8a6-114">Make your [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) call when startup processing has finished.</span></span> 
  

