---
title: Transport Anbieterübersicht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356637"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="403a6-103">Transport Anbieterübersicht</span><span class="sxs-lookup"><span data-stu-id="403a6-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="403a6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="403a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="403a6-105">Ein Transportanbieter ist eine Dynamic Link Library (DLL), die als Vermittler zwischen dem MAPI-Subsystem und einem oder mehreren zugrunde liegenden Messagingsystemen fungiert.</span><span class="sxs-lookup"><span data-stu-id="403a6-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="403a6-106">Ein Messagingsystem ist ein bestimmter Mechanismus, mit dem Nachrichten gesendet und empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="403a6-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="403a6-107">Einige Beispiele für Messagingsysteme sind:</span><span class="sxs-lookup"><span data-stu-id="403a6-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="403a6-108">Ein freigegebenes Netzwerkdateisystem, in das der Transportanbieter Nachrichten direkt schreibt.</span><span class="sxs-lookup"><span data-stu-id="403a6-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="403a6-109">Eine TCP/IP-Netzwerkschnittstelle, die der Transportanbieter zum Herstellen einer Verbindung mit einem Messaging Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="403a6-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="403a6-110">Ein Onlinedienst, mit dem Benutzer eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="403a6-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="403a6-111">Ein hostbasiertes Messaging-oder Office-Automatisierungssystem.</span><span class="sxs-lookup"><span data-stu-id="403a6-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="403a6-112">Eine Reihe von Remoteprozeduraufrufen für einen Messaging Server.</span><span class="sxs-lookup"><span data-stu-id="403a6-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="403a6-113">Alles, was zum Übertragen von Daten von einem Computer zu einem anderen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="403a6-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="403a6-114">Eine Transportanbieter-DLL muss mit der von MAPI angegebenen Schnittstelle übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="403a6-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="403a6-115">Als Transportanbieter Entwickler implementieren Sie diese Schnittstelle im Hinblick auf die im Messagingsystem vorhandene Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="403a6-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

