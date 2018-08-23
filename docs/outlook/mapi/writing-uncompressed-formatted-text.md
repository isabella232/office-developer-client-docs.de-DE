---
title: Schreiben von nicht komprimiertem formatierten Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d34168743926681ee7169a593e302755b193aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577044"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="d4ca0-103">Schreiben von nicht komprimiertem formatierten Text</span><span class="sxs-lookup"><span data-stu-id="d4ca0-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="d4ca0-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4ca0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4ca0-105">Bei der Vorbereitung zum Senden einer Nachricht mit formatierten Text, legen Sie entweder die Nachricht **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft in komprimierten oder nicht komprimierten Text.</span><span class="sxs-lookup"><span data-stu-id="d4ca0-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="d4ca0-106">Schreiben von komprimierten Text in der **PR_RTF_COMPRESSED** -Eigenschaft ist ein sehr CPU-intensiver Vorgang und kann die Leistung erheblich beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="d4ca0-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="d4ca0-107">Zur Verbesserung der Leistung der formatierte Nachrichten entweder senden:</span><span class="sxs-lookup"><span data-stu-id="d4ca0-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="d4ca0-108">Aktualisieren Sie die CPU, eine Lösung, die nicht immer plausibel ist.</span><span class="sxs-lookup"><span data-stu-id="d4ca0-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="d4ca0-109">Oder -</span><span class="sxs-lookup"><span data-stu-id="d4ca0-109">Or -</span></span>
    
- <span data-ttu-id="d4ca0-110">Schreiben von nicht komprimierten Text in der **PR_RTF_COMPRESSED** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d4ca0-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="d4ca0-111">Das Verfahren zum Festlegen von **PR_RTF_COMPRESSED** mit nicht komprimierten Text ist die gleichen wie für das Festlegen der Steuerelementvorlage mit komprimierten Text mit einer Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="d4ca0-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="d4ca0-112">Beim Aufruf von [WrapCompressedRTFStream](wrapcompressedrtfstream.md)festlegen Sie STORE_UNCOMPRESSED_RTF das Flag im _UlFlags_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="d4ca0-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="d4ca0-113">Festlegen der nicht komprimierten Text hat den Nachteil, dass sie die Größe der Nachrichten erhöht.</span><span class="sxs-lookup"><span data-stu-id="d4ca0-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

