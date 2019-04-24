---
title: Vorbereiten der Freigabe eines OSC-Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: In diesem Abschnitt werden Tests vorgeschlagen, die Sie vor der Freigabe des OSC-Anbieters (Outlook Social Connector) ausführen können.
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327153"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="a5fdd-103">Vorbereiten der Freigabe eines OSC-Anbieters</span><span class="sxs-lookup"><span data-stu-id="a5fdd-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="a5fdd-104">In diesem Abschnitt werden Tests vorgeschlagen, die Sie vor der Freigabe des OSC-Anbieters (Outlook Social Connector) ausführen können.</span><span class="sxs-lookup"><span data-stu-id="a5fdd-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="a5fdd-105">Sie können mit den Themen in diesem Abschnitt beginnen und einige dieser Tests während der Entwicklungs-und Testphase durchführen, aber Sie sollten diese Tests mit der Zeit abgeschlossen haben, die Sie freigeben.</span><span class="sxs-lookup"><span data-stu-id="a5fdd-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="a5fdd-106">Diese Tests überprüfen die grundlegenden Funktionen der Implementierung der OSC-Anbieterschnittstellen im Hinblick auf die Funktionen, die Sie für den OSC-Anbieter angeben.</span><span class="sxs-lookup"><span data-stu-id="a5fdd-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="a5fdd-107">Auch wenn OSC ein Feature ist, das von mehreren Office-Clientanwendungen gemeinsam verwendet wird, verwenden diese Tests Outlook als Client, um die grundlegenden Funktionen zu testen.</span><span class="sxs-lookup"><span data-stu-id="a5fdd-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="a5fdd-108">Sie sollten bestimmen, ob andere Tests für für Ihren anbieterspezifische Funktionen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a5fdd-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="a5fdd-109">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="a5fdd-109">In this section</span></span>

- <span data-ttu-id="a5fdd-110">[Testen der Bereitstellung](testing-deployment.md): Beschreibt Szenarien, die Sie bei der Installation und Deinstallation eines osc-Anbieters testen sollten.</span><span class="sxs-lookup"><span data-stu-id="a5fdd-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="a5fdd-111">[Testen von Funktionen, Authentifizierung und Konfiguration](testing-capabilities-authentication-and-configuration.md): Beschreibt Tests für das erhalten von Funktionen und Szenarios zum Konfigurieren eines Kontos und zum Authentifizieren eines Benutzers für ein soziales Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a5fdd-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="a5fdd-112">[TestIng folgende und Stop-folgende Personen](testing-following-and-stop-following-persons.md): Beschreibt Szenarien zum Testen des osc-Anbieters zum Hinzufügen einer Person als Freund oder zum Entfernen eines Freundes aus dem sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a5fdd-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="a5fdd-113">[Testen von Freunden](testing-friends.md): Beschreibt Tests und Szenarien, um zu überprüfen, ob der osc-Anbieter entsprechend der vom Anbieter unterstützten Synchronisierungsmodus Daten von Freunden und nicht-Freunden zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a5fdd-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="a5fdd-114">[Testaktivitäten](testing-activities.md): Beschreibt Tests und Szenarien, um zu überprüfen, ob der osc-Anbieter ordnungsgemäß Aktivitäten von Freunden und nicht-Freunden, je nach dem vom Anbieter unterstützten Synchronisierungsmodus, zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a5fdd-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="a5fdd-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="a5fdd-115">Reference</span></span>

- [<span data-ttu-id="a5fdd-116">Referenz zum Outlook Connector Provider für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="a5fdd-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="a5fdd-117">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="a5fdd-117">Related sections</span></span>

- [<span data-ttu-id="a5fdd-118">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="a5fdd-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="a5fdd-119">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="a5fdd-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="a5fdd-120">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="a5fdd-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="a5fdd-121">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="a5fdd-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="a5fdd-122">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="a5fdd-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

