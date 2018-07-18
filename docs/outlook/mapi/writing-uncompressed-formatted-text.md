---
title: Schreiben von nicht komprimiertem formatierten Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9baf3397255d6138caaad84de5ff5621bd6c9555
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795869"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="411c2-103">Schreiben von nicht komprimiertem formatierten Text</span><span class="sxs-lookup"><span data-stu-id="411c2-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="411c2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="411c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="411c2-105">Bei der Vorbereitung zum Senden einer Nachricht mit formatierten Text, legen Sie entweder die Nachricht **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft in komprimierten oder nicht komprimierten Text.</span><span class="sxs-lookup"><span data-stu-id="411c2-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="411c2-106">Schreiben von komprimierten Text in der **PR_RTF_COMPRESSED** -Eigenschaft ist ein sehr CPU-intensiver Vorgang und kann die Leistung erheblich beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="411c2-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="411c2-107">Zur Verbesserung der Leistung der formatierte Nachrichten entweder senden:</span><span class="sxs-lookup"><span data-stu-id="411c2-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="411c2-108">Aktualisieren Sie die CPU, eine Lösung, die nicht immer plausibel ist.</span><span class="sxs-lookup"><span data-stu-id="411c2-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="411c2-109">Oder -</span><span class="sxs-lookup"><span data-stu-id="411c2-109">Or -</span></span>
    
- <span data-ttu-id="411c2-110">Schreiben von nicht komprimierten Text in der **PR_RTF_COMPRESSED** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="411c2-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="411c2-111">Das Verfahren zum Festlegen von **PR_RTF_COMPRESSED** mit nicht komprimierten Text ist die gleichen wie für das Festlegen der Steuerelementvorlage mit komprimierten Text mit einer Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="411c2-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="411c2-112">Beim Aufruf von [WrapCompressedRTFStream](wrapcompressedrtfstream.md)festlegen Sie STORE_UNCOMPRESSED_RTF das Flag im _UlFlags_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="411c2-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="411c2-113">Festlegen der nicht komprimierten Text hat den Nachteil, dass sie die Größe der Nachrichten erhöht.</span><span class="sxs-lookup"><span data-stu-id="411c2-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

