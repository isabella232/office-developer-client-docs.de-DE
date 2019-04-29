---
title: Starten eines Dienstanbieters
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439555"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="c9fd6-103">Starten eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="c9fd6-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="c9fd6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9fd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9fd6-105">Sobald ein Client eine Sitzung mit MAPI startet, wird der Dienstanbieter gestartet.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="c9fd6-106">Transport Anbieter werden gestartet, wenn ein Client eine Anforderung für ihre Dienste stellt.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="c9fd6-107">Adressbuch-und Nachrichtenspeicher Anbieter werden während des Anmeldevorgangs des Clients gestartet.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="c9fd6-108">Ein Client ruft [IMAPISession:: openaddressbook](imapisession-openaddressbook.md) auf, um alle im Profil enthaltenen Adressbuchanbieter und [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) zu laden, um einen bestimmten Nachrichtenspeicher Anbieter zu laden.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="c9fd6-109">Adressbuchanbieter, die Teil eines Nachrichtendiensts sind, werden vor einem der anderen Anbieter im Dienst gestartet.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="c9fd6-110">MAPI startet jeden Dienstanbieter im aktiven Profil wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c9fd6-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="c9fd6-111">Suchen des Namens der DLL im Profil.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="c9fd6-112">Sie müssen den Namen der Anbieter-DLL in der Konfigurationsdatei MAPISVC. inf registrieren, um sicherzustellen, dass Sie im Profil angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="c9fd6-113">Wenn Ihr Dienstanbieter einem Profil einzeln oder als Teil eines Nachrichtendiensts hinzugefügt wird, werden alle **[Dienstanbieter]** Abschnitte aus MAPISVC. inf, die für Ihren Anbieter gelten, in das Profil kopiert.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="c9fd6-114">Weitere Informationen zur Struktur von MAPISVC. inf finden Sie unter [Datei Format von MAPISVC. inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="c9fd6-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="c9fd6-115">Aufrufen der Windows-API-Funktion **LoadLibrary** zum Laden der dll.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="c9fd6-116">Da MAPI bei jeder Verwendung einer Dienstanbieter-DLL (unabhängig davon, ob Sie bereits geladen wurde) oder nur zum ersten Mal **LoadLibrary** aufruft, darf der Dienstanbieter keine Annahmen darüber treffen, wie oft er geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="c9fd6-117">Bei jedem Aufruf von **LoadLibrary**führt MAPI einen Aufruf der Windows-API-Funktion **FreeLibrary** aus, wenn keine Dienstanbieter-dll mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="c9fd6-118">Aufrufen der Einstiegspunktfunktion für den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="c9fd6-119">MAPI Ruft die Einstiegspunktfunktion Ihres Anbieters auf, um den Anmeldevorgang zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="c9fd6-120">Einstiegspunktfunktionen stellen Sie sicher, dass Sie eine Version der Dienstanbieterschnittstelle (Service Provider Interface, SPI) verwenden, die mit der von MAPI verwendeten Version kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="c9fd6-121">Diese Funktionen geben auch Zeiger auf neu erstellte Anbieterobjekte zurück.</span><span class="sxs-lookup"><span data-stu-id="c9fd6-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="c9fd6-122">Weitere Informationen zum Erstellen einer Einstiegspunktfunktion für Ihren Anbieter finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="c9fd6-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9fd6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9fd6-123">See also</span></span>



[<span data-ttu-id="c9fd6-124">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c9fd6-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

