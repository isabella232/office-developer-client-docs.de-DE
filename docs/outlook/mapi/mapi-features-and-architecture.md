---
title: MAPI-Features und die Architektur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 34bae703-a979-437c-9d86-8b91e9822a54
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 75af9598daf4e0d940217504b00cab6d2201d93a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792971"
---
# <a name="mapi-features-and-architecture"></a><span data-ttu-id="b57cb-103">MAPI-Features und die Architektur</span><span class="sxs-lookup"><span data-stu-id="b57cb-103">MAPI Features and Architecture</span></span>

  
  
<span data-ttu-id="b57cb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b57cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b57cb-105">Messaging-API (MAPI) besteht aus einer Reihe von common Application programming Interfaces und eine Komponente Dynamic Link Library (DLL).</span><span class="sxs-lookup"><span data-stu-id="b57cb-105">Messaging API (MAPI) is composed of a set of common application programming interfaces and a dynamic-link library (DLL) component.</span></span> <span data-ttu-id="b57cb-106">Die Schnittstellen dienen zum Erstellen und Zugriff auf verschiedene Messaginganwendungen und messaging-Systeme, bietet eine einheitliche Umgebung für die Entwicklung und Verwendung und true Unabhängigkeit für beide bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b57cb-106">The interfaces are used to create and access diverse messaging applications and messaging systems, offering a uniform environment for development and use, and providing true independence for both.</span></span> <span data-ttu-id="b57cb-107">Die DLL-Datei enthält das MAPI-Subsystem, verwaltet die Interaktion zwischen Messaginganwendungen Front-End- und Back-End-messaging-Systeme und bietet eine einheitliche Benutzeroberfläche für häufige Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="b57cb-107">The DLL contains the MAPI subsystem, which manages the interaction between front-end messaging applications and back-end messaging systems and provides a common user interface for frequent tasks.</span></span> <span data-ttu-id="b57cb-108">MAPI-Subsystems fungiert als Clearing House zentralen vereinheitlicht die verschiedenen Messagingsystemen und mit Clients aus ihre Unterschiede abschirmen.</span><span class="sxs-lookup"><span data-stu-id="b57cb-108">The MAPI subsystem acts as a central clearinghouse to unify the various messaging systems and shield clients from their differences.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b57cb-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b57cb-109">See also</span></span>



[<span data-ttu-id="b57cb-110">MAPI-Konzepte (engl.)</span><span class="sxs-lookup"><span data-stu-id="b57cb-110">MAPI Concepts</span></span>](mapi-concepts.md)

