---
title: Erstellen eines Profils mithilfe von benutzerdefiniertem Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413304"
---
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="2af34-103">Erstellen eines Profils mithilfe von benutzerdefiniertem Code</span><span class="sxs-lookup"><span data-stu-id="2af34-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="2af34-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2af34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2af34-105">Wenn Sie Code zum Erstellen eines Profils schreiben, stellen Sie sicher, dass Sie wissen, wie Sie Profileinträge und die Art und Menge der Informationen, die für jeden Eintrag benötigt werden, bestellen können.</span><span class="sxs-lookup"><span data-stu-id="2af34-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="2af34-106">Die Auswirkungen der Reihenfolge von Einträgen in einem Profil werden in [MAPI](mapi-profiles.md)-Profilen erläutert.</span><span class="sxs-lookup"><span data-stu-id="2af34-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="2af34-107">**So erstellen Sie ein Profil mit C-oder C++-Code**</span><span class="sxs-lookup"><span data-stu-id="2af34-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="2af34-108">Lesen Sie die Headerdatei für jeden Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="2af34-108">Read the header file for each message service.</span></span> <span data-ttu-id="2af34-109">Verstehen Sie, welche Eigenschaften Sie konfigurieren müssen und welche Werte Sie verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="2af34-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="2af34-110">Rufen Sie die [MAPIAdminProfiles](mapiadminprofiles.md) -Funktion auf, um einen **IProfAdmin** -Schnittstellenzeiger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2af34-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="2af34-111">Rufen Sie [IProfAdmin:: CreateProfile](iprofadmin-createprofile.md) auf, um Ihr Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2af34-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="2af34-112">Wenn Sie ein Profil mit den Nachrichtendiensten erstellen möchten, die im Abschnitt **[Default Services]** des Mapisvc aufgeführt sind. INF-Datei, legen Sie das MAPI_DEFAULT_SERVICE-Flag fest.</span><span class="sxs-lookup"><span data-stu-id="2af34-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="2af34-113">Wenn Sie möchten, dass der Benutzerkonfigurationsinformationen eingeben kann, legen Sie das MAPI_DIALOG-Flag fest.</span><span class="sxs-lookup"><span data-stu-id="2af34-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="2af34-114">Stellen Sie sicher, dass Sie dieses Flag festlegen, wenn nicht alle erforderlichen Informationen über die MAPISVC verfügbar sind. INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="2af34-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="2af34-115">**CreateProfile** Ruft die Einstiegspunktfunktion für jeden Nachrichtendienst auf, der dem Profil hinzugefügt werden soll, wobei MSG_SERVICE_CREATE als _ulContext_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2af34-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="2af34-116">Rufen Sie [IProfAdmin:: AdminServices](iprofadmin-adminservices.md) auf, um ein Nachrichtendienst-Verwaltungsobjekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2af34-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="2af34-117">Verwenden Sie das Nachrichtendienst-Verwaltungsobjekt, um dem Profilnachrichten Dienste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2af34-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="2af34-118">Für jeden Nachrichtendienst, den Sie hinzufügen möchten:</span><span class="sxs-lookup"><span data-stu-id="2af34-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="2af34-119">Rufen Sie die [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode auf, um den neuen Nachrichtendienst zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2af34-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="2af34-120">Rufen Sie [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)auf, und übergeben Sie die **MAPIUID** -Struktur des soeben erstellten Diensts und ein Eigenschaftenwert Array mit den Konfigurationseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2af34-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="2af34-121">Zum Abrufen des Bezeichners eines neu hinzugefügten Diensts, bei dem es sich um die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Eigenschaft handelt, rufen Sie [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) auf, um auf die Nachrichtendienst Tabelle zuzugreifen und nach der Zeile zu suchen, die der Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="2af34-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="2af34-122">Die letzte Zeile in der Tabelle stellt den zuletzt hinzugefügten Nachrichtendienst dar.</span><span class="sxs-lookup"><span data-stu-id="2af34-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="2af34-123">Wenn Sie ein neues Profil als temporär festlegen möchten, rufen Sie die [IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md) -Methode unmittelbar nach der Anmeldung auf.</span><span class="sxs-lookup"><span data-stu-id="2af34-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="2af34-124">**DeleteProfile** markiert das neue Profil als gelöscht, während es für die Dauer der Sitzung nutzbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="2af34-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="2af34-125">Da es nicht in der Profiltabelle der Sitzung enthalten ist, können andere Clients es nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="2af34-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

