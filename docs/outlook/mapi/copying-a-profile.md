---
title: Kopieren eines Profils
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424728"
---
# <a name="copying-a-profile"></a><span data-ttu-id="e2694-103">Kopieren eines Profils</span><span class="sxs-lookup"><span data-stu-id="e2694-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="e2694-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2694-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2694-105">Eine Möglichkeit zum Erstellen eines Profils ist das Kopieren aus einem vorhandenen Profil und das Ändern der erforderlichen Nachrichtendienste und Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="e2694-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="e2694-106">Das Kopieren eines Profils umfasst die Verwendung eines Profilverwaltungsobjekts, das von MAPI über die [MAPIAdminProfiles-Funktion bereitgestellt](mapiadminprofiles.md) wird.</span><span class="sxs-lookup"><span data-stu-id="e2694-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="e2694-107">**So kopieren Sie ein Profil**</span><span class="sxs-lookup"><span data-stu-id="e2694-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="e2694-108">Rufen **Sie MAPIAdminProfiles auf,** um einen **IProfAdmin-Schnittstellenzeiger** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e2694-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="e2694-109">Rufen [Sie IProfAdmin::GetProfileTable auf,](iprofadmin-getprofiletable.md) um auf die Profiltabelle zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e2694-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="e2694-110">Erstellen Sie eine Eigenschaftseinschränkung mit [einer SPropertyRestriction-Struktur,](spropertyrestriction.md) um PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen des zu kopierenden Profils zu übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e2694-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="e2694-111">Rufen [Sie IMAPITable::FindRow auf,](imapitable-findrow.md) um die entsprechende Zeile in der Profiltabelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="e2694-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="e2694-112">Rufen [Sie IProfAdmin::CopyProfile](iprofadmin-copyprofile.md)auf, und übergeben Sie den Wert der **PR_DISPLAY_NAME** als _lpszOldProfileName-Parameter._</span><span class="sxs-lookup"><span data-stu-id="e2694-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

