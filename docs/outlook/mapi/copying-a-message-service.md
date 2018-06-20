---
title: Kopieren eines Nachricht-Diensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791431"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="4d4ec-103">Kopieren eines Nachricht-Diensts</span><span class="sxs-lookup"><span data-stu-id="4d4ec-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="4d4ec-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4d4ec-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="4d4ec-105">**Kopieren einer Messagingdiensts zu einem Profil**</span><span class="sxs-lookup"><span data-stu-id="4d4ec-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="4d4ec-106">Rufen Sie [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="4d4ec-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="4d4ec-107">Wenn ein Nachrichtendienst kopiert wird, ist die neue Instanz des Diensts auf genau die gleiche Weise wie die ursprüngliche konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4d4ec-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="4d4ec-108">In einigen Fällen wird **CopyMsgService** der Fehler MAPI_E_ACCESS_DENIED zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4d4ec-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="4d4ec-109">Die häufigste Ursache für diese Fehler Return ist ein Nachrichtendienst, der nicht selbst zu duplizierende zulässt.</span><span class="sxs-lookup"><span data-stu-id="4d4ec-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

