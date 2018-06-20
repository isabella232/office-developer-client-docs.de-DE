---
title: Ein Standardprofil festlegen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ea21e735dba8690a392629b92b636b834d7d57d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795503"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="7bbb9-103">Ein Standardprofil festlegen</span><span class="sxs-lookup"><span data-stu-id="7bbb9-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="7bbb9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7bbb9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7bbb9-105">Das Standardprofil ist das Profil, das verwendet wird, wenn Sie nicht explizit eine im Aufruf [MAPILogonEx](mapilogonex.md), stattdessen das MAPI_USE_DEFAULT-Flag festlegen angeben.</span><span class="sxs-lookup"><span data-stu-id="7bbb9-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="7bbb9-106">**Ein Standardprofil herstellen**</span><span class="sxs-lookup"><span data-stu-id="7bbb9-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="7bbb9-107">Rufen Sie die Funktion ["MAPIAdminProfiles"](mapiadminprofiles.md) zum Abrufen eines **IProfAdmin** Schnittstelle Zeigers.</span><span class="sxs-lookup"><span data-stu-id="7bbb9-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="7bbb9-108">Rufen Sie [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="7bbb9-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="7bbb9-109">**SetDefaultProfile** die **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))-Eigenschaft für neues Standardprofil festgelegt und die Einstellung für das vorherige Standardprofil entfernt.</span><span class="sxs-lookup"><span data-stu-id="7bbb9-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

