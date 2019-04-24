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
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357001"
---
# <a name="message-content"></a><span data-ttu-id="9d586-103">Nachrichteninhalt</span><span class="sxs-lookup"><span data-stu-id="9d586-103">Message Content</span></span>

  
  
<span data-ttu-id="9d586-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d586-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d586-105">Für den Nachrichteninhalt gibt es zwei mögliche Codierungen: eine mit MIME, die andere mit UUEncode.</span><span class="sxs-lookup"><span data-stu-id="9d586-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="9d586-106">MIME ist die bevorzugte Codierung.</span><span class="sxs-lookup"><span data-stu-id="9d586-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="9d586-107">Darüber hinaus definiert MAPI eine empfängerspezifische Eigenschaft, **PR_SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md)), die bestimmt, ob TNEF-Informationen in eine ausgehende Nachricht aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9d586-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="9d586-108">Es gibt also insgesamt vier Möglichkeiten zum Codieren von Nachrichteninhalten:</span><span class="sxs-lookup"><span data-stu-id="9d586-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="9d586-109">MIME mit TNEF</span><span class="sxs-lookup"><span data-stu-id="9d586-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="9d586-110">MIME ohne TNEF</span><span class="sxs-lookup"><span data-stu-id="9d586-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="9d586-111">UUEncode mit TNEF</span><span class="sxs-lookup"><span data-stu-id="9d586-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="9d586-112">UUEncode ohne TNEF</span><span class="sxs-lookup"><span data-stu-id="9d586-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="9d586-113">Das Auswählen von MIME oder UUENCODE für ausgehende Nachrichten wird nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="9d586-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="9d586-114">Die folgenden Eigenschaften sind aus TNEF ausgeschlossen: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="9d586-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="9d586-115">Alle anderen übertragenen Nachrichteneigenschaften sind im TNEF-Stream enthalten.</span><span class="sxs-lookup"><span data-stu-id="9d586-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="9d586-116">Die folgenden Vorschläge sollen eine Liste von Parametern enthalten, die die Implementierung für die Unterstützung entscheiden kann:</span><span class="sxs-lookup"><span data-stu-id="9d586-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="9d586-117">Ob mit MIME oder UUENCODE für ausgehende Nachrichten codiert werden soll: Boolean.</span><span class="sxs-lookup"><span data-stu-id="9d586-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="9d586-118">Zeichensatz für ausgehende Nachrichten: Zeichenfolge (direkt in den Charset-Parameter kopiert) oder Enumeration (intern in charset-Zeichenfolge übersetzt).</span><span class="sxs-lookup"><span data-stu-id="9d586-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

