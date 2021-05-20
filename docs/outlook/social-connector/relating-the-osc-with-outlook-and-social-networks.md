---
title: Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Der Outlook Social Connector (OSC) kann in der Office-Visitenkarte und Outlook-Personenbereich-Aktivitäten, Status- oder Fotoupdates für einen Kollegen, Freund oder eine person angezeigt werden, der Sie zugeordnet sind.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428011"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="6cfab-103">Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken</span><span class="sxs-lookup"><span data-stu-id="6cfab-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="6cfab-104">Der Outlook Social Connector (OSC) kann in der Office-Visitenkarte und Outlook-Personenbereich-Aktivitäten, Status- oder Fotoupdates für einen Kollegen, Freund oder eine person angezeigt werden, der Sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6cfab-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="6cfab-105">Standardmäßig zeigt das Betriebssystem die Outlook E-Mails, Anlagen und Besprechungsanfragen an, die von einer ausgewählten Person empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="6cfab-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="6cfab-106">Wenn die ausgewählte Person und der Office benutzer an einer SharePoint-Website zusammenarbeiten, zeigt das OsC auch Dokumentaktualisierungen und andere Websiteaktivitäten von dieser SharePoint an.</span><span class="sxs-lookup"><span data-stu-id="6cfab-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="6cfab-107">Abhängig von den Kontexten der Zuordnung, die der Office-Benutzer interessiert, kann der Office-Benutzer OSC-Anbieter für Geschäftsanwendungen, interne Unternehmenswebsites oder eine Vielzahl von professionellen und sozialen Netzwerkwebsites wie LinkedIn, Facebook und Windows Live installieren.</span><span class="sxs-lookup"><span data-stu-id="6cfab-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="6cfab-108">Um die Freigabe von Funktionen Office Clientanwendungen zu unterstützen, wird das OSC-Kernmodul als Teil einer freigegebenen Office-Komponente implementiert, und der Personenbereich wird als Outlook-Add-In implementiert.</span><span class="sxs-lookup"><span data-stu-id="6cfab-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="6cfab-109">Für die Verwendung des OSC muss ein Office-Benutzer Outlook auf diesem Clientcomputer installiert und Outlook mit einem Profil konfiguriert haben, damit das OSC Kontakte in einem Ordner Kontakte zwischenspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="6cfab-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="6cfab-110">Ein OSC-Anbieter ist eine COM-DLL (Component Object Model), mit der das OSC unabhängig von den APIs der einzelnen sozialen Netzwerke auf Daten in sozialen Netzwerken zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="6cfab-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="6cfab-111">Eine OSC-Anbieter-DLL muss lokal auf einem Clientcomputer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="6cfab-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="6cfab-112">Der OsC-Anbieter eines sozialen Netzwerks verbindet das OSC, das Teil von Outlook ist, mit dem sozialen Netzwerk im Internet.</span><span class="sxs-lookup"><span data-stu-id="6cfab-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="6cfab-113">Ein OSC-Anbieter muss eine Reihe von Schnittstellen implementieren, die als Teil der Erweiterbarkeit des OSC-Anbieters definiert sind, um mit dem OSC zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="6cfab-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="6cfab-114">Die Erweiterbarkeit des OSC-Anbieters ist als offene Plattform verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cfab-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="6cfab-115">Die Anbieterarchitektur des OSC ermöglicht es mehreren Anbietern, mit dem OSC-Kernmodul zu arbeiten und soziale Informationen wie Freunde und Aktivitäten zu aggregieren.</span><span class="sxs-lookup"><span data-stu-id="6cfab-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="6cfab-116">Abbildung 1 veranschaulicht die Architektur des OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="6cfab-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="6cfab-117">**Abbildung 1. Outlook Architektur des Anbieters für sozialen Connector**</span><span class="sxs-lookup"><span data-stu-id="6cfab-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Soziale Netzwerke, OSC-Provider, OSC und Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="6cfab-119">Begrifflichkeiten</span><span class="sxs-lookup"><span data-stu-id="6cfab-119">Terminology</span></span>

<span data-ttu-id="6cfab-120">In diesem Outlook Social Connector Provider Reference wird ein soziales Netzwerk verwendet, um auf die folgenden Arten von Websites zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="6cfab-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="6cfab-121">Zusammenarbeitswebsites wie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6cfab-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="6cfab-122">Websites für soziale Netzwerke wie Facebook und Windows Live.</span><span class="sxs-lookup"><span data-stu-id="6cfab-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="6cfab-123">Professional Netzwerkstandorte wie LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="6cfab-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="6cfab-124">Andere Geschäftsanwendungen oder unternehmensinterne Websites, die für Netzwerke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6cfab-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="6cfab-125">Der Begriff "Freund" wird im Allgemeinen verwendet, um Freunde, Familie, Kollegen, Verbindungen und alle anderen Personen, mit der ein Office-Benutzer in einem kollaborativen Kontext wie SharePoint verknüpft ist oder dem Konto des Benutzers für soziale Netzwerke hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6cfab-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="6cfab-126">Nicht-Freunde sind Personen, auf die in den Aktivitätsupdates von Freunden verwiesen wird, aber keine Freunde, die dem Konto Office sozialen Netzwerk des Benutzers hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="6cfab-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="6cfab-127">Kontakte sind Personen in einem Outlook Kontaktordner.</span><span class="sxs-lookup"><span data-stu-id="6cfab-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6cfab-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cfab-128">See also</span></span>

- [<span data-ttu-id="6cfab-129">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="6cfab-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

