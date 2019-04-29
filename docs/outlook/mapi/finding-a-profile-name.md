---
title: Suchen nach einem Profilnamen
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
# <a name="finding-a-profile-name"></a><span data-ttu-id="d349d-103">Suchen nach einem Profilnamen</span><span class="sxs-lookup"><span data-stu-id="d349d-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="d349d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d349d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d349d-105">Clients müssen manchmal den Namen des Profils ermitteln, das derzeit für die Sitzung verwendet wird, den Namen des Standardprofils oder den Namen eines alternativen Profils, das auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d349d-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="d349d-106">Es gibt verschiedene Möglichkeiten, den Namen eines Profils während einer Sitzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d349d-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="d349d-107">Wenn Sie den Namen eines Profils suchen müssen, das nicht unbedingt derjenige ist, der für die Sitzung verwendet wird, verwenden Sie das erste Verfahren.</span><span class="sxs-lookup"><span data-stu-id="d349d-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="d349d-108">Wenn Sie den Namen des Standardprofils suchen müssen, verwenden Sie die zweite Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="d349d-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="d349d-109">Wenn Sie den Namen des aktuellen Profils für die Sitzung suchen müssen, verwenden Sie das letzte Verfahren.</span><span class="sxs-lookup"><span data-stu-id="d349d-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="d349d-110">**So suchen Sie nach dem Namen eines beliebigen Profils**</span><span class="sxs-lookup"><span data-stu-id="d349d-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="d349d-111">Rufen Sie [MAPIAdminProfiles](mapiadminprofiles.md) auf, um einen **IProfAdmin** -Schnittstellenzeiger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d349d-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="d349d-112">Aufrufen von [IProfAdmin::](iprofadmin-getprofiletable.md) getprofilable für den Zugriff auf die Profiltabelle.</span><span class="sxs-lookup"><span data-stu-id="d349d-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="d349d-113">Rufen Sie die [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode der Profiltabelle auf, um alle Zeilen in der Tabelle abzurufen und zu überprüfen, ob Sie das Zielprofil darstellt.</span><span class="sxs-lookup"><span data-stu-id="d349d-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="d349d-114">**So suchen Sie nach dem Namen des Standardprofils**</span><span class="sxs-lookup"><span data-stu-id="d349d-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="d349d-115">Rufen Sie [MAPIAdminProfiles](mapiadminprofiles.md)auf.</span><span class="sxs-lookup"><span data-stu-id="d349d-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="d349d-116">Aufrufen von [IProfAdmin::](iprofadmin-getprofiletable.md) getprofilable für den Zugriff auf die Profiltabelle.</span><span class="sxs-lookup"><span data-stu-id="d349d-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="d349d-117">Erstellen Sie eine Eigenschaftseinschränkung mit einer [SPropertyRestriction](spropertyrestriction.md) -Struktur, um **PR_DEFAULT_PROFILE** ([PIDTAGDEFAULTPROFILE (](pidtagdefaultprofile-canonical-property.md)) mit dem Wert true zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="d349d-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="d349d-118">Rufen Sie [IMAPITable:: FindRow](imapitable-findrow.md) auf, um die Zeile in der Profiltabelle zu suchen, die das Standardprofil darstellt.</span><span class="sxs-lookup"><span data-stu-id="d349d-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="d349d-119">Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Spalte enthält den Namen des Standardprofils.</span><span class="sxs-lookup"><span data-stu-id="d349d-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="d349d-120">**So suchen Sie nach dem Namen des aktuellen Profils**</span><span class="sxs-lookup"><span data-stu-id="d349d-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="d349d-121">Führen Sie einen der folgenden Schritte aus, um den Namen des aktuellen Profils zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="d349d-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="d349d-122">Wenn Sie die [MAPIUID](mapiuid.md) -Struktur haben, die einen der Abschnitte des aktuellen Profils darstellt, übergeben Sie diese im Parameter _lpUID_ an [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md).</span><span class="sxs-lookup"><span data-stu-id="d349d-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="d349d-123">Rufen Sie die **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft des Profil Abschnitts mithilfe der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode ab.</span><span class="sxs-lookup"><span data-stu-id="d349d-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="d349d-124">Rufen Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable auf, um auf die Statustabelle zuzugreifen und die Zeile zu finden, deren **PR_RESOURCE_TYPE** ([pidtagresourcetype (](pidtagresourcetype-canonical-property.md)) auf MAPI_SUBSYSTEM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d349d-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="d349d-125">Die **PR_DISPLAY_NAME** -Spalte für diese Zeile ist der Profil Name.</span><span class="sxs-lookup"><span data-stu-id="d349d-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="d349d-126">Verwenden Sie die Status-Tabelle nicht während des Starts, da Sie eine Anwendung blockiert, bis der MAPI-Spooler alle Transportanbieter initialisiert hat.</span><span class="sxs-lookup"><span data-stu-id="d349d-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="d349d-127">Dies kann Ihre Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="d349d-127">This can degrade your performance.</span></span> 
    

