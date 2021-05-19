---
title: Löschen eines Profils
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410203"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="b5374-103">Löschen eines Profils</span><span class="sxs-lookup"><span data-stu-id="b5374-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="b5374-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5374-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b5374-105">**So löschen Sie ein Profil**</span><span class="sxs-lookup"><span data-stu-id="b5374-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="b5374-106">Rufen [Sie IProfAdmin::D eleteProfile auf.](iprofadmin-deleteprofile.md)</span><span class="sxs-lookup"><span data-stu-id="b5374-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="b5374-107">**DeleteProfile** markiert das Profil zum Löschen, wenn es derzeit verwendet wird, und wartet, bis es nicht mehr aktiv ist, um es zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="b5374-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="b5374-108">Das Profil wird erst ausgeblendet, wenn jeder Client mit einer aktiven Sitzung die Verbindung getrennt hat.</span><span class="sxs-lookup"><span data-stu-id="b5374-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="b5374-109">**DeleteProfile** ruft die Einstiegspunktfunktion jedes Nachrichtendiensts im Profil auf, bei dem der  _ulContext-Parameter_ auf MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="b5374-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="b5374-110">Die Aufrufe der Einstiegspunktfunktionen erfolgen, bevor die Dienste physisch aus dem Profil entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b5374-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

