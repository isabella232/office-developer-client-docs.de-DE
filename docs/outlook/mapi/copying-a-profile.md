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
ms.openlocfilehash: 53b7099ae74828a97eb703b865ba30ab385e9a5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564934"
---
# <a name="copying-a-profile"></a><span data-ttu-id="685ec-103">Kopieren eines Profils</span><span class="sxs-lookup"><span data-stu-id="685ec-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="685ec-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="685ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="685ec-105">Eine Möglichkeit zum Erstellen eines Profils ist Kopieren eines vorhandenen Profils und ändern Sie die erforderlichen Message-Dienste und -Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="685ec-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="685ec-106">Kopieren eines Profils beinhaltet die Verwendung einer Profile Administration-Objekt von MAPI über die Funktion ["MAPIAdminProfiles"](mapiadminprofiles.md) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="685ec-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="685ec-107">**Kopieren ein Profils**</span><span class="sxs-lookup"><span data-stu-id="685ec-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="685ec-108">Rufen Sie **"MAPIAdminProfiles"** zum Abrufen eines **IProfAdmin** Schnittstelle Zeigers.</span><span class="sxs-lookup"><span data-stu-id="685ec-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="685ec-109">Rufen Sie [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) Zugriff auf die Benutzerprofildienst-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="685ec-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="685ec-110">Erstellen Sie eine eigenschaftseinschränkung mit einer [SPropertyRestriction](spropertyrestriction.md) Struktur entsprechend **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen des Profils, kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="685ec-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="685ec-111">Rufen Sie [IMAPITable](imapitable-findrow.md) , um die entsprechende Zeile in der Profiltabelle zu suchen.</span><span class="sxs-lookup"><span data-stu-id="685ec-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="685ec-112">Rufen Sie [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), der Wert der Spalte **PR_DISPLAY_NAME** als _LpszOldProfileName_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="685ec-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

