---
title: QuickSteps für Informationen zum Entwickeln eines Providers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: In diesem Thema werden einige Schritte erfahren Sie mehr über das Entwickeln eines Providers Outlook Social Connector (OSC).
ms.openlocfilehash: 345e8600c704504be091ee23c66b7f85575cde90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796081"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="b4a6b-103">QuickSteps für Informationen zum Entwickeln eines Providers</span><span class="sxs-lookup"><span data-stu-id="b4a6b-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="b4a6b-104">Um einen OSC-Anbieter zu entwickeln, müssen Sie die folgenden allgemeinen Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="b4a6b-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="b4a6b-105">Die vier obligatorischen Schnittstellen implementieren: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)und [ISocialPerson](isocialpersoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="b4a6b-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="b4a6b-106">Je nach Ihrem sozialen Netzwerk-Unterstützung für das Zwischenspeichern von Anmeldeinformationen, die nach einer Person für das soziale Netzwerk oder dynamisch synchronisieren Freunde und deren Aktivitäten möchten Sie möglicherweise die [ISocialSession2](isocialsession2iunknown.md) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="b4a6b-107">Parallel mit Schnittstellen implementieren testen und Debuggen des OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="b4a6b-108">Bereitstellen des OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="b4a6b-109">Führen Sie die endgültige Tests vor der Freigabe.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="b4a6b-110">Schritt A: Implementieren von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b4a6b-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="b4a6b-111">Ein OSC-Anbieter implementiert Schnittstellen, damit die OSC diese Schnittstellen verwenden kann, um die erforderlichen Informationen zu oder aus dem sozialen Netzwerk, über den OSC-Anbieter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="b4a6b-112">Dazu gehören folgende:</span><span class="sxs-lookup"><span data-stu-id="b4a6b-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="b4a6b-113">Wie Sie im Anmeldedialogfeld Konto für einen Benutzer darstellen.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="b4a6b-114">Gibt an, ob der Anbieter mit Freunde oder Aktivitäten unterstützt wie auf dem sozialen Netzwerk angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="b4a6b-115">Wie in der Visitenkarte oder Outlook Personenbereich Freunde und Aktivitäten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="b4a6b-116">Wann Freunde oder Aktivitäten Informationen auf der Visitenkarte oder Personenbereich zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="b4a6b-117">Die Informationen wird an die OSC in Form von XML-Zeichenfolgen als Output-Parameter von Schnittstellenmethoden in der Regel vom Anbieter übergeben.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="b4a6b-118">Die OSC und einem OSC-Anbieter werden mit dem OSC-Anbieter XML-Schema entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="b4a6b-119">Im Rahmen die Schnittstellen implementieren, benötigen Sie daher verstehen, wie das XML-Schema Sie Informationen angeben, wie oben aufgelisteten können.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="b4a6b-120">Die folgenden Ressourcen wird erläutert, wie XML für Anbieterfunktionen für, Freunde und Aktivitäten angeben:</span><span class="sxs-lookup"><span data-stu-id="b4a6b-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="b4a6b-121">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="b4a6b-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="b4a6b-122">Synchronisieren von Freunde und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="b4a6b-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="b4a6b-123">Funktionen XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b4a6b-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="b4a6b-124">XML-Code für Funktionen</span><span class="sxs-lookup"><span data-stu-id="b4a6b-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="b4a6b-125">Freunde XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b4a6b-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="b4a6b-126">XML-Code für Freunde</span><span class="sxs-lookup"><span data-stu-id="b4a6b-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="b4a6b-127">Beispiel für eine Aktivität Feed XML</span><span class="sxs-lookup"><span data-stu-id="b4a6b-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="b4a6b-128">XML-Code für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="b4a6b-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="b4a6b-129">Bevor Sie die Implementierung starten, finden Sie auch in den folgenden Themen Zeit zu sparen Sie weiter unten in den Debugvorgang:</span><span class="sxs-lookup"><span data-stu-id="b4a6b-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="b4a6b-130">Technische Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4a6b-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="b4a6b-131">Bewährte Methoden für das Entwickeln eines Providers</span><span class="sxs-lookup"><span data-stu-id="b4a6b-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="b4a6b-132">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="b4a6b-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="b4a6b-133">Schritt B: Debuggen</span><span class="sxs-lookup"><span data-stu-id="b4a6b-133">Step B: Debugging</span></span>

<span data-ttu-id="b4a6b-134">Das Thema schlägt [Debuggen eines Providers](debugging-a-provider.md) Debuggen von Prozeduren, die Sie beim Entwickeln eines OSC-Providers verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="b4a6b-135">Während Sie entwickeln, finden Sie auch auf [Erste bereit OSC-Providers](getting-ready-to-release-an-osc-provider.md) für ein besseres Verständnis der das erwartete Verhalten in bestimmten Szenarien (z. B. grundlegende und formularbasierte Authentifizierung) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="b4a6b-136">Schritt C: Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="b4a6b-136">Step C: Deploying</span></span>

<span data-ttu-id="b4a6b-137">Finden Sie unter den folgenden Themen Informationen zu Anforderungen für die Bereitstellung zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b4a6b-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="b4a6b-138">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="b4a6b-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="b4a6b-139">Registrieren eines Providers</span><span class="sxs-lookup"><span data-stu-id="b4a6b-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="b4a6b-140">Checkliste für Installation</span><span class="sxs-lookup"><span data-stu-id="b4a6b-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="b4a6b-141">Schritt D: Final Tests vor der Freigabe</span><span class="sxs-lookup"><span data-stu-id="b4a6b-141">Step D: Final testing before release</span></span>

<span data-ttu-id="b4a6b-142">Je nach Ihrem sozialen Netzwerk und die OSC-Anbieter stehen in der Regel anbieterspezifische Tests aus, die Sie ausführen sollten, bevor Sie vom Dienstanbieter freigeben.</span><span class="sxs-lookup"><span data-stu-id="b4a6b-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="b4a6b-143">Eine Liste mit vorgeschlagenen von Tests finden Sie unter [Erste bereit OSC-Providers](getting-ready-to-release-an-osc-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b4a6b-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b4a6b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4a6b-144">See also</span></span>

- [<span data-ttu-id="b4a6b-145">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="b4a6b-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

