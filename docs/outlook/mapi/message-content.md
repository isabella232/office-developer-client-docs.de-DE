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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435460"
---
# <a name="message-content"></a><span data-ttu-id="c49c3-103">Nachrichteninhalt</span><span class="sxs-lookup"><span data-stu-id="c49c3-103">Message Content</span></span>

  
  
<span data-ttu-id="c49c3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c49c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c49c3-105">Es gibt zwei mögliche Codierungen für den Nachrichteninhalt: eine mit MIME, die andere mit uuencode.</span><span class="sxs-lookup"><span data-stu-id="c49c3-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="c49c3-106">MIME ist die bevorzugte Codierung.</span><span class="sxs-lookup"><span data-stu-id="c49c3-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="c49c3-107">Darüber hinaus definiert MAPI die Eigenschaft **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), die bestimmt, ob #A0 in eine ausgehende Nachricht eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c49c3-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="c49c3-108">Es gibt also insgesamt vier Möglichkeiten zum Codieren von Nachrichteninhalten:</span><span class="sxs-lookup"><span data-stu-id="c49c3-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="c49c3-109">MIME mit TNEF</span><span class="sxs-lookup"><span data-stu-id="c49c3-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="c49c3-110">MIME ohne TNEF</span><span class="sxs-lookup"><span data-stu-id="c49c3-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="c49c3-111">uuencode mit TNEF</span><span class="sxs-lookup"><span data-stu-id="c49c3-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="c49c3-112">uuencode ohne TNEF</span><span class="sxs-lookup"><span data-stu-id="c49c3-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="c49c3-113">Es wird nicht angegeben, wie Sie MIME oder uuencode für ausgehende Nachrichten auswählen.</span><span class="sxs-lookup"><span data-stu-id="c49c3-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="c49c3-114">Die folgenden Eigenschaften werden von TNEF **ausgeschlossen: \* PR_SENDER_**, **PR_ATTACH_DATA_ \***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="c49c3-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="c49c3-115">Alle anderen nachrichtendurchlässigen Eigenschaften sind im TNEF-Stream enthalten.</span><span class="sxs-lookup"><span data-stu-id="c49c3-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="c49c3-116">Die folgenden Vorschläge sollen eine Liste von Parametern bereitstellen, die von der Implementierung unterstützt werden können:</span><span class="sxs-lookup"><span data-stu-id="c49c3-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="c49c3-117">Gibt an, ob mit MIME oder Uuencode für ausgehende Nachrichten codiert werden soll: boolean.</span><span class="sxs-lookup"><span data-stu-id="c49c3-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="c49c3-118">Zeichensatz, der für ausgehende Nachrichten verwendet werden soll: Zeichenfolge (direkt in charset-Parameter kopiert) oder Enumeration (intern in Zeichensatzzeichenfolge übersetzt).</span><span class="sxs-lookup"><span data-stu-id="c49c3-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

