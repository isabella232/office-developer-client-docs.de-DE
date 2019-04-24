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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333054"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="2bf5f-103">Kopieren eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="2bf5f-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="2bf5f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bf5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2bf5f-105">**So kopieren Sie einen Nachrichtendienst in ein Profil**</span><span class="sxs-lookup"><span data-stu-id="2bf5f-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="2bf5f-106">Rufen Sie [IMsgServiceAdmin:: CopyMsgService](imsgserviceadmin-copymsgservice.md)auf.</span><span class="sxs-lookup"><span data-stu-id="2bf5f-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="2bf5f-107">Wenn ein Nachrichtendienst kopiert wird, wird die neue Instanz des Diensts genau auf die gleiche Weise konfiguriert wie das Original.</span><span class="sxs-lookup"><span data-stu-id="2bf5f-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="2bf5f-108">Manchmal gibt **CopyMsgService** den Fehler MAPI_E_ACCESS_DENIED zurück.</span><span class="sxs-lookup"><span data-stu-id="2bf5f-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="2bf5f-109">Die häufigste Ursache für diesen Fehler ist ein Nachrichtendienst, der nicht dupliziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2bf5f-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

