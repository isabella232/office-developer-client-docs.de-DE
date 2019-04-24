---
title: Formatierter Text in MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f37d65e4beb328c2c92cf0c2ab28586af6bee45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327468"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="27036-103">Formatierter Text in MAPI</span><span class="sxs-lookup"><span data-stu-id="27036-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="27036-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27036-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27036-105">Der Text einer Nachricht kann mit nur-Text oder formatiertem Text gespeichert und übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="27036-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="27036-106">Formatierter Text verbessert den Nachrichtentext, indem sein Aussehen mit beispielsweise einer oder mehreren Schriftarten, Schriftgraden oder Textfarben geändert wird.</span><span class="sxs-lookup"><span data-stu-id="27036-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="27036-107">Es wird empfohlen, dass alle Clients und nach Möglichkeit alle Nachrichtenspeicher Anbieter formatierten Text unterstützen.</span><span class="sxs-lookup"><span data-stu-id="27036-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="27036-108">Die Unterstützung von formatiertem Text in Nachrichten bietet einen Mehrwert durch verbesserte Nachrichten Lesbarkeit und eine einfachere und effizientere Nachrichtenverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="27036-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="27036-109">Formatierter Text kann auf verschiedene Arten implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="27036-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="27036-110">Die häufigste Methode ist das Rich-Text-Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="27036-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="27036-111">MAPI definiert drei transmitable-Eigenschaften für die Aufbewahrung von Nachrichtentext Informationen: **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)) für nur-Text, **PR_HTML** ([pidtaghtml (](pidtaghtml-canonical-property.md)) für HTML und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) für RTF-Text, der komprimiert wurde.</span><span class="sxs-lookup"><span data-stu-id="27036-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="27036-112">Da die formatierte Version eines Nachrichtentexts doppelt so groß wie die Version ohne Formatierung sein kann, wird der RTF-Text komprimiert, bevor er mit der Nachricht übertragen und in der **PR_RTF_COMPRESSED** -Eigenschaft gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="27036-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="27036-113">Wenn die Nachricht auf dem Bildschirm angezeigt werden soll, wird Sie mithilfe einer von MAPI bereitgestellten Hilfsfunktion unkomprimiert entpackt.</span><span class="sxs-lookup"><span data-stu-id="27036-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="27036-114">MAPI definiert diese beiden Nachrichtentext Eigenschaften und-Mechanismen für die Konvertierung zwischen diesen, sodass RTF-fähige Clients mit Clients und Messagingsystemen interagieren können, die keinen formatierten Text unterstützen.</span><span class="sxs-lookup"><span data-stu-id="27036-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="27036-115">Synchronisieren von Text und Formatierung</span><span class="sxs-lookup"><span data-stu-id="27036-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="27036-116">Beschreibt, wie der RTF-Nachrichtentext mit der Formatierung synchronisiert bleibt.</span><span class="sxs-lookup"><span data-stu-id="27036-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="27036-117">Unterstützung von formatiertem Text in ausgehenden Nachrichten: Aufgaben des Kunden</span><span class="sxs-lookup"><span data-stu-id="27036-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="27036-118">Beschreibt die Verantwortlichkeiten der Clientanwendung für die Unterstützung von formatiertem Text in ausgehenden Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="27036-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="27036-119">Unterstützung von formatiertem Text in eingehenden Nachrichten: Aufgaben des Kunden</span><span class="sxs-lookup"><span data-stu-id="27036-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="27036-120">Beschreibt die Verantwortlichkeiten der Clientanwendung für die Unterstützung von formatiertem Text in eingehenden Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="27036-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="27036-121">Unterstützung von formatiertem Text: Aufgaben des Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="27036-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="27036-122">Beschreibt die Aufgaben des Nachrichtenspeichers zur Unterstützung von formatiertem Text.</span><span class="sxs-lookup"><span data-stu-id="27036-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="27036-123">Unterstützung von formatiertem Text: Rendering Attachments</span><span class="sxs-lookup"><span data-stu-id="27036-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="27036-124">Beschreibt, wie Sie auswählen, wo Anlagen gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="27036-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="27036-125">Unterstützung von formatiertem Text: Aufgaben des Gateways</span><span class="sxs-lookup"><span data-stu-id="27036-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="27036-126">Beschreibt die Aufgaben des Gateways für ausgehende und eingehende formatierte Textnachrichten.</span><span class="sxs-lookup"><span data-stu-id="27036-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

