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
ms.openlocfilehash: d13af3a2d0293641fd87d1065bceedfa4b62a3b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573243"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="5fbcb-103">Löschen eines Profils</span><span class="sxs-lookup"><span data-stu-id="5fbcb-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="5fbcb-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fbcb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="5fbcb-105">**Zum Löschen eines Profils**</span><span class="sxs-lookup"><span data-stu-id="5fbcb-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="5fbcb-106">Rufen Sie [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span><span class="sxs-lookup"><span data-stu-id="5fbcb-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="5fbcb-107">**DeleteProfile** markiert das Profil zum Löschen, wenn es derzeit warten verwendet wird, bis es nicht mehr entfernen aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="5fbcb-108">Das Profil wird nicht tatsächlich ausgeblendet, bis jeder Client mit einer aktiven Sitzung unterbrochen hat.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="5fbcb-109">**DeleteProfile** Ruft die Eintrags-Funktion von jeder Nachrichtendienst im Profil mit dem _UlContext_ -Parameter auf MSG_SERVICE_DELETE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="5fbcb-110">Die Aufrufe an den Eintrag Punktfunktionen tritt auf, bevor die Dienste physisch aus dem Profil entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5fbcb-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

