---
title: Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Der Outlook Connector für soziale Netzwerke (OSC) kann in der Office-VisitenKarte und im Outlook-Personen Bereich Aktivitäten, Status oder Foto Updates für einen Kollegen, eine Freundin oder eine beliebige Person, der Sie zugeordnet sind, anzeigen.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329257"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="f6a4a-103">Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken</span><span class="sxs-lookup"><span data-stu-id="f6a4a-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="f6a4a-104">Der Outlook Connector für soziale Netzwerke (OSC) kann in der Office-VisitenKarte und im Outlook-Personen Bereich Aktivitäten, Status oder Foto Updates für einen Kollegen, eine Freundin oder eine beliebige Person, der Sie zugeordnet sind, anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="f6a4a-105">Standardmäßig zeigt OSC die Outlook-e-Mails, Anlagen und Besprechungsanfragen an, die von einer ausgewählten Person empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="f6a4a-106">Wenn die ausgewählte Person und der Office-Benutzer an einer SharePoint-Website zusammenarbeiten, zeigt der OSC auch Dokumentaktualisierungen und andere Websiteaktivitäten von dieser SharePoint-Website an.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="f6a4a-107">Je nach den Kontexten, an denen der Office-Benutzer interessiert ist, kann der Office-Benutzer OSC-Anbieter für Branchenanwendungen, interne Unternehmenswebsites oder eine Vielzahl von Websites mit professionellen und sozialen Netzwerken wie LinkedIn installieren. Facebook und Windows Live.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="f6a4a-108">Zur Unterstützung der Freigabe von Funktionen in Office-Clientanwendungen wird das OSC-Kern Modul als Teil einer gemeinsam genutzten Office-Komponente implementiert, und der Personen Bereich wird als Outlook-Add-in implementiert.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="f6a4a-109">Um den OSC zu verwenden, muss ein Office-Benutzer Outlook auf diesem Clientcomputer installiert und Outlook mit einem Profil konfiguriert haben, damit OSC Kontakte in einem Kontakteordner zwischenspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="f6a4a-110">Ein OSC-Anbieter ist eine COM-DLL (Component Object Model), die es dem OSC ermöglicht, auf soziale Netzwerkdaten auf eine Art und Weise zuzugreifen, die unabhängig von den APIs der einzelnen sozialen Netzwerke ist.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="f6a4a-111">Eine OSC-Anbieter-DLL muss lokal auf einem Clientcomputer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="f6a4a-112">OSC-Anbieter eines sozialen Netzwerks verbindet den OSC, der Teil von Outlook ist, mit dem sozialen Netzwerk im Internet.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="f6a4a-113">Ein OSC-Anbieter muss eine Reihe von Schnittstellen implementieren, die als Teil der OSC-Anbieter Erweiterbarkeit für die Kommunikation mit dem OSC definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="f6a4a-114">OSC-Anbieter Erweiterbarkeit ist als offene Plattform verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="f6a4a-115">Die Anbieter Architektur des OSC ermöglicht es mehreren Anbietern, mit dem OSC-Kern Modul zu arbeiten und soziale Informationen wie Freunde und Aktivitäten zu aggregieren.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="f6a4a-116">Abbildung 1 zeigt die OSC-Anbieter Architektur.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="f6a4a-117">**Abbildung 1. Architektur des Outlook Social Connector-Anbieters**</span><span class="sxs-lookup"><span data-stu-id="f6a4a-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Soziale Netzwerke, OSC-Provider, OSC und Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="f6a4a-119">Terminologie</span><span class="sxs-lookup"><span data-stu-id="f6a4a-119">Terminology</span></span>

<span data-ttu-id="f6a4a-120">In dieser Outlook Social Connector-Anbieter Referenz wird ein soziales Netzwerk verwendet, um auf die folgenden Websitetypen zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="f6a4a-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="f6a4a-121">Gemeinsame Websites wie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="f6a4a-122">Websites für soziale Netzwerke wie Facebook und Windows Live.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="f6a4a-123">Professionelle Netzwerk Websites wie LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="f6a4a-124">Andere Branchenanwendungen oder unternehmensinterne Websites, die für Netzwerke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="f6a4a-125">Der Begriff Friend wird im Allgemeinen verwendet, um Freunde, Familie, Kollegen, Verbindungen und alle anderen Personen, denen ein Office-Benutzer in einem kollaborativen Kontext wie SharePoint zugeordnet ist, oder das soziale Netzwerkkonto des Benutzers hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="f6a4a-126">Nicht-Freunde sind Personen, auf die in den Aktivitäts Updates von Freunden verwiesen wird, aber keine Freunde, die dem sozialen Netzwerkkonto des Office-Benutzers hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="f6a4a-127">Kontakte sind Personen in einem Outlook-Kontaktordner.</span><span class="sxs-lookup"><span data-stu-id="f6a4a-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6a4a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6a4a-128">See also</span></span>

- [<span data-ttu-id="f6a4a-129">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="f6a4a-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

