---
title: Profil Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 84c2d02da840dfcad077462954cb10894ba153d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795309"
---
# <a name="profile-tables"></a><span data-ttu-id="3410e-103">Profil Tabellen</span><span class="sxs-lookup"><span data-stu-id="3410e-103">Profile Tables</span></span>

  
  
<span data-ttu-id="3410e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3410e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3410e-105">Die Benutzerprofildienst-Tabelle enthält Informationen über alle Profile, die mit einer bestimmten Clientanwendung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3410e-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="3410e-106">Es wird eine Profiltabelle für jede Sitzung für die Verwendung durch Clients von MAPI implementiert.</span><span class="sxs-lookup"><span data-stu-id="3410e-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="3410e-107">Clientzugriff durch Aufrufen der [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) -Methode die Benutzerprofildienst-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3410e-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="3410e-108">Die Benutzerprofildienst-Tabelle ist eine statische Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3410e-108">The profile table is a static table.</span></span> <span data-ttu-id="3410e-109">Profile, die zum Löschen gekennzeichnet wurden, sind nicht in der Profiltabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="3410e-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="3410e-110">Als wird mit den meisten Tabelle Implementierungen, wenn **"GetProfileTable"** aufgerufen wird und es keine Profile an den Client sind, die Tabelle mit null Zeilen erstellt.</span><span class="sxs-lookup"><span data-stu-id="3410e-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="3410e-111">Die folgenden Eigenschaften bilden die erforderliche Spalte im Profil Tabellen festzulegen:</span><span class="sxs-lookup"><span data-stu-id="3410e-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="3410e-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3410e-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="3410e-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3410e-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3410e-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3410e-114">See also</span></span>



[<span data-ttu-id="3410e-115">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="3410e-115">MAPI Tables</span></span>](mapi-tables.md)

