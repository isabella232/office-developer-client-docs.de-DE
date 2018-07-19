---
title: Starten eines Dienstanbieters
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: 'Letzte Änderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 99f47ee4fe990b0e77fcf868977b72d83bfdbac7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795628"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="0eaf7-103">Starten eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="0eaf7-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="0eaf7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0eaf7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0eaf7-105">Zu einem bestimmten Zeitpunkt nach dem Starten eines Clients einer Sitzung mit MAPI, wird Ihr Dienstanbieter gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="0eaf7-106">Transportanbieter gestartet wurden, wenn ein Client für ihre Dienste anfordert.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="0eaf7-107">Address Book und Message-Anbieter werden während der Client Anmeldevorgang gestartet.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="0eaf7-108">Ein Client ruft [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) , um die im Profil und [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) zum Laden der Anbieter eine bestimmte Nachricht enthalten adressbuchanbietern implementierte zu laden.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="0eaf7-109">Von adressbuchanbietern implementierte, die Teil eines Diensts Nachricht sind wurden vor allen anderen Anbieter im Dienst gestartet.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="0eaf7-110">MAPI startet jeder Dienstanbieter in das aktive Profil, indem Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="0eaf7-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="0eaf7-111">Suchen den Namen der entsprechenden DLL im Profil.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="0eaf7-112">Sie müssen den Namen Ihres Anbieters DLL registrieren, in der Konfigurationsdatei Mapisvc.inf, um sicherzustellen, dass es im Profil angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="0eaf7-113">Wenn Ihr Dienstanbieter zu einem Profil einzeln oder als Teil eines Diensts Nachricht hinzugefügt wird, werden alle Abschnitte **[Service Provider]** aus Mapisvc.inf, die vom Dienstanbieter liegen, in das Profil kopiert.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="0eaf7-114">Weitere Informationen zur Struktur von Mapisvc.inf finden Sie unter [File Format der MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="0eaf7-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="0eaf7-115">Aufrufen der Windows-API-Funktion **LoadLibrary** zum Laden der DLL.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="0eaf7-116">Da MAPI **LoadLibrary** entweder jedes Mal, wenn es verwendet einen Dienstanbieter DLL (unabhängig davon, ob es bereits geladen wurde) oder nur beim ersten Mal aufruft, muss Ihren Dienstanbieter nicht Annahmen über die Anzahl der Male vornehmen, die sie geladen wird.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="0eaf7-117">Für jeden Aufruf von **LoadLibrary**führt MAPI einen Aufruf an die Windows-API-Funktion **FreeLibrary** bei einem Dienstanbieter, die, den DLL nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="0eaf7-118">Aufrufen der Eintrag Point-Funktion für den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="0eaf7-119">MAPI-Aufrufen des Anbieters Eintrag Point-Funktion zum Initiieren des Anmeldevorgangs.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="0eaf7-120">Entry Point Funktionen stellen Sie sicher, dass Sie eine Version der der Dienstanbieter-Schnittstelle (SPI) verwenden, die mit der Version von MAPI verwendet wird, kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="0eaf7-121">Diese Funktionen geben auch Zeiger auf neu erstellten Anbieterobjekte.</span><span class="sxs-lookup"><span data-stu-id="0eaf7-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="0eaf7-122">Zeigen Sie die Funktion für Weitere Informationen zum Erstellen eines Eintrags für den Anbieter, finden Sie unter [Implementieren einer Service Provider Eintrag zeigen-Funktion](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="0eaf7-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0eaf7-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0eaf7-123">See also</span></span>



[<span data-ttu-id="0eaf7-124">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0eaf7-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

