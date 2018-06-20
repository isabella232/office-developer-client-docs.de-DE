---
title: OSC typisch aufrufenden Sequenzen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: Dieser Abschnitt beschreibt die typischen aufrufende Outlook Social Connector (OSC) Sequenzen der Elemente in die OSC-Anbieter Erweiterungsschnittstellen, die ein OSC-Anbieter implementiert.
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796074"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="b7538-103">OSC typisch aufrufenden Sequenzen</span><span class="sxs-lookup"><span data-stu-id="b7538-103">OSC typical calling sequences</span></span>

<span data-ttu-id="b7538-104">Dieser Abschnitt beschreibt die typischen aufrufende Outlook Social Connector (OSC) Sequenzen der Elemente in die OSC-Anbieter Erweiterungsschnittstellen, die ein OSC-Anbieter implementiert.</span><span class="sxs-lookup"><span data-stu-id="b7538-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="b7538-105">Die normalen aufrufenden Sequenzen veranschaulichen, wie und wann die OSC verwendet diese Schnittstellen und Methoden, mit der Sie eine bessere können bestimmen, wie einen bestimmten Member für einen Anbieter Erweiterbarkeitsschnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="b7538-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="b7538-106">Die tatsächliche aufrufende Sequenz kann je nach den Möglichkeiten, die von der [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode zurückgegebene variieren.</span><span class="sxs-lookup"><span data-stu-id="b7538-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="b7538-107">Die folgenden: Beispiele für Funktionen</span><span class="sxs-lookup"><span data-stu-id="b7538-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="b7538-108">Anbieter unterstützt für die erste, Zwischenspeichern oder dynamisch Nachschlagen Freunde und Aktivitäten aus dem sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="b7538-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="b7538-109">Die Benutzeroberfläche, die die OSC für die Benutzeranmeldung angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7538-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="b7538-110">Der Authentifizierungstyp (beispielsweise formularbasierte Authentifizierung), den die OSC verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7538-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="b7538-111">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="b7538-111">In this section</span></span>

- <span data-ttu-id="b7538-112">[Standardauthentifizierung](basic-authentication.md): Beschreibt die typische aufrufende Abfolge der die OSC unterstützen Sie einen Office-Benutzer, die mit einem sozialen Netzwerk angemeldet ist, wenn der OSC-Anbieter Standardauthentifizierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7538-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="b7538-113">[Formularbasierte Authentifizierung](forms-based-authentication.md): Beschreibt die typische aufrufende Abfolge der die OSC unterstützen Sie einen Office-Benutzer, die mit einem sozialen Netzwerk angemeldet ist, wenn der OSC-Anbieter formularbasierte Authentifizierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7538-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="b7538-114">[Erste Aktivitäten](getting-activities.md): Beschreibt die typische aufrufende Abfolge der die OSC zum Synchronisieren der Aktivitäten des Office-Benutzers Freunde aus einem sozialen Netzwerk, wenn der OSC-Anbieter für soziale Netzwerke Synchronisierung von Aktivitäten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7538-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="b7538-115">[Erste Freunde Informationen](getting-friends-information.md): Beschreibt die normale aufrufende Abfolge der die OSC Freunde-Liste der Office-Benutzer von einem sozialen Netzwerk, synchronisieren, wenn der OSC-Anbieter für soziale Netzwerke zwischengespeicherten Synchronisierung von Kontakten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7538-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="b7538-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="b7538-116">Reference</span></span>

- [<span data-ttu-id="b7538-117">Referenz zum Outlook Connector Provider für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="b7538-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="b7538-118">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="b7538-118">Related sections</span></span>

- [<span data-ttu-id="b7538-119">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="b7538-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="b7538-120">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="b7538-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="b7538-121">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="b7538-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="b7538-122">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="b7538-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="b7538-123">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="b7538-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="b7538-124">Bewährte Methoden für das Entwickeln eines Providers</span><span class="sxs-lookup"><span data-stu-id="b7538-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="b7538-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7538-125">See also</span></span>

- [<span data-ttu-id="b7538-126">XML-Code für Funktionen</span><span class="sxs-lookup"><span data-stu-id="b7538-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

