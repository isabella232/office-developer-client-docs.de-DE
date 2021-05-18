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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408089"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="dc6f7-103">Formatierter Text in MAPI</span><span class="sxs-lookup"><span data-stu-id="dc6f7-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="dc6f7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc6f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc6f7-105">Der Text einer Nachricht kann mithilfe von Nur-Text oder formatiertem Text gespeichert und übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="dc6f7-106">Formatierter Text verbessert den Nachrichtentext, indem er seine Darstellung z. B. mit einer oder mehreren Schriftarten, Schriftgrößen oder Textfarben ändert.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="dc6f7-107">Es wird empfohlen, dass alle Clients und wann immer möglich alle Nachrichtenspeicheranbieter formatierten Text unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="dc6f7-108">Die Unterstützung formatierter Texte in Nachrichten bietet einen Mehrwert, indem die Nachrichten lesbarkeit verbessert und die Nachrichtenverarbeitung einfacher und effizienter wird.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="dc6f7-109">Formatierter Text kann auf unterschiedliche Weise implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="dc6f7-110">Die gängigste Methode ist das Rich Text Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="dc6f7-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="dc6f7-111">MAPI definiert drei durchlässige Eigenschaften zum Halten von Nachrichtentextinformationen: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) für Nur-Text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) für HTML und **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) für komprimierten RTF-Text.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="dc6f7-112">Da die formatierte Version eines Nachrichtentexts doppelt so groß wie die Version ohne Formatierung sein kann, wird der RTF-Text komprimiert, bevor er mit der Nachricht übertragen und in der PR_RTF_COMPRESSED **gespeichert** wird.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="dc6f7-113">Wenn es an der Zeit ist, die Nachricht auf dem Bildschirm anzuzeigen, wird sie mithilfe einer Hilfsfunktion, die von MAPI bereitgestellt wird, nicht komprimiert.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="dc6f7-114">MAPI definiert diese beiden Nachrichtentexteigenschaften und -mechanismen für die Konvertierung zwischen diesen, sodass RTF-übergreifende Clients mit Clients und Messagingsystemen zusammenarbeiten können, die formatierten Text nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="dc6f7-115">Synchronisieren von Text und Formatierung</span><span class="sxs-lookup"><span data-stu-id="dc6f7-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="dc6f7-116">Beschreibt, wie RTF-Nachrichtentext mit der Formatierung synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="dc6f7-117">Unterstützen von formatierten Text in ausgehenden Nachrichten: Clientaufgaben</span><span class="sxs-lookup"><span data-stu-id="dc6f7-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="dc6f7-118">Beschreibt die Verantwortlichkeiten der Clientanwendung für die Unterstützung formatierten Texts in ausgehenden Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="dc6f7-119">Unterstützen von formatierten Text in eingehenden Nachrichten: Clientzu zuständigkeiten</span><span class="sxs-lookup"><span data-stu-id="dc6f7-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="dc6f7-120">Beschreibt die Verantwortlichkeiten der Clientanwendung für die Unterstützung formatierten Texts in eingehenden Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="dc6f7-121">Unterstützen von formatierten Text: Nachrichten Store Verantwortlichkeiten</span><span class="sxs-lookup"><span data-stu-id="dc6f7-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="dc6f7-122">Beschreibt die Aufgaben des Nachrichtenspeichers für die Unterstützung formatierten Texts.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="dc6f7-123">Unterstützen von formatierten Text: Rendern von Anlagen</span><span class="sxs-lookup"><span data-stu-id="dc6f7-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="dc6f7-124">Beschreibt, wie Sie auswählen, wo Anlagen gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="dc6f7-125">Unterstützen von formatierten Text: Gateway-Verantwortlichkeiten</span><span class="sxs-lookup"><span data-stu-id="dc6f7-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="dc6f7-126">Beschreibt die Verantwortlichkeiten des Gateways für ausgehende und eingehende formatierte Textnachrichten.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

