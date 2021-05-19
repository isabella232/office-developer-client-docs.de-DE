---
title: QuickSteps zum Entwickeln eines Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: In diesem Thema werden einige Schritte zum Entwickeln eines Outlook Social Connector (OSC) vorgeschlagen.
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424217"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="c1db3-103">QuickSteps zum Entwickeln eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="c1db3-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="c1db3-104">Zum Entwickeln eines OSC-Anbieters müssen Sie die folgenden allgemeinen Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c1db3-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="c1db3-105">Implementieren Sie die vier obligatorischen Schnittstellen: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)und [ISocialPerson](isocialpersoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c1db3-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="c1db3-106">Abhängig von der Unterstützung Ihres sozialen Netzwerks für das Zwischenspeichern von Anmeldeinformationen, das Folgen einer Person im sozialen Netzwerk oder die dynamische Synchronisierung von Freunden und ihren Aktivitäten sollten Sie die [ISocialSession2-Schnittstelle](isocialsession2iunknown.md) implementieren.</span><span class="sxs-lookup"><span data-stu-id="c1db3-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="c1db3-107">Testen und debuggen Sie parallel zur Implementierung von Schnittstellen den OSC-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c1db3-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="c1db3-108">Bereitstellen des OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="c1db3-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="c1db3-109">Durchführen der letzten Tests vor der Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="c1db3-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="c1db3-110">Schritt A: Implementieren von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c1db3-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="c1db3-111">Ein OSC-Anbieter implementiert Schnittstellen, damit das OSC diese Schnittstellen verwenden kann, um über den OSC-Anbieter erforderliche Informationen über oder aus dem sozialen Netzwerk zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c1db3-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="c1db3-112">Diese Informationen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c1db3-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="c1db3-113">So stellen Sie einem Benutzer das Anmeldedialogfeld des Kontos vor.</span><span class="sxs-lookup"><span data-stu-id="c1db3-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="c1db3-114">Gibt an, ob der Anbieter die Anzeige von Freunden oder Aktivitäten unterstützt, die im sozialen Netzwerk angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c1db3-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="c1db3-115">Anzeigen von Freunden und Aktivitäten in der Visitenkarte oder Outlook Personenbereich.</span><span class="sxs-lookup"><span data-stu-id="c1db3-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="c1db3-116">Informationen zum Aktualisieren von Freunden oder Aktivitäten auf der Visitenkarte oder im Personenbereich.</span><span class="sxs-lookup"><span data-stu-id="c1db3-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="c1db3-117">Die Informationen werden in der Regel vom Anbieter an die OSC in Form von XML-Zeichenfolgen als Ausgabeparameter von Schnittstellenmethoden übergeben.</span><span class="sxs-lookup"><span data-stu-id="c1db3-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="c1db3-118">Sowohl der OSC als auch ein OSC-Anbieter entsprechen dem XML-Schema des OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="c1db3-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="c1db3-119">Daher benötigen Sie bei der Implementierung der Schnittstellen ein gutes Verständnis dafür, wie Das XML-Schema es Ihnen ermöglicht, Informationen wie oben aufgeführt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c1db3-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="c1db3-120">In den folgenden Ressourcen wird erläutert, wie Sie XML für Anbieterfunktionen, Freunde und Aktivitäten angeben:</span><span class="sxs-lookup"><span data-stu-id="c1db3-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="c1db3-121">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="c1db3-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="c1db3-122">Synchronisieren von Freunden und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="c1db3-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="c1db3-123">Capabilities XML(Beispiel)</span><span class="sxs-lookup"><span data-stu-id="c1db3-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="c1db3-124">XML für Funktionen</span><span class="sxs-lookup"><span data-stu-id="c1db3-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="c1db3-125">Friends-XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="c1db3-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="c1db3-126">XML für Freunde</span><span class="sxs-lookup"><span data-stu-id="c1db3-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="c1db3-127">Beispiel für Aktivitätsfeed-XML</span><span class="sxs-lookup"><span data-stu-id="c1db3-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="c1db3-128">XML für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="c1db3-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="c1db3-129">Bevor Sie mit der Implementierung beginnen, lesen Sie auch die folgenden Themen, um Später im Debugprozess Zeit zu sparen:</span><span class="sxs-lookup"><span data-stu-id="c1db3-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="c1db3-130">Technische Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1db3-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="c1db3-131">Bewährte Methoden für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="c1db3-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="c1db3-132">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="c1db3-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="c1db3-133">Schritt B: Debuggen</span><span class="sxs-lookup"><span data-stu-id="c1db3-133">Step B: Debugging</span></span>

<span data-ttu-id="c1db3-134">Im Thema [Debuggen eines Anbieters](debugging-a-provider.md) werden Debugverfahren vorgeschlagen, die Sie bei der Entwicklung eines OSC-Anbieters verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c1db3-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="c1db3-135">Während Der Entwicklung können Sie sich auch auf [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) beziehen, um sich ein besseres Verständnis des erwarteten Verhaltens in bestimmten Szenarien (z. B. einfache und formularbasierte Authentifizierung) zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="c1db3-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="c1db3-136">Schritt C: Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="c1db3-136">Step C: Deploying</span></span>

<span data-ttu-id="c1db3-137">Weitere Informationen zu Bereitstellungsanforderungen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c1db3-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="c1db3-138">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="c1db3-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="c1db3-139">Registrieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="c1db3-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="c1db3-140">Prüfliste für die Installation</span><span class="sxs-lookup"><span data-stu-id="c1db3-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="c1db3-141">Schritt D: Abschließende Tests vor der Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="c1db3-141">Step D: Final testing before release</span></span>

<span data-ttu-id="c1db3-142">Abhängig von Ihrem sozialen Netzwerk und dem OSC-Anbieter gibt es in der Regel anbieterspezifische Tests, die Sie vor der Veröffentlichung Ihres Anbieters durchführen sollten.</span><span class="sxs-lookup"><span data-stu-id="c1db3-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="c1db3-143">Eine vorgeschlagene Liste der Tests finden Sie unter [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c1db3-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1db3-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1db3-144">See also</span></span>

- [<span data-ttu-id="c1db3-145">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="c1db3-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

