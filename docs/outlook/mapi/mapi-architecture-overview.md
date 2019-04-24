---
title: Übersicht über die MAPI-Architektur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 98a723528a714918ad7e0f10534efb0d38ef139a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297890"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="af9ff-103">Übersicht über die MAPI-Architektur</span><span class="sxs-lookup"><span data-stu-id="af9ff-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="af9ff-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af9ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af9ff-105">MAPI definiert eine modulare Architektur, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="af9ff-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="af9ff-106">![Architektur von Outlook 2010] (media/amapi_43.gif "Architektur von Outlook 2010")</span><span class="sxs-lookup"><span data-stu-id="af9ff-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="af9ff-107">Die MAPI-Anwendung wird als Clientanwendung bezeichnet, da es sich um einen Client des MAPI-Subsystems handelt.</span><span class="sxs-lookup"><span data-stu-id="af9ff-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="af9ff-108">Messaging-basierte Anwendungen beschäftigen Messaging als zentralen Teil ihrer Verarbeitung und bieten umfangreiche Messaging-Features wie den Austausch von Informationen verschiedener Typen in verschiedenen Formaten und die Möglichkeit, die Informationen lokal zu speichern und zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="af9ff-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="af9ff-109">E-Mail-, Scheduling-und Workflowanwendungen sind Beispiele für Messaging basierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="af9ff-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="af9ff-110">Das MAPI-Subsystem besteht aus einer allgemeinen Benutzeroberfläche und den Programmierschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="af9ff-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="af9ff-111">Bei der allgemeinen Benutzeroberfläche handelt es sich um eine Reihe von Dialogfeldern, mit denen Clientanwendungen konsistent aussehen und Benutzer eine konsistente Arbeitsweiseerhalten.</span><span class="sxs-lookup"><span data-stu-id="af9ff-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="af9ff-112">MAPI verfügt über Programmierschnittstellen, die vom MAPI-Subsystem, von Client Softwareentwicklern und von Dienstanbieter Entwicklern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af9ff-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="af9ff-113">Die MAPI-Programmierschnittstelle ist die Hauptobjekt basierte Programmierschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="af9ff-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="af9ff-114">Die MAPI-Programmierschnittstelle ähnelt dem OLE-Komponentenobjektmodell und wird vom MAPI-Subsystem und Messaging-basierten Clientanwendungen verwendet, die in C oder C++ geschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="af9ff-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="af9ff-115">Als Client Softwareentwickler führen Sie MAPI-Aufrufe direkt über die MAPI-Programmierschnittstelle aus.</span><span class="sxs-lookup"><span data-stu-id="af9ff-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="af9ff-116">Sie können Messaging mit einer einzelnen MAPI-Clientschnittstelle oder einer Kombination von Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="af9ff-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="af9ff-117">Eine einzelne Anwendung kann Aufrufe an Methoden oder Funktionen vornehmen, die zu einer der Schnittstellen gehören.</span><span class="sxs-lookup"><span data-stu-id="af9ff-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af9ff-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af9ff-118">See also</span></span>

<span data-ttu-id="af9ff-119">-[MAPI-Features und-Architektur](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="af9ff-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

