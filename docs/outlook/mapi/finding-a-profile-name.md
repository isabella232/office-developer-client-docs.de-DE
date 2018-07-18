---
title: Suchen nach einem Profilnamen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 332b78bcebbcd54de43376553ec4aea386c1c359
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791682"
---
# <a name="finding-a-profile-name"></a><span data-ttu-id="10b4a-103">Suchen nach einem Profilnamen</span><span class="sxs-lookup"><span data-stu-id="10b4a-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="10b4a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10b4a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10b4a-105">In einigen Fällen müssen Clients suchen den Namen des Profils wird derzeit für die Sitzung, den Namen des Standardprofils oder den Namen eines alternativen Profils auf dem Computer installierten verwendet.</span><span class="sxs-lookup"><span data-stu-id="10b4a-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="10b4a-106">Es gibt einige Methoden zum Abrufen des Namens eines Profils im Laufe einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="10b4a-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="10b4a-107">Wenn Sie den Namen eines Profils zu suchen, die nicht unbedingt für die Sitzung verwendet werden müssen, verwenden Sie das erste Verfahren.</span><span class="sxs-lookup"><span data-stu-id="10b4a-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="10b4a-108">Wenn Sie den Namen des Standardprofils suchen müssen, verwenden Sie das zweite Verfahren.</span><span class="sxs-lookup"><span data-stu-id="10b4a-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="10b4a-109">Wenn Sie den Namen des aktuellen Profils für die Sitzung zu suchen möchten, verwenden Sie das letzte Verfahren.</span><span class="sxs-lookup"><span data-stu-id="10b4a-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="10b4a-110">**Suchen Sie den Namen Profil**</span><span class="sxs-lookup"><span data-stu-id="10b4a-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="10b4a-111">Rufen Sie ["MAPIAdminProfiles"](mapiadminprofiles.md) zum Abrufen eines **IProfAdmin** Schnittstelle Zeigers.</span><span class="sxs-lookup"><span data-stu-id="10b4a-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="10b4a-112">Rufen Sie [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) Zugriff auf die Benutzerprofildienst-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="10b4a-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="10b4a-113">Rufen Sie [die Profiltabelle QueryRows zum Abrufen aller Zeilen in der Tabelle und Untersuchen von jedem Befehl die EINGABETASTE, um zu bestimmen, ob sie Ihr Zielprofil darstellt](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="10b4a-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="10b4a-114">**Der Name des Standardprofils gefunden**</span><span class="sxs-lookup"><span data-stu-id="10b4a-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="10b4a-115">Rufen Sie ["MAPIAdminProfiles"](mapiadminprofiles.md).</span><span class="sxs-lookup"><span data-stu-id="10b4a-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="10b4a-116">Rufen Sie [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) Zugriff auf die Benutzerprofildienst-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="10b4a-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="10b4a-117">Erstellen Sie eine eigenschaftseinschränkung mit einer [SPropertyRestriction](spropertyrestriction.md) Struktur, der **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) mit dem Wert TRUE entspricht.</span><span class="sxs-lookup"><span data-stu-id="10b4a-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="10b4a-118">Rufen Sie [IMAPITable](imapitable-findrow.md) , um die Zeile in der Profiltabelle zu suchen, die das Standardprofil darstellt.</span><span class="sxs-lookup"><span data-stu-id="10b4a-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="10b4a-119">Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Spalte enthält den Namen des Standardprofils.</span><span class="sxs-lookup"><span data-stu-id="10b4a-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="10b4a-120">**Der Name des aktuellen Profils gefunden**</span><span class="sxs-lookup"><span data-stu-id="10b4a-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="10b4a-121">Führen Sie die folgenden Schritte aus, um den Namen des aktuellen Profils zu finden:</span><span class="sxs-lookup"><span data-stu-id="10b4a-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="10b4a-122">Unter der Annahme, dass Sie die [MAPIUID](mapiuid.md) -Struktur, die einen der Abschnitte für das aktuelle Profil darstellt haben, übergeben Sie sie an [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)im _LpUID_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="10b4a-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="10b4a-123">Rufen Sie das Profilabschnitt **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft mithilfe der Methode [IMAPIProp::GetProps](imapiprop-getprops.md) ab.</span><span class="sxs-lookup"><span data-stu-id="10b4a-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="10b4a-124">Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) Zugriff auf die Statustabelle, und suchen Sie die Zeile, die die **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))-Spalte auf MAPI_SUBSYSTEM festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="10b4a-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="10b4a-125">Die **PR_DISPLAY_NAME** Spalte für diese Zeile ist der Name der Benutzerprofildienst.</span><span class="sxs-lookup"><span data-stu-id="10b4a-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="10b4a-126">Verwenden Sie nicht die Statustabelle während des Starts von, da es eine Anwendung blockiert, bis die MAPI-Warteschlange die Initialisierung aller Transportanbieter für den abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="10b4a-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="10b4a-127">Dies kann die Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="10b4a-127">This can degrade your performance.</span></span> 
    

