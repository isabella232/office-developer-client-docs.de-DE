---
title: MAPI-Spooler-Übersicht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309580"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="587a3-103">MAPI-Spooler-Übersicht</span><span class="sxs-lookup"><span data-stu-id="587a3-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="587a3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="587a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="587a3-105">MAPI-Spooler ist eine Funktion des Microsoft Office Outlook-Prozesses, der für das Senden von Nachrichten an und das Empfangen von e-Mails von einem Messagingsystem zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="587a3-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="587a3-106">MAPI-Spooler spielt eine wichtige Rolle bei Nachrichtenempfang und-Zustellung.</span><span class="sxs-lookup"><span data-stu-id="587a3-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="587a3-107">Wenn ein Messagingsystem nicht verfügbar ist, werden die Nachrichten von der MAPI-Warteschlange gespeichert und zu einem späteren Zeitpunkt automatisch weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="587a3-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="587a3-108">Diese Fähigkeit, Daten bei Bedarf beizubehalten oder zu senden, wird als "Store" und "Forward" bezeichnet, eine wichtige Funktion in Umgebungen, in denen Remoteverbindungen gängig sind und der Netzwerkdatenverkehr hoch ist.</span><span class="sxs-lookup"><span data-stu-id="587a3-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="587a3-109">MAPI-Spooler wird als Hintergrundthread in Outlook ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="587a3-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="587a3-110">MAPI-Spooler hat zusätzliche Aufgaben im Zusammenhang mit der Nachrichtenverteilung.</span><span class="sxs-lookup"><span data-stu-id="587a3-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="587a3-111">Zu diesen zusätzlichen Aufgaben gehört Folgendes:</span><span class="sxs-lookup"><span data-stu-id="587a3-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="587a3-112">Nachverfolgen der Empfängertypen, die von bestimmten Transportanbietern verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="587a3-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="587a3-113">Informieren einer Clientanwendung, wenn eine neue Nachricht zugestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="587a3-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="587a3-114">Aufrufen der Nachrichten Vorverarbeitung und nach Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="587a3-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="587a3-115">Generieren von Berichten, die darauf hindeuten, dass die Nachrichtenübermittlung stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="587a3-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="587a3-116">Verwalten des Status von verarbeiteten Empfängern.</span><span class="sxs-lookup"><span data-stu-id="587a3-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="587a3-117">Die folgende Abbildung zeigt auf einer hohen Ebene, wie eine Nachricht von einem Client zum Messagingsystem fließt.</span><span class="sxs-lookup"><span data-stu-id="587a3-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="587a3-118">**Flussdiagramm für ausgehende Nachrichten**</span><span class="sxs-lookup"><span data-stu-id="587a3-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="587a3-119">![Ablauf der ausgehenden Nachrichten] (media/amapi_46.gif "Ablauf der ausgehenden Nachrichten")</span><span class="sxs-lookup"><span data-stu-id="587a3-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="587a3-120">Der Benutzer einer Clientanwendung sendet eine Nachricht an einen oder mehrere Empfänger.</span><span class="sxs-lookup"><span data-stu-id="587a3-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="587a3-121">Der Nachrichtenspeicher Anbieter initiiert den Sendevorgang und formatiert die Nachricht mit zusätzlichen Informationen, die für die Übertragung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="587a3-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="587a3-122">MAPI-Spooler empfängt die zu verarbeitende Nachricht, wenn eine der folgenden Bedingungen eintritt:</span><span class="sxs-lookup"><span data-stu-id="587a3-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="587a3-123">Der Nachrichtenspeicher Anbieter ist nicht eng mit einem Transportanbieter gekoppelt.</span><span class="sxs-lookup"><span data-stu-id="587a3-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="587a3-124">Die Nachricht erfordert die Vorverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="587a3-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="587a3-125">Der Nachrichtenspeicher und der Transportanbieter sind eng gekoppelt, können jedoch nicht alle Empfänger verarbeiten, an die die Nachricht adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="587a3-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="587a3-126">Wenn die Nachricht vom MAPI-Spooler empfangen wird, wird die erforderliche Vorverarbeitung ausgeführt und die Nachricht an den entsprechenden Transportanbieter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="587a3-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="587a3-127">Der Transportanbieter übergibt die Nachricht an das Messagingsystem, das Sie an den beabsichtigten Empfänger sendet.</span><span class="sxs-lookup"><span data-stu-id="587a3-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="587a3-128">Bei eingehenden Nachrichten wird der Fluss umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="587a3-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="587a3-129">Der Transportanbieter empfängt eine Nachricht von seinem Messagingsystem und benachrichtigt MAPI-Spooler.</span><span class="sxs-lookup"><span data-stu-id="587a3-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="587a3-130">Spooler führt alle erforderlichen Nachbearbeitung aus und informiert den Nachrichtenspeicher Anbieter darüber, dass eine neue Nachricht eingegangen ist.</span><span class="sxs-lookup"><span data-stu-id="587a3-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="587a3-131">Diese Benachrichtigung veranlasst den Client, seine Nachrichtenanzeige zu aktualisieren, sodass der Benutzer die neue Nachricht lesen kann.</span><span class="sxs-lookup"><span data-stu-id="587a3-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="587a3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="587a3-132">See also</span></span>

- [<span data-ttu-id="587a3-133">MAPI-Features und -Architektur</span><span class="sxs-lookup"><span data-stu-id="587a3-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

