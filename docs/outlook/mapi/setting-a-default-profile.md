---
title: Festlegen eines Standardprofils
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439814"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="da02a-103">Festlegen eines Standardprofils</span><span class="sxs-lookup"><span data-stu-id="da02a-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="da02a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da02a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da02a-105">Das Standardprofil ist das Profil, das verwendet wird, wenn Sie im Aufruf von [MAPILogonEx](mapilogonex.md)nicht explizit angeben, sondern stattdessen das MAPI_USE_DEFAULT-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="da02a-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="da02a-106">**So richten Sie ein Standardprofil ein**</span><span class="sxs-lookup"><span data-stu-id="da02a-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="da02a-107">Rufen Sie die [MAPIAdminProfiles](mapiadminprofiles.md) -Funktion auf, um einen **IProfAdmin** -Schnittstellenzeiger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="da02a-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="da02a-108">Rufen Sie [IProfAdmin:: SetDefaultProfile](iprofadmin-setdefaultprofile.md)auf.</span><span class="sxs-lookup"><span data-stu-id="da02a-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="da02a-109">**SetDefaultProfile** legt die **PR_DEFAULT_PROFILE** ([pidtagdefaultprofile (](pidtagdefaultprofile-canonical-property.md))-Eigenschaft für das neue Standardprofil fest und entfernt die Einstellung für das vorherige Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="da02a-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

