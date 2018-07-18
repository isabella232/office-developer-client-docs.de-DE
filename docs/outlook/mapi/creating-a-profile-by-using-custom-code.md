---
title: Erstellen ein Profil mit benutzerdefiniertem Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 74869293215b86c69ab4e0b1337be6014419fa3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791488"
---
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="6b1f4-103">Erstellen ein Profil mit benutzerdefiniertem Code</span><span class="sxs-lookup"><span data-stu-id="6b1f4-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="6b1f4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b1f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b1f4-105">Wenn Sie dem Schreiben von Code zum Erstellen eines Profils auswählen, stellen Sie sicher, dass Sie verstehen, wie bestellen profileinträgen und den Typ und die Menge der Informationen, die für jeden Eintrag erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="6b1f4-106">Die Auswirkungen der Einträge in einem Profil Sortierung in [MAPI-Profile](mapi-profiles.md)erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="6b1f4-107">**Zum Erstellen eines Profils mit C oder C++-code**</span><span class="sxs-lookup"><span data-stu-id="6b1f4-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="6b1f4-108">Lesen Sie die Headerdatei für jeden Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-108">Read the header file for each message service.</span></span> <span data-ttu-id="6b1f4-109">Verstehen, welche Eigenschaften, die Sie konfigurieren müssen und welche Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="6b1f4-110">Rufen Sie die Funktion ["MAPIAdminProfiles"](mapiadminprofiles.md) zum Abrufen eines **IProfAdmin** Schnittstelle Zeigers.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="6b1f4-111">Rufen Sie [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) um Ihr Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="6b1f4-112">Wenn Sie ein Profil mit der Nachrichtendienste aufgeführt, in der die Datei MAPISVC im Abschnitt **[Default Services]** erstellen möchten. INF-Datei, legen Sie das MAPI_DEFAULT_SERVICE-Flag.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="6b1f4-113">Wenn Sie den Benutzer zur Eingabe von Konfigurationsinformationen aktivieren möchten, legen Sie die MAPI_DIALOG-Flag.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="6b1f4-114">Stellen Sie sicher, dass Sie dieses Flag festlegen, wenn nicht alle erforderlichen Informationen über die Datei MAPISVC verfügbar ist. INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="6b1f4-115">**CreateProfile** Ruft die Funktion Eintrag für jeden Nachrichtendienst mit MSG_SERVICE_CREATE als _UlContext_ -Parameter festgelegt, das Profil hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="6b1f4-116">Rufen Sie [IProfAdmin::AdminServices](iprofadmin-adminservices.md) , um eine Nachricht Service Administration-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="6b1f4-117">Verwenden Sie das Objekt "Message" Service Administration Message-Dienste zu dem Profil hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="6b1f4-118">Für jeden Nachrichtendienst, die Sie hinzufügen möchten:</span><span class="sxs-lookup"><span data-stu-id="6b1f4-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="6b1f4-119">Rufen Sie die [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode, um den neuen Dienst erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="6b1f4-120">Rufen Sie [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), übergeben Sie die **MAPIUID** Struktur des Diensts, den Sie gerade erstellt haben und ein Array-Eigenschaft Wert Konfiguration Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="6b1f4-121">Rufen Sie auf, um den Bezeichner für den Dienst neu hinzugefügte abzurufen, das die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaft ist, [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) Zugriff auf die Nachricht Service Tabelle und suchen Sie nach der Zeile, die darstellt der Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="6b1f4-122">Die letzte Zeile in der Tabelle wird die zuletzt hinzugefügten Messagingdiensts darstellen.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="6b1f4-123">Um ein neues Profil temporäre machen, rufen Sie die [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) -Methode unmittelbar nach der Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="6b1f4-124">**DeleteProfile** kennzeichnet das neue Profil als gelöscht und dass es für die Dauer der Sitzung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="6b1f4-125">Weil es nicht in der Sitzung Profiltabelle enthalten, werden andere Clients nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b1f4-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

