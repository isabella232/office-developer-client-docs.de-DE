---
title: Profiltabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1046c8d92feec16428329636257ed9c1f0ec8719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571479"
---
# <a name="profile-tables"></a><span data-ttu-id="fd4fb-103">Profiltabellen</span><span class="sxs-lookup"><span data-stu-id="fd4fb-103">Profile Tables</span></span>

  
  
<span data-ttu-id="fd4fb-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd4fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd4fb-105">Die Benutzerprofildienst-Tabelle enthält Informationen über alle Profile, die mit einer bestimmten Clientanwendung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="fd4fb-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="fd4fb-106">Es wird eine Profiltabelle für jede Sitzung für die Verwendung durch Clients von MAPI implementiert.</span><span class="sxs-lookup"><span data-stu-id="fd4fb-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="fd4fb-107">Clientzugriff durch Aufrufen der [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) -Methode die Benutzerprofildienst-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fd4fb-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="fd4fb-108">Die Benutzerprofildienst-Tabelle ist eine statische Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fd4fb-108">The profile table is a static table.</span></span> <span data-ttu-id="fd4fb-109">Profile, die zum Löschen gekennzeichnet wurden, sind nicht in der Profiltabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="fd4fb-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="fd4fb-110">Als wird mit den meisten Tabelle Implementierungen, wenn **"GetProfileTable"** aufgerufen wird und es keine Profile an den Client sind, die Tabelle mit null Zeilen erstellt.</span><span class="sxs-lookup"><span data-stu-id="fd4fb-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="fd4fb-111">Die folgenden Eigenschaften bilden die erforderliche Spalte im Profil Tabellen festzulegen:</span><span class="sxs-lookup"><span data-stu-id="fd4fb-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="fd4fb-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fd4fb-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fd4fb-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fd4fb-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd4fb-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd4fb-114">See also</span></span>



[<span data-ttu-id="fd4fb-115">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="fd4fb-115">MAPI Tables</span></span>](mapi-tables.md)

