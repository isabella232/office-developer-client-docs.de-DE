---
title: Unterstützen der Nachrichtendienstkonfiguration
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: aa1a433e90eda24f1199783bc604e047deb03ecd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350610"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="2df9f-103">Unterstützen der Nachrichtendienstkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2df9f-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="2df9f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2df9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2df9f-105">Gehen Sie folgendermaßen vor, um die Nachrichtendienst Konfiguration zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="2df9f-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="2df9f-106">Implementieren Sie eine Einstiegspunktfunktion, die dem [MSGSERVICEENTRY](msgserviceentry.md) -Prototyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="2df9f-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="2df9f-107">Einstiegspunktfunktionen für den Nachrichtendienst verwalten den Zugriff auf Konfigurationsdaten und werden in den folgenden Situationen aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="2df9f-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="2df9f-108">Wenn ein Client sich anmeldet, um Informationen zum Konfigurieren des Nachrichtendiensts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2df9f-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="2df9f-109">Wenn ein Client eine Konfigurationseigenschaft anzeigen oder ändern möchte.</span><span class="sxs-lookup"><span data-stu-id="2df9f-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="2df9f-110">Obwohl die meisten Nachrichtendienste Einstiegspunktfunktionen bereitstellen, sind diese Funktionen nicht unbedingt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2df9f-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="2df9f-111">Nachrichtendienste können auf andere Weise auf Konfigurationsdaten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2df9f-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="2df9f-112">Die Verwendung einer Einstiegspunktfunktion standardisiert und vereinfacht jedoch den Konfigurationsprozess.</span><span class="sxs-lookup"><span data-stu-id="2df9f-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="2df9f-113">MAPI erwartet, dass alle Einstiegspunktfunktionen des Nachrichtendiensts Eigenschaften aus den Profil Abschnitten speichern und abrufen können, die dem Nachrichtendienst zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2df9f-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="2df9f-114">Sie können diese Funktionalität interaktiv, programmgesteuert oder interaktiv und programmgesteuert unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2df9f-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="2df9f-115">Zur Unterstützung der interaktiven Konfiguration geben Sie ein Eigenschaftenfenster an, in dem die an der Konfiguration des Nachrichtendiensts beteiligten Eigenschaften angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2df9f-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="2df9f-116">Optional können Sie auch Eigenschaftenblätter für jeden konfigurierbaren Anbieter bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2df9f-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="2df9f-117">Einige Nachrichtendienste schränken Benutzer auf eine schreibgeschützte Ansicht der Konfigurationseigenschaften ein. andere Nachrichtendienste ermöglichen es Benutzern, Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="2df9f-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="2df9f-118">Zur Unterstützung der programmgesteuerten Konfiguration muss Ihre Nachrichtendienst-Einstiegspunktfunktion ohne Benutzereingriff arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="2df9f-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="2df9f-119">Wenn der Nachrichtendienst vom Profil-Assistenten aufgerufen werden kann, müssen Sie die programmgesteuerte Konfiguration unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2df9f-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="2df9f-120">Wenn sich der Nachrichtendienst nicht mit dem Profil-Assistenten konfigurieren lässt, können Sie auswählen, ob die programmgesteuerte Konfiguration unterstützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2df9f-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="2df9f-121">Weitere Informationen zur Unterstützung der Konfiguration in einer Einstiegspunktfunktion für den Nachrichtendienst finden Sie unter [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="2df9f-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="2df9f-122">Veröffentlichen Sie den Namen der Einstiegspunktfunktion des Nachrichtendiensts in der Konfigurationsdatei MAPISVC. inf, indem Sie den folgenden Eintrag im Abschnitt Nachrichtendienst einschließen:</span><span class="sxs-lookup"><span data-stu-id="2df9f-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="2df9f-123">Erstellen Sie ein oder mehrere Eigenschaftenblatt-Dialogfelder zum Anzeigen von Konfigurationsdaten.</span><span class="sxs-lookup"><span data-stu-id="2df9f-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="2df9f-124">Führen Sie die folgenden Aufgaben aus, wenn Sie zulassen möchten, dass der Profil-Assistent Ihren Nachrichtendienst konfiguriert:</span><span class="sxs-lookup"><span data-stu-id="2df9f-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="2df9f-125">Implementieren Sie eine Einstiegspunktfunktion, die dem [WIZARDENTRY](wizardentry.md) -Prototyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="2df9f-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="2df9f-126">Implementieren Sie eine Windows-Standarddialogfeld-Prozedur, die dem [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) -Prototyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="2df9f-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="2df9f-127">Verbessern Sie die Einstiegspunktfunktion Ihres Nachrichtendiensts, um auf zusätzliche Ereignisse zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="2df9f-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2df9f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2df9f-128">See also</span></span>

- [<span data-ttu-id="2df9f-129">Nachrichtendienst Implementierung</span><span class="sxs-lookup"><span data-stu-id="2df9f-129">Message Service Implementation</span></span>](message-service-implementation.md)

