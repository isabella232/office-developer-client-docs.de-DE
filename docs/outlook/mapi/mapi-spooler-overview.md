---
title: MAPI-Warteschlange (Übersicht)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5e4bd4f6038db3dbb33ec3511d953448fea7a6c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793091"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="06c98-103">MAPI-Warteschlange (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="06c98-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="06c98-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06c98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06c98-105">MAPI-Warteschlange ergibt sich aus der Microsoft Office Outlook-Prozess, der für das Senden von Nachrichten an und Empfangen von Nachrichten aus einem messaging-System verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="06c98-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="06c98-106">MAPI-Warteschlange spielt eine wichtige Rolle in der Nachricht und die Zustellung.</span><span class="sxs-lookup"><span data-stu-id="06c98-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="06c98-107">Bei einem messaging-System nicht verfügbar ist, MAPI-Warteschlange werden die Nachrichten gespeichert und automatisch zu einem späteren Zeitpunkt weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="06c98-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="06c98-108">Die Möglichkeit, halten Sie sich oder Senden von Daten bei Bedarf wird als speichern und weiterleiten, ein wichtiges Feature in Umgebungen, in denen Remoteverbindungen sind häufige und Netzwerkdatenverkehr ist hoch, bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="06c98-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="06c98-109">MAPI-Warteschlange in Outlook als Hintergrundthread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06c98-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="06c98-110">MAPI-Warteschlange verfügt über zusätzliche Aufgaben im Zusammenhang mit der Verteilung von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="06c98-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="06c98-111">Diese zusätzlichen Aufgaben umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="06c98-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="06c98-112">Verfolgen von die Empfängertypen, die vom Anbieter von spezifischen Transport verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="06c98-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="06c98-113">Eine Clientanwendung informiert, wenn eine neue Nachricht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="06c98-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="06c98-114">Nachricht der vorverarbeitung und Traditionsgemäß aufrufen.</span><span class="sxs-lookup"><span data-stu-id="06c98-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="06c98-115">Generieren von Berichten, die angeben, Nachrichtenübermittlung ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="06c98-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="06c98-116">Verwalten von Status auf verarbeiteten Empfänger.</span><span class="sxs-lookup"><span data-stu-id="06c98-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="06c98-117">Die folgende Abbildung zeigt auf allgemeiner Ebene, wie eine Nachricht von einem Client an die messaging-System fließt.</span><span class="sxs-lookup"><span data-stu-id="06c98-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="06c98-118">**Flussdiagramm für ausgehende Nachrichten**</span><span class="sxs-lookup"><span data-stu-id="06c98-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="06c98-119">![Ausgehende Nachrichtenfluss] (media/amapi_46.gif "Ausgehende Nachrichtenfluss")</span><span class="sxs-lookup"><span data-stu-id="06c98-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="06c98-120">Der Benutzer von einer Clientanwendung sendet eine Nachricht an einen oder mehrere Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="06c98-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="06c98-121">Die Nachricht speichern Anbieter initiiert im Sendevorgang Formatierung der Nachricht mit zusätzlichen Informationen für die Übertragung benötigt.</span><span class="sxs-lookup"><span data-stu-id="06c98-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="06c98-122">MAPI-Warteschlange empfängt die Meldung verarbeiten, wenn einer der folgenden Situationen auftreten:</span><span class="sxs-lookup"><span data-stu-id="06c98-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="06c98-123">Der Nachricht Speicheranbieter ist nicht eng mit eines Transportdienstes verknüpft.</span><span class="sxs-lookup"><span data-stu-id="06c98-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="06c98-124">Die Nachricht muss der vorverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="06c98-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="06c98-125">Die Nachrichtenspeicher und Transport Anbieter eng verknüpft sind, aber sie können nicht alle Empfänger, an die Nachricht adressiert ist, behandeln.</span><span class="sxs-lookup"><span data-stu-id="06c98-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="06c98-126">Wenn MAPI-Warteschlange die Nachricht empfängt, führt der erforderlichen vorverarbeitung und übermittelt die Nachricht an den entsprechenden Adressbuchhierarchie.</span><span class="sxs-lookup"><span data-stu-id="06c98-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="06c98-127">Der Adressbuchhierarchie bietet die Nachricht an die messaging-System, an den Empfänger sendet.</span><span class="sxs-lookup"><span data-stu-id="06c98-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="06c98-128">Mit eingehenden Nachrichten wird der Ablauf umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="06c98-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="06c98-129">Der Transportdienst empfängt eine Nachricht von messaging-System und MAPI-Warteschlange benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="06c98-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="06c98-130">Warteschlange führt alle erforderlichen Nachbearbeitung und dem Speicheranbieter Nachricht informiert werden, dass eine neue Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="06c98-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="06c98-131">Diese Benachrichtigung wird vom Client zum Aktualisieren der Nachricht-Display, dem der Benutzer die neue Nachricht lesen.</span><span class="sxs-lookup"><span data-stu-id="06c98-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06c98-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06c98-132">See also</span></span>

- [<span data-ttu-id="06c98-133">MAPI-Features und die Architektur</span><span class="sxs-lookup"><span data-stu-id="06c98-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

