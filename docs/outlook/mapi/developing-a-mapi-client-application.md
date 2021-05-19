---
title: Entwickeln einer MAPI-Clientanwendung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410035"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="1f47e-103">Entwickeln einer MAPI-Clientanwendung</span><span class="sxs-lookup"><span data-stu-id="1f47e-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="1f47e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f47e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f47e-105">MAPI-Clientanwendungen werden mit der objektorientierten MAPI-Clientschnittstelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1f47e-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="1f47e-106">MAPI-Clients interagieren mit einem oder mehreren Messagingsystemen über das MAPI-Subsystem und MAPI-kompatible Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="1f47e-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="1f47e-107">Diese Interaktion kann auf unterschiedliche Weise erfolgen. Es gibt eine enorme Vielfalt an Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="1f47e-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="1f47e-108">Bei den meisten Clients handelt es sich um Messagingclients, die Messaging entweder in ihren etablierten Featuresatz integrieren oder Messaging als primäres Feature ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f47e-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="1f47e-109">Zu den weiteren Features, die MAPI-Clients bereitstellen können, gehören die Profilverwaltung oder die Adressbuch- und Nachrichtenspeicherverwaltung.</span><span class="sxs-lookup"><span data-stu-id="1f47e-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="1f47e-110">Alle Messagingclients initialisieren die MAPI-Bibliotheken und starten **eine** Sitzung mit dem MAPI-Subsystem.</span><span class="sxs-lookup"><span data-stu-id="1f47e-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="1f47e-111">Weitere Informationen finden Sie unter [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="1f47e-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="1f47e-112">Nachdem eine Sitzung eingerichtet wurde, kann ein Client:</span><span class="sxs-lookup"><span data-stu-id="1f47e-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="1f47e-113">Behandeln sie ausgehende Nachrichten, einschließlich Antworten, weitergeleitete Nachrichten und erneute Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="1f47e-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="1f47e-114">Behandeln eingehender Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="1f47e-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="1f47e-115">Behandeln Sie den Nachrichtenspeicher, indem Sie Ordner und Nachrichten öffnen, Nachrichten erstellen, ändern, kopieren und senden, Unterhaltungen nachverfolgen und einen oder mehrere Ordner durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="1f47e-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="1f47e-116">Behandeln Sie das Adressbuch, indem Sie Empfänger erstellen und ändern, Einträge suchen und die Containerhierarchie durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="1f47e-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="1f47e-117">Behandeln Sie einen Transportanbieter, indem Sie eine Neukonfiguration durchführen, Optionen und Transportreihenfolge festlegen und Nachrichten bei Bedarf senden.</span><span class="sxs-lookup"><span data-stu-id="1f47e-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="1f47e-118">Behandeln der Ereignisbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="1f47e-118">Handle event notification.</span></span>
    
- <span data-ttu-id="1f47e-119">Behandeln von Formularen</span><span class="sxs-lookup"><span data-stu-id="1f47e-119">Handle forms.</span></span>
    
- <span data-ttu-id="1f47e-120">Behandeln von Profilen und Nachrichtendiensten.</span><span class="sxs-lookup"><span data-stu-id="1f47e-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="1f47e-121">Verwenden Sie die Themen in diesem Abschnitt, um Ihnen bei der Implementierung dieser grundlegenden Aufgaben und der spezifischen Features zu helfen, die Ihren MAPI-Client eindeutig machen.</span><span class="sxs-lookup"><span data-stu-id="1f47e-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

