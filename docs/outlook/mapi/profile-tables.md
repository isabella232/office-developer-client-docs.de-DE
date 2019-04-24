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
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328560"
---
# <a name="profile-tables"></a><span data-ttu-id="94cc2-103">Profiltabellen</span><span class="sxs-lookup"><span data-stu-id="94cc2-103">Profile Tables</span></span>

  
  
<span data-ttu-id="94cc2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94cc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94cc2-105">In der Profiltabelle werden Informationen zu allen Profilen aufgelistet, die einer bestimmten Clientanwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="94cc2-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="94cc2-106">Es gibt eine Profiltabelle für jede Sitzung, die von MAPI zur Verwendung durch Clients implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="94cc2-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="94cc2-107">Clients greifen auf die Profiltabelle zu, indem Sie die [IProfAdmin::](iprofadmin-getprofiletable.md) getprofilable-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="94cc2-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="94cc2-108">Die Profiltabelle ist eine statische Tabelle.</span><span class="sxs-lookup"><span data-stu-id="94cc2-108">The profile table is a static table.</span></span> <span data-ttu-id="94cc2-109">Profile, die zum Löschen markiert wurden, sind nicht in der Profiltabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="94cc2-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="94cc2-110">Wie bei den meisten Tabellen Implementierungen \*\*\*\* wird die Tabelle mit null Zeilen erstellt, wenn getprofilable aufgerufen wird und keine Profile für den Client verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="94cc2-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="94cc2-111">Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in Profiltabellen:</span><span class="sxs-lookup"><span data-stu-id="94cc2-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="94cc2-112">**PR_DEFAULT_PROFILE** ([Pidtagdefaultprofile (](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="94cc2-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="94cc2-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="94cc2-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94cc2-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94cc2-114">See also</span></span>



[<span data-ttu-id="94cc2-115">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="94cc2-115">MAPI Tables</span></span>](mapi-tables.md)

