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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432716"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="3af67-103">MAPI-Spooler-Übersicht</span><span class="sxs-lookup"><span data-stu-id="3af67-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="3af67-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3af67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3af67-105">DER MAPI-Spooler ist eine Funktion des Microsoft Office Outlook, der für das Senden von Nachrichten an und den Empfang von Nachrichten von einem Messagingsystem zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="3af67-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="3af67-106">Der MAPI-Spooler spielt eine wichtige Rolle bei der Nachrichtenbestätigung und -zustellung.</span><span class="sxs-lookup"><span data-stu-id="3af67-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="3af67-107">Wenn ein Messagingsystem nicht verfügbar ist, speichert der MAPI-Spooler die Nachrichten und gibt sie zu einem späteren Zeitpunkt automatisch weiter.</span><span class="sxs-lookup"><span data-stu-id="3af67-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="3af67-108">Diese Möglichkeit, Daten bei Bedarf zu speichern oder zu senden, wird als Speicher und Weiterleitung bezeichnet. Dies ist ein entscheidendes Feature in Umgebungen, in denen Remoteverbindungen häufig verwendet werden und der Netzwerkdatenverkehr hoch ist.</span><span class="sxs-lookup"><span data-stu-id="3af67-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="3af67-109">DER MAPI-Spooler wird als Hintergrundthread innerhalb Outlook.</span><span class="sxs-lookup"><span data-stu-id="3af67-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="3af67-110">Der MAPI-Spooler hat zusätzliche Verantwortlichkeiten im Zusammenhang mit der Nachrichtenverteilung.</span><span class="sxs-lookup"><span data-stu-id="3af67-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="3af67-111">Diese zusätzlichen Aufgaben umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3af67-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="3af67-112">Nachverfolgen der Empfängertypen, die von bestimmten Transportanbietern verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="3af67-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="3af67-113">Informieren einer Clientanwendung, wenn eine neue Nachricht zugestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3af67-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="3af67-114">Aufrufen der Nachrichtenvorverarbeitung und nach der Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="3af67-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="3af67-115">Generieren von Berichten, die angeben, dass die Nachrichtenzustellung erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="3af67-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="3af67-116">Beibehalten des Status für verarbeitete Empfänger.</span><span class="sxs-lookup"><span data-stu-id="3af67-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="3af67-117">Die folgende Abbildung zeigt auf einer hohen Ebene, wie eine Nachricht von einem Client zum Messagingsystem fließt.</span><span class="sxs-lookup"><span data-stu-id="3af67-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="3af67-118">**Flussdiagramm für ausgehende Nachrichten**</span><span class="sxs-lookup"><span data-stu-id="3af67-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="3af67-119">![Ausgehender Nachrichtenfluss](media/amapi_46.gif "Ausgehender Nachrichtenfluss")</span><span class="sxs-lookup"><span data-stu-id="3af67-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="3af67-120">Der Benutzer einer Clientanwendung sendet eine Nachricht an einen oder mehrere Empfänger.</span><span class="sxs-lookup"><span data-stu-id="3af67-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="3af67-121">Der Nachrichtenspeicheranbieter initiiert den Sendevorgang und formatiert die Nachricht mit zusätzlichen Informationen, die für die Übertragung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3af67-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="3af67-122">Der MAPI-Spooler empfängt die Zu verarbeitende Nachricht, wenn eine der folgenden Bedingungen auftritt:</span><span class="sxs-lookup"><span data-stu-id="3af67-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="3af67-123">Der Nachrichtenspeicheranbieter ist nicht eng mit einem Transportanbieter gekoppelt.</span><span class="sxs-lookup"><span data-stu-id="3af67-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="3af67-124">Die Nachricht erfordert eine Vorverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="3af67-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="3af67-125">Der Nachrichtenspeicher und der Transportanbieter sind eng gekoppelt, können jedoch nicht alle Empfänger behandeln, an die die Nachricht adressiert wird.</span><span class="sxs-lookup"><span data-stu-id="3af67-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="3af67-126">Wenn der MAPI-Spooler die Nachricht empfängt, führt er alle erforderlichen Vorverarbeitungen durch und übermittelt die Nachricht an den entsprechenden Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="3af67-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="3af67-127">Der Transportanbieter gibt die Nachricht an sein Messagingsystem weiter, das sie an den beabsichtigten Empfänger sendet.</span><span class="sxs-lookup"><span data-stu-id="3af67-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="3af67-128">Bei eingehenden Nachrichten wird der Fluss umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="3af67-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="3af67-129">Der Transportanbieter empfängt eine Nachricht von seinem Messagingsystem und benachrichtigt den MAPI-Spooler.</span><span class="sxs-lookup"><span data-stu-id="3af67-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="3af67-130">Spooler führt alle erforderlichen Nachverarbeitungen durch und informiert den Nachrichtenspeicheranbieter, dass eine neue Nachricht eingetroffen ist.</span><span class="sxs-lookup"><span data-stu-id="3af67-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="3af67-131">Diese Benachrichtigung bewirkt, dass der Client seine Nachrichtenanzeige aktualisiert, sodass der Benutzer die neue Nachricht lesen kann.</span><span class="sxs-lookup"><span data-stu-id="3af67-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3af67-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3af67-132">See also</span></span>

- [<span data-ttu-id="3af67-133">MAPI-Features und -Architektur</span><span class="sxs-lookup"><span data-stu-id="3af67-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

