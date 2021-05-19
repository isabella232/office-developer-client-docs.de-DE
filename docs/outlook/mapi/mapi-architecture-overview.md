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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410077"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="f3f13-103">Übersicht über die MAPI-Architektur</span><span class="sxs-lookup"><span data-stu-id="f3f13-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="f3f13-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3f13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3f13-105">MAPI definiert eine modulare Architektur, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f3f13-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="f3f13-106">![Outlook 2010-Architektur](media/amapi_43.gif "Outlook 2010-Architektur")</span><span class="sxs-lookup"><span data-stu-id="f3f13-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="f3f13-107">Die MAPI-Anwendung wird als Clientanwendung bezeichnet, da sie ein Client des MAPI-Subsystems ist.</span><span class="sxs-lookup"><span data-stu-id="f3f13-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="f3f13-108">Messaging-basierte Anwendungen verwenden Messaging als zentralen Teil ihrer Verarbeitung und bieten umfangreiche Messagingfeatures, z. B. den Austausch von Informationen verschiedener Typen in verschiedenen Formaten und die Möglichkeit, die Informationen lokal zu speichern und zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="f3f13-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="f3f13-109">E-Mail-, Planungs- und Arbeitsflussanwendungen sind Beispiele für messagingbasierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="f3f13-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="f3f13-110">Das MAPI-Subsystem besteht aus einer gemeinsamen Benutzeroberfläche und den Programmierschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="f3f13-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="f3f13-111">Bei der allgemeinen Benutzeroberfläche handelt es sich um eine Reihe von Dialogfelder, die Clientanwendungen ein einheitliches Aussehen und Benutzern eine konsistente Arbeit ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f3f13-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="f3f13-112">MAPI verfügt über Programmierschnittstellen, die vom MAPI-Subsystem, von Clientsoftwareentwicklern und von Dienstanbieterentwicklern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3f13-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="f3f13-113">Die MAPI-Programmierschnittstelle ist die wichtigste objektbasierte Programmierschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f3f13-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="f3f13-114">Die MAPI-Programmierschnittstelle ähnelt dem OLE-Komponentenobjektmodell und wird vom #A0 und messagingbasierten Clientanwendungen verwendet, die in C oder C++ geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="f3f13-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="f3f13-115">Als Clientsoftwareentwickler nehmen Sie MAPI-Aufrufe direkt über die MAPI-Programmierschnittstelle vor.</span><span class="sxs-lookup"><span data-stu-id="f3f13-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="f3f13-116">Sie können Messaging mit einer einzelnen MAPI-Clientschnittstelle oder einer Kombination von Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="f3f13-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="f3f13-117">Eine einzelne Anwendung kann Methoden oder Funktionen aufrufen, die zu einer der Schnittstellen gehören.</span><span class="sxs-lookup"><span data-stu-id="f3f13-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f3f13-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3f13-118">See also</span></span>

<span data-ttu-id="f3f13-119">-[MAPI-Features und -Architektur](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="f3f13-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

