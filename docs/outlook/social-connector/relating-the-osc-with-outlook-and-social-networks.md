---
title: Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) können in die Office-Visitenkarte und Outlook Personenbereich Aktivitäten, Status oder Foto Updates anzeigen, für einen Kollegen, Friend oder Personen, denen Sie zugeordnet sind.
ms.openlocfilehash: 6dc6221b89eca5303e7cf6a201927659d4ac9107
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796085"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="fad54-103">Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken</span><span class="sxs-lookup"><span data-stu-id="fad54-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="fad54-104">Outlook Social Connector (OSC) können in die Office-Visitenkarte und Outlook Personenbereich Aktivitäten, Status oder Foto Updates anzeigen, für einen Kollegen, Friend oder Personen, denen Sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fad54-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="fad54-105">In der Standardeinstellung der OSC zeigt die Outlook-e-Mails, Anlagen, und Besprechungsanfragen von eine ausgewählte Person erhalten.</span><span class="sxs-lookup"><span data-stu-id="fad54-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="fad54-106">Wenn die ausgewählte Person und der Office-Benutzer auf einer SharePoint-Website arbeiten, zeigt die OSC auch Dokument Updates und andere Website Aktivitäten aus dieser SharePoint-Website.</span><span class="sxs-lookup"><span data-stu-id="fad54-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="fad54-107">Je nach dem Kontext der Zuordnung, die der Benutzer Office interessiert ist, kann der Benutzer Office OSC-Anbieter für Line-of-Business Applications, interne Unternehmenswebsites oder eine Vielzahl von professional und sozialen Netzwerk-Websites, wie beispielsweise LinkedIn installieren, Facebook und Windows Live.</span><span class="sxs-lookup"><span data-stu-id="fad54-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="fad54-108">Zur Unterstützung der Freigabe von der Funktionalität der Office-Clientanwendungen OSC zentralen Modul als Teil eines gemeinsam genutzte Office-Komponente implementiert ist, und den Personenbereich als Outlook-add-in implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="fad54-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="fad54-109">Für die Verwendung der OSC muss Benutzer in einem Office-Version von Outlook auf dem Clientcomputer und Outlook mit einem Profil so konfiguriert, dass die OSC-Kontakte im Kontakteordner cache kann haben.</span><span class="sxs-lookup"><span data-stu-id="fad54-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="fad54-110">Ein OSC-Provider ist eine DLL-Datei, mit der die OSC für soziale Netzwerke Zugriff auf Daten in eine Möglichkeit, die unabhängig von den einzelnen sozialen Netzwerk-APIs kann, Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="fad54-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="fad54-111">Ein OSC-Anbieter-DLL muss lokal auf einem Clientcomputer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="fad54-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="fad54-112">Ein social Network OSC-Anbieter verbindet das osc bilden, die Bestandteil von Outlook ist, mit dem sozialen Netzwerk im Internet.</span><span class="sxs-lookup"><span data-stu-id="fad54-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="fad54-113">Ein OSC-Anbieter muss eine Reihe von Schnittstellen, die als Teil der Erweiterbarkeit des OSC-Anbieter, Kommunikation mit dem OSC definiert implementieren.</span><span class="sxs-lookup"><span data-stu-id="fad54-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="fad54-114">Erweiterbarkeit des OSC-Providers ist als eine offene Plattform verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fad54-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="fad54-115">Die Architektur der die OSC kann mehrere Anbieter zum Arbeiten mit dem OSC zentralen Modul und aggregierte für soziale Netzwerke Informationen wie Freunde und Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="fad54-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="fad54-116">Abbildung 1 zeigt die Architektur der OSC-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="fad54-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="fad54-117">**Abbildung 1. Outlook Connector für soziale Netzwerke-Architektur**</span><span class="sxs-lookup"><span data-stu-id="fad54-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Soziale Netzwerke, OSC-Provider, OSC und Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="fad54-119">Terminologie</span><span class="sxs-lookup"><span data-stu-id="fad54-119">Terminology</span></span>

<span data-ttu-id="fad54-120">In dieser Outlook Social Connector Provider Referenz wird ein social Network verweisen auf die folgenden Arten von Websites verwendet:</span><span class="sxs-lookup"><span data-stu-id="fad54-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="fad54-121">Zusammenarbeit wie SharePoint-Websites.</span><span class="sxs-lookup"><span data-stu-id="fad54-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="fad54-122">-Websites für soziale Netzwerke wie Facebook und Windows Live.</span><span class="sxs-lookup"><span data-stu-id="fad54-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="fad54-123">Professional Netzwerkstandorten wie LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="fad54-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="fad54-124">Andere Line-of-Business Applications oder interne Unternehmenswebsites für Netzwerke verwendet.</span><span class="sxs-lookup"><span data-stu-id="fad54-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="fad54-125">Der Begriff Friend wird im Allgemeinen umfassen Freunde, Familie, Kollegen, Verbindungen und anderer Benutzer ein Office-Benutzer in einem gemeinsamen Kontext wie SharePoint zugeordnet ist oder das Konto des Benutzers für soziale Netzwerke hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="fad54-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="fad54-126">Nicht-Freunde Personen in Freunde Aktivität Updates verwiesen werden jedoch nicht Freunde, die das Office Konto des Benutzers für soziale Netzwerke hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="fad54-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="fad54-127">Kontakte sind Personen in einer Outlook-Kontaktordner.</span><span class="sxs-lookup"><span data-stu-id="fad54-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fad54-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fad54-128">See also</span></span>

- [<span data-ttu-id="fad54-129">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="fad54-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

