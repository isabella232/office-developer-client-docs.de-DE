---
title: Schreiben von nicht komprimierten formatierten Texten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426324"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="5411c-103">Schreiben von nicht komprimierten formatierten Texten</span><span class="sxs-lookup"><span data-stu-id="5411c-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="5411c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5411c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5411c-105">Wenn Sie das Senden einer Nachricht mit formatiertem Text **vorbereiten,** legen Sie entweder die eigenschaft PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) der Nachricht auf komprimierten oder nicht komprimierten Text festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5411c-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="5411c-106">Das Schreiben von komprimiertem Text in **PR_RTF_COMPRESSED** ist ein sehr CPU-intensiver Vorgang und kann sich erheblich auf die Leistung auswirken.</span><span class="sxs-lookup"><span data-stu-id="5411c-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="5411c-107">Um die Leistung des Sendens formatierter Nachrichten zu verbessern, führen Sie entweder die</span><span class="sxs-lookup"><span data-stu-id="5411c-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="5411c-108">Aktualisieren Sie die CPU, eine Lösung, die nicht immer plausibel ist.</span><span class="sxs-lookup"><span data-stu-id="5411c-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="5411c-109">Oder -</span><span class="sxs-lookup"><span data-stu-id="5411c-109">Or -</span></span>
    
- <span data-ttu-id="5411c-110">Schreiben Sie unkomprimierten Text in die **PR_RTF_COMPRESSED** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5411c-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="5411c-111">Das Verfahren zum Festlegen **PR_RTF_COMPRESSED** mit nicht komprimiertem Text ist identisch mit dem Festlegen mit komprimiertem Text, mit einer Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="5411c-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="5411c-112">Legen Sie [beim Aufrufen von WrapCompressedRTFStream](wrapcompressedrtfstream.md)das STORE_UNCOMPRESSED_RTF im  _ulFlags-Parameter_ ein.</span><span class="sxs-lookup"><span data-stu-id="5411c-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="5411c-113">Das Festlegen von nicht komprimierten Text hat den Nachteil, dass die Größe von Nachrichten erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="5411c-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

