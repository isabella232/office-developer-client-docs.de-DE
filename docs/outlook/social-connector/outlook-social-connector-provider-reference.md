---
title: Outlook Connector für soziale Netzwerke – Anbieterverweis
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: Der Outlook Connector für soziale Netzwerke 2013 bietet einen Hub für die private und berufliche Kommunikation.
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359836"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="e38bf-103">Outlook Connector für soziale Netzwerke – Anbieterverweis</span><span class="sxs-lookup"><span data-stu-id="e38bf-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="e38bf-104">Der Outlook Connector für soziale Netzwerke 2013 bietet einen Hub für die private und berufliche Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="e38bf-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="e38bf-105">Der Connector für soziale Netzwerke (OSC) arbeitet mit SharePoint Server, SharePoint Workspace, dem Lync-Client und allen Office-Clientanwendungen, die Anwesenheitsinformationen unterstützen und deren Kontaktkarten mit OSC kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="e38bf-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="e38bf-106">In Outlook beispielsweise können Benutzer nach der Auswahl eines Outlook-Elements, wie einer E-Mail oder Besprechungsanfrage, mit einem Klick auf den Sender oder Empfänger direkt im Personenbereich von Outlook Aktivitäten, Fotos und Statusaktualisierungen dieser Person in sozialen Netwerken ansehen.</span><span class="sxs-lookup"><span data-stu-id="e38bf-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="e38bf-107">Dort werden außerdem alle Outlook -E-Mails, Anhänge, und Besprechungen aus der Kontakthistorie mit dieser Person angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e38bf-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="e38bf-108">Im professionellen Bereich können Benutzer einer SharePoint-Website im Personenbereich auch Dokumentaktualisierungen und andere Websiteaktivitäten dieser Person sehen.</span><span class="sxs-lookup"><span data-stu-id="e38bf-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="e38bf-p103">Soziale Netzwerke können einen Anbieter für OSC entwickeln, um Aktualisierungen im sozialen Netzwerk mit kompatiblen Servern und Anwendungen zu synchronisieren. Beliebte soziale Netzwerke wie LinkedIn, Facebook und Windows Live bieten bereits solche Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="e38bf-p103">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications. Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="e38bf-111">In der Connector für soziale Netzwerke 2013-Anbieterreferenz wird erklärt, wie Sie einen OSC-Anbieter über die OSC-Anbietererweiterung entwickeln können.</span><span class="sxs-lookup"><span data-stu-id="e38bf-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="e38bf-112">Wenn Sie gerade erst mit dem Entwickeln von Lösungen für Outlook begonnen haben, finden Sie im Artikel [Auswählen einer API oder Technologie zum Entwickeln von Lösungen für Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) weitere Informationen zu den APIs und Technologien, die am besten zu Ihren Anforderungen passen.</span><span class="sxs-lookup"><span data-stu-id="e38bf-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="e38bf-113">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="e38bf-113">In this section</span></span>

- <span data-ttu-id="e38bf-114">[Erste Schritte bei der Entwicklung eines Outlook Connector für soziale Netzwerke-Anbieters](getting-started-with-developing-an-outlook-social-connector-provider.md): Enthält einen Überblick über OSC: Wozu Sie den Anbieter verwenden können, erste Schritte für die Entwicklung eines Anbieters, technische Voraussetzungen, Best Practices und Neuigkeiten in dieser Version.</span><span class="sxs-lookup"><span data-stu-id="e38bf-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="e38bf-115">[OSC-Beispielvorlagen](osc-sample-templates.md): In diesem Thema werden verschiedene Visual Studio-Vorlagen zur Entwicklung eines Anbieters beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e38bf-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="e38bf-116">[Typische Aufrufabfolgen des OSC](osc-typical-calling-sequences.md): In diesem Thema werden einige typische Aufrufabfolgen des OSC der Mitglieder der OSC-Anbietererweiterungsschnittstellen vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="e38bf-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="e38bf-117">Dies sollte Ihnen helfen, die Implementierung dieser Schnittstellen besser zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="e38bf-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="e38bf-118">[Entwickeln eines Anbieters mit dem OSC XML-Schema](developing-a-provider-with-the-osc-xml-schema.md): In diesem Thema wird beschrieben, wie ein OSC-Anbieter durch die OSC-Anwendungserweiterungsschnittstellen und das OSC XML-Schema unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e38bf-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="e38bf-119">[Debuggen eines Anbieters](debugging-a-provider.md): In diesem Thema werden mögliche Schritte zum Debuggen eines OSC-Anbieters vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="e38bf-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="e38bf-120">[Bereitstellen eines Anbieters](deploying-a-provider.md): In diesem Thema werden die Registrierungsvoraussetzungen für einen OSC-Anbieter beschrieben. Außerdem finden Sie hier eine Checkliste für die Installation eines Anbieters.</span><span class="sxs-lookup"><span data-stu-id="e38bf-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="e38bf-121">[Vorbereiten der Veröffentlichung eines OSC-Anbieters](getting-ready-to-release-an-osc-provider.md): Schlägt Tests vor, die Sie vor der Veröffentlichung eines OSC-Anbieters durchführen können.</span><span class="sxs-lookup"><span data-stu-id="e38bf-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="e38bf-122">[Outlook Connector für soziale Netzwerke – Anbieterverweis](outlook-social-connector-provider-reference-0.md): In diesem Thema finden Sie Referenzinformationen zu den OSC-Anbietererweiterungsschnittstellen, dem OSC XML-Schema und Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="e38bf-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e38bf-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e38bf-123">See also</span></span>

- [<span data-ttu-id="e38bf-124">Urheberrechtshinweis für Outlook Connector für soziale Netzwerke 2013 – Anbieterverweis</span><span class="sxs-lookup"><span data-stu-id="e38bf-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="e38bf-125">Konventionen für Office Developer-Dokumente</span><span class="sxs-lookup"><span data-stu-id="e38bf-125">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)   
- [<span data-ttu-id="e38bf-126">Barrierefreiheit in Microsoft-Produkten</span><span class="sxs-lookup"><span data-stu-id="e38bf-126">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)  
- [<span data-ttu-id="e38bf-127">Auszüge aus den Onlinedatenschutzbestimmungen von Microsoft</span><span class="sxs-lookup"><span data-stu-id="e38bf-127">Microsoft Online Privacy Notice</span></span>](https://privacy.microsoft.com/en-us/privacystatement)
    

