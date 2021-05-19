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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418995"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="ff8e3-103">Unterstützen der Nachrichtendienstkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ff8e3-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="ff8e3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff8e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff8e3-105">Verwenden Sie das folgende Verfahren, um die Konfiguration des Nachrichtendiensts zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="ff8e3-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="ff8e3-106">Implementieren Sie eine Einstiegspunktfunktion, die dem [MSGSERVICEENTRY-Prototyp](msgserviceentry.md) entspricht.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="ff8e3-107">Nachrichtendienst-Einstiegspunktfunktionen verwalten den Zugriff auf Konfigurationsdaten und werden unter den folgenden Umständen aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="ff8e3-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="ff8e3-108">Wenn sich ein Client anmeldet, um Informationen zum Konfigurieren des Nachrichtendiensts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="ff8e3-109">Wenn ein Client eine Konfigurationseigenschaft anzeigen oder ändern möchte.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="ff8e3-110">Obwohl die meisten Nachrichtendienste Einstiegspunktfunktionen bereitstellen, sind diese Funktionen nicht unbedingt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="ff8e3-111">Nachrichtendienste können auf andere Weise Zugriff auf Konfigurationsdaten bieten.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="ff8e3-112">Durch die Verwendung einer Einstiegspunktfunktion wird jedoch der Konfigurationsprozess standardisiert und vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="ff8e3-113">MAPI erwartet, dass alle Nachrichtendienst-Einstiegspunktfunktionen Eigenschaften aus den Profilabschnitten speichern und abrufen können, die ihrem Nachrichtendienst zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="ff8e3-114">Sie können diese Funktionalität interaktiv, programmgesteuert oder sowohl interaktiv als auch programmgesteuert unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="ff8e3-115">Um die interaktive Konfiguration zu unterstützen, stellen Sie ein Eigenschaftenblatt zur Verfügung, das die Eigenschaften anzeigt, die beim Konfigurieren des Nachrichtendiensts beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="ff8e3-116">Optional können Sie auch Eigenschaftenblätter für jeden konfigurierbaren Anbieter liefern.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="ff8e3-117">Einige Nachrichtendienste beschränken Benutzer auf eine schreibgeschützte Ansicht von Konfigurationseigenschaften. Mit anderen Nachrichtendiensten können Benutzer Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="ff8e3-118">Um die programmgesteuerte Konfiguration zu unterstützen, muss ihre Nachrichtendienst-Einstiegspunktfunktion ohne Benutzereingriff funktionieren können.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="ff8e3-119">Wenn Ihr Nachrichtendienst vom Profil-Assistenten aufgerufen werden kann, müssen Sie die programmgesteuerte Konfiguration unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="ff8e3-120">Wenn ihr Nachrichtendienst sich nicht mithilfe des Profil-Assistenten konfigurieren lässt, können Sie auswählen, ob die programmgesteuerte Konfiguration unterstützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="ff8e3-121">Weitere Informationen zur Unterstützung der Konfiguration in einer Nachrichtendienst-Einstiegspunktfunktion finden Sie unter [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="ff8e3-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="ff8e3-122">Veröffentlichen Sie den Namen ihrer Nachrichtendienst-Einstiegspunktfunktion in der Konfigurationsdatei Mapisvc.inf, indem Sie den folgenden Eintrag im Abschnitt Nachrichtendienst hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="ff8e3-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="ff8e3-123">Erstellen Sie ein oder mehrere Eigenschaftenblattdialogfelder zum Anzeigen von Konfigurationsdaten.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="ff8e3-124">Führen Sie die folgenden Aufgaben aus, wenn Sie dem Profil-Assistenten die Konfiguration des Nachrichtendiensts ermöglichen möchten:</span><span class="sxs-lookup"><span data-stu-id="ff8e3-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="ff8e3-125">Implementieren Sie eine Einstiegspunktfunktion, die dem [WIZARDENTRY-Prototyp](wizardentry.md) entspricht.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="ff8e3-126">Implementieren Sie eine Windows- und Standarddialogfeldprozedur, die dem [SERVICEWIZARDDLGPROC-Prototyp](servicewizarddlgproc.md) entspricht.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="ff8e3-127">Erweitern Sie die Einstiegspunktfunktion des Nachrichtendiensts, um auf zusätzliche Ereignisse zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="ff8e3-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff8e3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff8e3-128">See also</span></span>

- [<span data-ttu-id="ff8e3-129">Implementierung des Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="ff8e3-129">Message Service Implementation</span></span>](message-service-implementation.md)

