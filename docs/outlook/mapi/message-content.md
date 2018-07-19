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
ms.openlocfilehash: 5e8debcd5a60357f05dfb7b6bde1faf972e50a26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793256"
---
# <a name="message-content"></a><span data-ttu-id="b996c-103">Nachrichteninhalt</span><span class="sxs-lookup"><span data-stu-id="b996c-103">Message Content</span></span>

  
  
<span data-ttu-id="b996c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b996c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b996c-105">Es gibt zwei mögliche Codierung für den Nachrichteninhalt: eine Verwendung von MIME, die andere mit Uuencode.</span><span class="sxs-lookup"><span data-stu-id="b996c-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="b996c-106">MIME ist die bevorzugte Codierung.</span><span class="sxs-lookup"><span data-stu-id="b996c-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="b996c-107">Darüber hinaus definiert MAPI eine Eigenschaft pro Empfänger, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), der steuert, ob die TNEF-Informationen in eine ausgehende Nachricht enthalten sein sollen oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b996c-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="b996c-108">Es bestehen nun also insgesamt vier Arten der Codierung Nachrichteninhalt:</span><span class="sxs-lookup"><span data-stu-id="b996c-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="b996c-109">Mit TNEF MIME-Ermittlung</span><span class="sxs-lookup"><span data-stu-id="b996c-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="b996c-110">Ohne TNEF MIME-Ermittlung</span><span class="sxs-lookup"><span data-stu-id="b996c-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="b996c-111">UUENCODE mit TNEF</span><span class="sxs-lookup"><span data-stu-id="b996c-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="b996c-112">UUENCODE ohne TNEF</span><span class="sxs-lookup"><span data-stu-id="b996c-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="b996c-113">Auswählen von MIME oder Uuencode für ausgehende Nachrichten wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="b996c-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="b996c-114">Die folgenden Eigenschaften werden von TNEF ausgeschlossen: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="b996c-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="b996c-115">Alle anderen Übertragungseinehit Nachrichteneigenschaften sind im TNEF-Datenstrom enthalten.</span><span class="sxs-lookup"><span data-stu-id="b996c-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="b996c-116">Die folgenden Vorschläge sind vorgesehen, um eine Liste der Parameter bereitzustellen, die die Implementierung entscheiden kann, wie unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b996c-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="b996c-117">Ob zum Codieren mithilfe von MIME oder Uuencode für ausgehende Nachrichten: boolean.</span><span class="sxs-lookup"><span data-stu-id="b996c-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="b996c-118">Zeichensatz für ausgehende Nachrichten: Zeichenfolge (kopiert direkt an Charset-Parameter) oder -Enumeration (intern übersetzt Charset-Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="b996c-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

