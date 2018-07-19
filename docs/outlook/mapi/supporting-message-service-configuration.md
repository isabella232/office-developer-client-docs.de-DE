---
title: Unterstützende Nachricht Dienstkonfiguration
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e1782f3c20c1741e0e4b1859f1b29d835444009c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795653"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="8fa06-103">Unterstützende Nachricht Dienstkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8fa06-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="8fa06-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8fa06-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8fa06-105">Zur Unterstützung der Nachricht Dienstkonfiguration verwenden Sie die folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="8fa06-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="8fa06-106">Implementieren Sie eine Eintrag Point-Funktion, die den [MSGSERVICEENTRY](msgserviceentry.md) Prototyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="8fa06-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="8fa06-107">Nachricht Webdienstfunktionen Entry Point Verwalten des Zugriffs auf Konfigurationsdaten und werden in den folgenden Umständen aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="8fa06-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="8fa06-108">Abrufen von Informationen zum Konfigurieren Ihrer Messagingdiensts beim Anmelden eines Clients an.</span><span class="sxs-lookup"><span data-stu-id="8fa06-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="8fa06-109">Wenn ein Client möchte anzeigen oder Ändern einer Konfigurationseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8fa06-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="8fa06-110">Obwohl die meisten Message-Dienste wie gewünscht Entry Point-Funktionen, bereitgestellt werden, sind diese Funktionen nicht zwingend erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8fa06-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="8fa06-111">Message-Dienste können auf die Konfigurationsdaten auf andere Weise bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8fa06-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="8fa06-112">Jedoch eine Entry Point-Funktion verwenden standardisiert und vereinfacht den Prozess der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8fa06-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="8fa06-113">MAPI erwartet, dass alle Nachricht Service Eintrag Point-Funktionen können zum Speichern und Abrufen von Eigenschaften aus der Profil-Abschnitte, die ihre Nachrichtendienst zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8fa06-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="8fa06-114">Sie können diese Funktionalität unterstützen, interaktiv, programmgesteuert oder beide programmgesteuert und interaktiv.</span><span class="sxs-lookup"><span data-stu-id="8fa06-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="8fa06-115">Geben Sie zur Unterstützung der interaktiven Konfiguration eines Eigenschaftenblatts, das die Eigenschaften zum Konfigurieren Ihrer Messagingdiensts anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8fa06-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="8fa06-116">Optional können Sie auch Eigenschaftenseiten für jeden konfigurierbar Anbieter angeben.</span><span class="sxs-lookup"><span data-stu-id="8fa06-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="8fa06-117">Einige Nachrichtendienste beschränken Benutzer zu einer nur-Lese-Ansicht von Konfigurationseigenschaften. andere Nachrichtendienste können Benutzer Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="8fa06-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="8fa06-118">Zur Unterstützung der programmgesteuerte Konfiguration muss Ihre Nachricht Service Entry Point-Funktion ohne Benutzereingriff arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="8fa06-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="8fa06-119">Wenn Ihre Nachricht Service mit dem Profil-Assistenten aufgerufen werden kann, müssen Sie die programmgesteuerte Konfiguration unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8fa06-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="8fa06-120">Wenn Ihre Messagingdiensts nicht selbst konfiguriert werden soll, mithilfe der Profil-Assistent zulassen, können Sie ob programmgesteuerten Konfiguration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8fa06-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="8fa06-121">Weitere Informationen zur Unterstützung der Konfiguration in einer Nachricht Diensteintrag Funktion finden Sie [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="8fa06-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="8fa06-122">Veröffentlichen Sie den Namen Ihrer Nachricht Service Entry Point-Funktion in der Konfigurationsdatei Mapisvc.inf durch den folgenden Eintrag im Abschnitt Dienst Nachricht einschließlich:</span><span class="sxs-lookup"><span data-stu-id="8fa06-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="8fa06-123">Erstellen Sie eine oder mehrere Eigenschaft Blatt Dialogfelder für die Anzeige von Daten zur Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8fa06-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="8fa06-124">Führen Sie die folgenden Aufgaben aus, wenn Sie zulassen, des Profil-Assistenten, um Ihre Messagingdiensts zu konfigurieren möchten:</span><span class="sxs-lookup"><span data-stu-id="8fa06-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="8fa06-125">Implementieren Sie eine Eintrag Point-Funktion, die den [WIZARDENTRY](wizardentry.md) Prototyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="8fa06-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="8fa06-126">Implementieren Sie ein Windows Dialogfeld Feld Standardverfahren, die den [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) Prototyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="8fa06-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="8fa06-127">Verbessern Sie Ihre Nachricht Service Eintrag Point-Funktion, um auf zusätzliche Ereignisse zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="8fa06-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8fa06-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fa06-128">See also</span></span>

- [<span data-ttu-id="8fa06-129">Nachrichtendienstimplementierung</span><span class="sxs-lookup"><span data-stu-id="8fa06-129">Message Service Implementation</span></span>](message-service-implementation.md)

