---
title: MAPI-Architektur (Übersicht)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: db8ca0945c429e7b277ec95b419386d1ce175169
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792943"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="d4e07-103">MAPI-Architektur (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="d4e07-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="d4e07-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4e07-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4e07-105">MAPI definiert eine modulare Architektur, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d4e07-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="d4e07-106">![Outlook 2010-Architektur] (media/amapi_43.gif "Outlook 2010-Architektur")</span><span class="sxs-lookup"><span data-stu-id="d4e07-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="d4e07-107">Die MAPI-Anwendung wird als Clientanwendung bezeichnet, da es sich um einen Client des MAPI-Subsystems darstellt.</span><span class="sxs-lookup"><span data-stu-id="d4e07-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="d4e07-108">Messaging-basierte Anwendungen als ein zentraler Bestandteil von deren Verarbeitung messaging einsetzen und bieten umfangreiche-Funktionen, wie etwa den Austausch von Informationen über verschiedene Arten in verschiedenen Formaten und die Möglichkeit zum Speichern und organisieren die Informationen lokal.</span><span class="sxs-lookup"><span data-stu-id="d4e07-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="d4e07-109">E-Mail, Planung und Arbeit Flow Anwendungen sind Beispiele für die messaging-basierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d4e07-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="d4e07-110">MAPI-Subsystems eine einheitliche Benutzeroberfläche und die Programmierschnittstellen besteht.</span><span class="sxs-lookup"><span data-stu-id="d4e07-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="d4e07-111">Einheitliche Benutzeroberfläche ist eine Gruppe von Dialogfeldern, die Clientanwendungen ein einheitliches Aussehen und Benutzer bietet ein konsistentes arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4e07-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="d4e07-112">MAPI hat Programmierschnittstellen, die von MAPI-Subsystems, Client-Software-Entwicklern und Service Provider Entwickler verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4e07-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="d4e07-113">Die MAPI-Programmierschnittstelle ist die Haupt-Objekt-basierten Programmierschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d4e07-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="d4e07-114">Die MAPI-Programmierschnittstelle ähnelt der OLE Component Object Model und wird von der MAPI-Subsystems und messaging-basierte Clientanwendungen, die in C oder C++ geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d4e07-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="d4e07-115">Als Client Softwareentwickler stellen Sie MAPI-Aufrufe direkt über die MAPI-Programmierschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d4e07-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="d4e07-116">Sie können die messaging mit einer einzigen Benutzeroberfläche der MAPI-Client oder eine Kombination von Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="d4e07-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="d4e07-117">In einer einzigen Anwendung kann Methoden oder Funktionen, die zu einer Schnittstelle gehören anrufen.</span><span class="sxs-lookup"><span data-stu-id="d4e07-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d4e07-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4e07-118">See also</span></span>

<span data-ttu-id="d4e07-119">-[MAPI-Features und die Architektur](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="d4e07-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

