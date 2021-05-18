---
title: Suchen eines Profilnamens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407921"
---
# <a name="finding-a-profile-name"></a><span data-ttu-id="8332f-103">Suchen eines Profilnamens</span><span class="sxs-lookup"><span data-stu-id="8332f-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="8332f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8332f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8332f-105">Clients müssen manchmal den Namen des Profils finden, das derzeit für die Sitzung verwendet wird, den Namen des Standardprofils oder den Namen eines alternativen Profils, das auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8332f-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="8332f-106">Es gibt mehrere Möglichkeiten, den Namen eines Profils während einer Sitzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8332f-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="8332f-107">Wenn Sie den Namen eines Profils suchen müssen, das nicht unbedingt für die Sitzung verwendet wird, verwenden Sie das erste Verfahren.</span><span class="sxs-lookup"><span data-stu-id="8332f-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="8332f-108">Wenn Sie den Namen des Standardprofils suchen müssen, verwenden Sie das zweite Verfahren.</span><span class="sxs-lookup"><span data-stu-id="8332f-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="8332f-109">Wenn Sie den Namen des aktuellen Profils für die Sitzung suchen müssen, verwenden Sie das letzte Verfahren.</span><span class="sxs-lookup"><span data-stu-id="8332f-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="8332f-110">**So suchen Sie den Namen eines profils**</span><span class="sxs-lookup"><span data-stu-id="8332f-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="8332f-111">Rufen [Sie MAPIAdminProfiles auf,](mapiadminprofiles.md) um einen **IProfAdmin-Schnittstellenzeiger** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8332f-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="8332f-112">Rufen [Sie IProfAdmin::GetProfileTable auf,](iprofadmin-getprofiletable.md) um auf die Profiltabelle zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8332f-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="8332f-113">Rufen Sie die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) der Profiltabelle auf, um alle Zeilen in der Tabelle abzurufen und die einzelnen Zeilen zu untersuchen, um festzustellen, ob sie Ihr Zielprofil darstellt.</span><span class="sxs-lookup"><span data-stu-id="8332f-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="8332f-114">**So suchen Sie den Namen des Standardprofils**</span><span class="sxs-lookup"><span data-stu-id="8332f-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="8332f-115">Rufen [Sie MAPIAdminProfiles auf.](mapiadminprofiles.md)</span><span class="sxs-lookup"><span data-stu-id="8332f-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="8332f-116">Rufen [Sie IProfAdmin::GetProfileTable auf,](iprofadmin-getprofiletable.md) um auf die Profiltabelle zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8332f-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="8332f-117">Erstellen Sie eine Eigenschaftseinschränkung mit [einer SPropertyRestriction-Struktur,](spropertyrestriction.md) um PR_DEFAULT_PROFILE **(** [PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) mit dem Wert TRUE zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8332f-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="8332f-118">Rufen [Sie IMAPITable::FindRow](imapitable-findrow.md) auf, um die Zeile in der Profiltabelle zu finden, die das Standardprofil darstellt.</span><span class="sxs-lookup"><span data-stu-id="8332f-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="8332f-119">Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) enthält den Namen des Standardprofils.</span><span class="sxs-lookup"><span data-stu-id="8332f-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="8332f-120">**So suchen Sie den Namen des aktuellen Profils**</span><span class="sxs-lookup"><span data-stu-id="8332f-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="8332f-121">Führen Sie einen der folgenden Schritte aus, um den Namen des aktuellen Profils zu finden:</span><span class="sxs-lookup"><span data-stu-id="8332f-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="8332f-122">Wenn Sie die [MAPIUID-Struktur](mapiuid.md) haben, die einen der Abschnitte des aktuellen Profils darstellt, übergeben Sie sie im  _lpUID-Parameter_ an [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span><span class="sxs-lookup"><span data-stu-id="8332f-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="8332f-123">Rufen Sie die PR_PROFILE_NAME **(** [PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft des Profilabschnitts mithilfe der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) ab.</span><span class="sxs-lookup"><span data-stu-id="8332f-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="8332f-124">Rufen [Sie IMAPISession::GetStatusTable](imapisession-getstatustable.md) auf, um auf die Statustabelle zu zugreifen und die Zeile zu suchen, für die **die Spalte PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) auf MAPI_SUBSYSTEM.</span><span class="sxs-lookup"><span data-stu-id="8332f-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="8332f-125">Die **PR_DISPLAY_NAME** spalte für diese Zeile ist der Profilname.</span><span class="sxs-lookup"><span data-stu-id="8332f-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="8332f-126">Verwenden Sie die Statustabelle beim Starten nicht, da sie eine Anwendung blockiert, bis der MAPI-Spooler alle Transportanbieter initialisiert hat.</span><span class="sxs-lookup"><span data-stu-id="8332f-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="8332f-127">Dies kann ihre Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="8332f-127">This can degrade your performance.</span></span> 
    

