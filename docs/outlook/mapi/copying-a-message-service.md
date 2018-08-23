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
ms.openlocfilehash: 8388d14446a230b032e49ad0d614c85e79b8ece8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573719"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="9b105-103">Kopieren eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="9b105-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="9b105-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b105-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9b105-105">**Kopieren einer Messagingdiensts zu einem Profil**</span><span class="sxs-lookup"><span data-stu-id="9b105-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="9b105-106">Rufen Sie [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="9b105-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="9b105-107">Wenn ein Nachrichtendienst kopiert wird, ist die neue Instanz des Diensts auf genau die gleiche Weise wie die ursprüngliche konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="9b105-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="9b105-108">In einigen Fällen wird **CopyMsgService** der Fehler MAPI_E_ACCESS_DENIED zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b105-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="9b105-109">Die häufigste Ursache für diese Fehler Return ist ein Nachrichtendienst, der nicht selbst zu duplizierende zulässt.</span><span class="sxs-lookup"><span data-stu-id="9b105-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

