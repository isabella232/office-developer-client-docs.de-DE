---
title: Für OSC typische Aufrufsequenzen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: In diesem Abschnitt werden die typischen Anruf Sequenzen für Outlook Social Connector (OSC) von Mitgliedern in den OSC-Erweiterbarkeitsschnittstellen beschrieben, die ein OSC-Anbieter implementiert.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413612"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="525b0-103">Für OSC typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="525b0-103">OSC typical calling sequences</span></span>

<span data-ttu-id="525b0-104">In diesem Abschnitt werden die typischen Anruf Sequenzen für Outlook Social Connector (OSC) von Mitgliedern in den OSC-Erweiterbarkeitsschnittstellen beschrieben, die ein OSC-Anbieter implementiert.</span><span class="sxs-lookup"><span data-stu-id="525b0-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="525b0-105">Die typischen Aufrufsequenzen veranschaulichen, wie und wann der OSC solche Schnittstellen und Methoden verwendet, damit Sie besser bestimmen können, wie Sie ein bestimmtes Element auf einer Anbieter Erweiterungsschnittstelle implementieren können.</span><span class="sxs-lookup"><span data-stu-id="525b0-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="525b0-106">Die tatsächliche Aufrufsequenz kann je nach den von der [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode zurückgegebenen Funktionen variieren.</span><span class="sxs-lookup"><span data-stu-id="525b0-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="525b0-107">Beispiele für Funktionen sind:</span><span class="sxs-lookup"><span data-stu-id="525b0-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="525b0-108">Anbieterunterstützung für das Abrufen, Zwischenspeichern oder dynamisches Nachschlagen von Freunden und Aktivitäten aus dem sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="525b0-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="525b0-109">Die Benutzeroberfläche, die vom OSC für die Benutzeranmeldung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="525b0-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="525b0-110">Der Authentifizierungstyp (beispielsweise die formularbasierte Authentifizierung), der vom OSC verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="525b0-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="525b0-111">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="525b0-111">In this section</span></span>

- <span data-ttu-id="525b0-112">[Standardauthentifizierung](basic-authentication.md): Beschreibt die typische Anruffolge des osc zur Unterstützung eines Office-Benutzers, der sich an einem sozialen Netzwerk anmeldet, wenn der osc-Anbieter die Standardauthentifizierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="525b0-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="525b0-113">[Formularbasierte Authentifizierung](forms-based-authentication.md): Beschreibt die typische Aufrufsequenz des osc zur Unterstützung eines Office-Benutzers, der sich bei einem sozialen Netzwerk anmeldet, wenn der osc-Anbieter die formularbasierte Authentifizierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="525b0-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="525b0-114">[Abrufen von Aktivitäten](getting-activities.md): Beschreibt die typische Aufrufsequenz des osc, um die Aktivitäten der Freunde des Office-Benutzers von einem sozialen Netzwerk zu synchronisieren, wenn der Netzwerk-osc-Anbieter die Synchronisierung von Aktivitäten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="525b0-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="525b0-115">[Informationen zu Freunden](getting-friends-information.md): Beschreibt die typische Anruf Sequenz des osc, um die Freundesliste des Office-Benutzers aus einem sozialen Netzwerk zu synchronisieren, wenn der osc-Anbieter für soziale Netzwerke die zwischengespeicherte Synchronisierung von Kontakten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="525b0-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="525b0-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="525b0-116">Reference</span></span>

- [<span data-ttu-id="525b0-117">Referenz zum Outlook Connector Provider für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="525b0-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="525b0-118">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="525b0-118">Related sections</span></span>

- [<span data-ttu-id="525b0-119">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="525b0-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="525b0-120">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="525b0-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="525b0-121">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="525b0-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="525b0-122">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="525b0-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="525b0-123">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="525b0-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="525b0-124">Bewährte Methoden für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="525b0-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="525b0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="525b0-125">See also</span></span>

- [<span data-ttu-id="525b0-126">XML für Funktionen</span><span class="sxs-lookup"><span data-stu-id="525b0-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

