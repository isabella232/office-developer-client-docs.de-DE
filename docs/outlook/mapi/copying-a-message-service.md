---
title: Kopieren eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425393"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="aaee2-103">Kopieren eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="aaee2-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="aaee2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaee2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="aaee2-105">**So kopieren Sie einen Nachrichtendienst in ein Profil**</span><span class="sxs-lookup"><span data-stu-id="aaee2-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="aaee2-106">Rufen [Sie IMsgServiceAdmin::CopyMsgService auf.](imsgserviceadmin-copymsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="aaee2-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="aaee2-107">Wenn ein Nachrichtendienst kopiert wird, wird die neue Instanz des Diensts auf die gleiche Weise wie das Original konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="aaee2-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="aaee2-108">Manchmal **gibt CopyMsgService** den Fehler MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="aaee2-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="aaee2-109">Die häufigste Ursache für diese Fehlerrückmeldung ist ein Nachrichtendienst, der sich nicht duplizieren lässt.</span><span class="sxs-lookup"><span data-stu-id="aaee2-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

