---
title: Vorbereiten eines OSC-Providers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: In diesem Abschnitt wird die Tests, die Sie ausführen können, bevor Sie Ihren Outlook Social Connector (OSC)-Anbieter freigeben.
ms.openlocfilehash: 5caf4144a8daed31d30c9ecbcf9cf21c2300ed8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795961"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="5e6f8-103">Vorbereiten eines OSC-Providers</span><span class="sxs-lookup"><span data-stu-id="5e6f8-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="5e6f8-104">In diesem Abschnitt wird die Tests, die Sie ausführen können, bevor Sie Ihren Outlook Social Connector (OSC)-Anbieter freigeben.</span><span class="sxs-lookup"><span data-stu-id="5e6f8-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="5e6f8-105">Können in Bezug auf die Themen in diesem Abschnitt starten und einige dieser Tests während der Entwicklungs- und Testphase Suchtool, aber Sie sollten diese Tests durch die Zeit, die Sie freigeben abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="5e6f8-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="5e6f8-106">Diese Tests überprüfen, ob die grundlegende Funktionen der Implementierung der OSC-Anbieter Schnittstellen in Bezug auf die Funktionen, die Sie für den OSC-Anbieter angeben.</span><span class="sxs-lookup"><span data-stu-id="5e6f8-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="5e6f8-107">Darüber hinaus, obwohl die OSC ein Feature von mehreren Office-Clientanwendungen gemeinsam genutzt wird, verwenden Sie diese Tests Outlook als Client zum Testen der grundlegenden Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="5e6f8-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="5e6f8-108">Sie sollten bestimmen, ob andere Tests an Ihren Anbieter für bestimmte Features erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5e6f8-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="5e6f8-109">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="5e6f8-109">In this section</span></span>

- <span data-ttu-id="5e6f8-110">[Testen der Bereitstellung](testing-deployment.md): Szenarien, die Sie für testen sollten, um die Installation und Deinstallation von einem OSC-Anbieter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5e6f8-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="5e6f8-111">[Testen der Funktionen, Authentifizierung und Konfiguration](testing-capabilities-authentication-and-configuration.md): werden die Tests für das Abrufen von Funktionen und Szenarien zum Konfigurieren eines Kontos und Authentifizieren eines Benutzers für ein social Network beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5e6f8-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="5e6f8-112">[In der folgenden Tests und Stop-folgenden Personen](testing-following-and-stop-following-persons.md): Beschreibt Szenarien zum Testen, ob der OSC-Anbieter, um eine Person als Freund hinzuzufügen oder um einen Freund aus dem sozialen Netzwerk zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5e6f8-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="5e6f8-113">[Testen der Freunde](testing-friends.md): Beschreibt Tests und Szenarien zu überprüfen, ob der OSC-Anbieter entsprechend Daten Freunde und nicht-Freunde, sofern zutreffend, je nach den Synchronisierungsmodus zurückgibt, die vom Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e6f8-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="5e6f8-114">[Testen von Aktivitäten](testing-activities.md): Beschreibt Tests und Szenarien zu überprüfen, ob der OSC-Anbieter entsprechend Aktivitäten Freunde und nicht-Freunde, sofern zutreffend, je nach den Synchronisierungsmodus zurückgibt, die vom Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e6f8-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="5e6f8-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="5e6f8-115">Reference</span></span>

- [<span data-ttu-id="5e6f8-116">Referenz zum Outlook Connector Provider für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="5e6f8-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="5e6f8-117">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="5e6f8-117">Related sections</span></span>

- [<span data-ttu-id="5e6f8-118">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="5e6f8-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="5e6f8-119">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="5e6f8-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="5e6f8-120">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="5e6f8-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="5e6f8-121">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="5e6f8-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="5e6f8-122">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="5e6f8-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

