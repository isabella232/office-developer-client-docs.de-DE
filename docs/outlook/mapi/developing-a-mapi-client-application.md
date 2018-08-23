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
ms.openlocfilehash: bffcfdd6d688c483655b97d61075b147430e3fcc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564976"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="544d1-103">Entwickeln einer MAPI-Clientanwendung</span><span class="sxs-lookup"><span data-stu-id="544d1-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="544d1-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="544d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="544d1-105">MAPI-Clientanwendungen werden mit der objektorientierte MAPI-Client-Schnittstelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="544d1-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="544d1-106">MAPI-Clients interagieren mit Messagingsystemen über die MAPI-Subsystems und MAPI-kompatible-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="544d1-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="544d1-107">Diese Interaktion kann auf verschiedene Weise auftreten. Es gibt eine enorme Vielfalt an in-Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="544d1-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="544d1-108">Die meisten Clients werden entweder Integration von messaging in ihren eingerichteten Featuregruppe oder Ausführen als ihre primäre Feature messaging-Clients messaging.</span><span class="sxs-lookup"><span data-stu-id="544d1-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="544d1-109">Andere Features, die möglicherweise MAPI-Clients bereitstellen sind profilverwaltung oder Adressbuch und Nachricht Management zu speichern.</span><span class="sxs-lookup"><span data-stu-id="544d1-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="544d1-110">Alle Messagingclients initialisieren die MAPI-Bibliotheken und starten Sie eine **Sitzung** mit MAPI-Subsystems.</span><span class="sxs-lookup"><span data-stu-id="544d1-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="544d1-111">Weitere Informationen finden Sie unter [Zugreifen auf Objekte mithilfe der Sitzung](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="544d1-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="544d1-112">Nachdem eine Sitzung eingerichtet wurde, können ein Client:</span><span class="sxs-lookup"><span data-stu-id="544d1-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="544d1-113">Ausgehende Nachrichten, einschließlich Antworten, Nachrichten und hohem weitergeleitet behandelt.</span><span class="sxs-lookup"><span data-stu-id="544d1-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="544d1-114">Eingehende Nachrichten behandelt.</span><span class="sxs-lookup"><span data-stu-id="544d1-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="544d1-115">Behandeln des Nachrichtenspeichers durch Öffnen Ordner und Nachrichten, erstellen, ändern, kopieren, und Senden von Nachrichten, Nachverfolgen von Unterhaltungen, und suchen einen oder mehrere Ordner.</span><span class="sxs-lookup"><span data-stu-id="544d1-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="544d1-116">Behandeln Sie das Adressbuch durch Erstellen und Ändern von Empfängern, Einträge suchen und Durchlaufen der Containerhierarchie.</span><span class="sxs-lookup"><span data-stu-id="544d1-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="544d1-117">Behandeln eines Transportdienstes Neukonfiguration durchführen, Optionen und Transport-Reihenfolge festlegen und Senden von Nachrichten bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="544d1-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="544d1-118">Benachrichtigung zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="544d1-118">Handle event notification.</span></span>
    
- <span data-ttu-id="544d1-119">Behandeln von Formularen.</span><span class="sxs-lookup"><span data-stu-id="544d1-119">Handle forms.</span></span>
    
- <span data-ttu-id="544d1-120">Behandeln von Benutzerprofilen und Message-Dienste.</span><span class="sxs-lookup"><span data-stu-id="544d1-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="544d1-121">Mithilfe der Themen in diesem Abschnitt können Sie das Implementieren dieser grundlegenden Aufgaben und Features, die MAPI-Client eindeutige zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="544d1-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

