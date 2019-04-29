---
title: Entwickeln einer MAPI-Client Anwendung
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
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="7fba1-103">Entwickeln einer MAPI-Client Anwendung</span><span class="sxs-lookup"><span data-stu-id="7fba1-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="7fba1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fba1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fba1-105">MAPI-Clientanwendungen werden mit der objektorientierten MAPI-Clientschnittstelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7fba1-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="7fba1-106">MAPI-Clients interagieren mit einem oder mehreren Messagingsystemen über das MAPI-Subsystem und die MAPI-kompatiblen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="7fba1-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="7fba1-107">Diese Interaktion kann auf viele verschiedene Arten erfolgen. Es gibt eine enorme Vielfalt in Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="7fba1-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="7fba1-108">Bei den meisten Clients handelt es sich um Messagingclients, die entweder Messaging in den festgelegten Featuresatz integrieren oder Messaging als primäres Feature ausführen.</span><span class="sxs-lookup"><span data-stu-id="7fba1-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="7fba1-109">Zu den weiteren Features, die MAPI-Clients bieten können, gehören die Profilverwaltung oder das Adressbuch-und Nachrichtenspeicher Management.</span><span class="sxs-lookup"><span data-stu-id="7fba1-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="7fba1-110">Alle Messagingclients initialisieren die MAPI-Bibliotheken und starten eine **Sitzung** mit dem MAPI-Subsystem.</span><span class="sxs-lookup"><span data-stu-id="7fba1-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="7fba1-111">Weitere Informationen finden Sie unter [zugreifen auf Objekte mithilfe der Sitzung](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="7fba1-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="7fba1-112">Nachdem eine Sitzung eingerichtet wurde, kann ein Client:</span><span class="sxs-lookup"><span data-stu-id="7fba1-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="7fba1-113">Behandeln Sie ausgehende Nachrichten, einschließlich Antworten, weitergeleiteten Nachrichten und erneuten Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="7fba1-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="7fba1-114">Behandeln eingehender Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="7fba1-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="7fba1-115">Behandeln Sie den Nachrichtenspeicher, indem Sie Ordner und Nachrichten öffnen, Nachrichten erstellen, ändern, kopieren und senden, Unterhaltungen nachverfolgen und einen oder mehrere Ordner durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="7fba1-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="7fba1-116">Behandeln des Adressbuchs durch Erstellen und Ändern von Empfängern, Suchen von Einträgen und durchlaufen der Containerhierarchie.</span><span class="sxs-lookup"><span data-stu-id="7fba1-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="7fba1-117">Behandeln eines Transportanbieters durch Ausführen einer Neukonfiguration, Festlegen von Optionen und Transport Reihenfolge und Senden von Nachrichten bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="7fba1-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="7fba1-118">Ereignisbenachrichtigung behandeln.</span><span class="sxs-lookup"><span data-stu-id="7fba1-118">Handle event notification.</span></span>
    
- <span data-ttu-id="7fba1-119">Behandeln von Formularen</span><span class="sxs-lookup"><span data-stu-id="7fba1-119">Handle forms.</span></span>
    
- <span data-ttu-id="7fba1-120">Behandeln von Profilen und Nachrichtendiensten</span><span class="sxs-lookup"><span data-stu-id="7fba1-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="7fba1-121">Verwenden Sie die Themen in diesem Abschnitt, um Sie bei der Implementierung dieser grundlegenden Aufgaben und der spezifischen Features zu unterstützen, mit denen Ihr MAPI-Client eindeutig wird.</span><span class="sxs-lookup"><span data-stu-id="7fba1-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

