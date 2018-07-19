---
title: Transportanbieterübersicht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 22b9da0cfe70cf499cc6f3a699eabe4aaee25b0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795766"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="a8ad2-103">Transportanbieterübersicht</span><span class="sxs-lookup"><span data-stu-id="a8ad2-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="a8ad2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8ad2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8ad2-105">Ein Transportanbieter ist eine Dynamic Link Library (DLL) fungiert als Mittler zwischen MAPI-Subsystems und einen oder mehrere zugrunde liegenden messaging-Systeme.</span><span class="sxs-lookup"><span data-stu-id="a8ad2-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="a8ad2-106">Messaging-System ist einen bestimmten Mechanismus, mit dem Nachrichten gesendet und empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="a8ad2-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="a8ad2-107">Beispiele von Messagingsystemen sind:</span><span class="sxs-lookup"><span data-stu-id="a8ad2-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="a8ad2-108">Eine Netzwerkfreigabe Dateisystem, die der Adressbuchhierarchie Nachrichten direkt schreibt.</span><span class="sxs-lookup"><span data-stu-id="a8ad2-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="a8ad2-109">Eine TCP/IP-Netzwerkschnittstelle, die mit der Adressbuchhierarchie messaging-Server herstellt.</span><span class="sxs-lookup"><span data-stu-id="a8ad2-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="a8ad2-110">Ein Onlinedienst, die Benutzer eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="a8ad2-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="a8ad2-111">Ein Host-basierte messaging oder Office Automatisierungssystem.</span><span class="sxs-lookup"><span data-stu-id="a8ad2-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="a8ad2-112">Eine Reihe von Remoteprozeduraufrufe an einen Messagingserver.</span><span class="sxs-lookup"><span data-stu-id="a8ad2-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="a8ad2-113">Alle Werte, die zum Übertragen von Daten von einem Computer zu einem anderen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a8ad2-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="a8ad2-114">Ein Transportdienstes DLL muss die MAPI angegebene Schnittstelle entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a8ad2-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="a8ad2-115">Als Entwickler Anbieter Transport implementieren Sie diese Schnittstelle im Hinblick auf die Funktionalität im Nachrichtensystem vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a8ad2-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

