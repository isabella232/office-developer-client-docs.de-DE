---
title: Nachrichteninhalt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 85bd3f7db53f195295405fb0b02c25f084786a67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586081"
---
# <a name="message-content"></a><span data-ttu-id="c0c6f-103">Nachrichteninhalt</span><span class="sxs-lookup"><span data-stu-id="c0c6f-103">Message Content</span></span>

  
  
<span data-ttu-id="c0c6f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0c6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0c6f-105">Es gibt zwei mögliche Codierung für den Nachrichteninhalt: eine Verwendung von MIME, die andere mit Uuencode.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="c0c6f-106">MIME ist die bevorzugte Codierung.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="c0c6f-107">Darüber hinaus definiert MAPI eine Eigenschaft pro Empfänger, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), der steuert, ob die TNEF-Informationen in eine ausgehende Nachricht enthalten sein sollen oder nicht.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="c0c6f-108">Es bestehen nun also insgesamt vier Arten der Codierung Nachrichteninhalt:</span><span class="sxs-lookup"><span data-stu-id="c0c6f-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="c0c6f-109">Mit TNEF MIME-Ermittlung</span><span class="sxs-lookup"><span data-stu-id="c0c6f-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="c0c6f-110">Ohne TNEF MIME-Ermittlung</span><span class="sxs-lookup"><span data-stu-id="c0c6f-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="c0c6f-111">UUENCODE mit TNEF</span><span class="sxs-lookup"><span data-stu-id="c0c6f-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="c0c6f-112">UUENCODE ohne TNEF</span><span class="sxs-lookup"><span data-stu-id="c0c6f-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="c0c6f-113">Auswählen von MIME oder Uuencode für ausgehende Nachrichten wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="c0c6f-114">Die folgenden Eigenschaften werden von TNEF ausgeschlossen: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="c0c6f-115">Alle anderen Übertragungseinehit Nachrichteneigenschaften sind im TNEF-Datenstrom enthalten.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="c0c6f-116">Die folgenden Vorschläge sind vorgesehen, um eine Liste der Parameter bereitzustellen, die die Implementierung entscheiden kann, wie unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c0c6f-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="c0c6f-117">Ob zum Codieren mithilfe von MIME oder Uuencode für ausgehende Nachrichten: boolean.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="c0c6f-118">Zeichensatz für ausgehende Nachrichten: Zeichenfolge (kopiert direkt an Charset-Parameter) oder -Enumeration (intern übersetzt Charset-Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="c0c6f-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

