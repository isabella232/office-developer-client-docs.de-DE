---
title: Hinzufügen von Informationen zum Rendern formatierter Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b912d81c1413fb40b6ddccc2f54bc393a6b67857
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791265"
---
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="09946-103">Hinzufügen von Informationen zum Rendern formatierter Text</span><span class="sxs-lookup"><span data-stu-id="09946-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="09946-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09946-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09946-105">Um den Speicherort in formatierten Text anzugeben, in dem eine Anlage gerendert wird, müssen Sie in der Nachricht **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft eine Abfolge von Platzhalterzeichen einfügen.</span><span class="sxs-lookup"><span data-stu-id="09946-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="09946-106">Die Platzhalter Sequenz besteht aus der folgenden Zeichen: `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="09946-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="09946-107">**Von Renderinginformationen zu formatierten Nachrichtentext hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="09946-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="09946-108">Beim Schreiben des Streams des Texts in der Nachricht **PR_RTF_COMPRESSED** -Eigenschaft fügen Sie die Platzhalter Sequenz und ein Leerzeichen an der Position, in dem die Anlage gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="09946-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="09946-109">Legen Sie die **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft aller Anlagen in einen numerischen Wert.</span><span class="sxs-lookup"><span data-stu-id="09946-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="09946-110">Der niedrigste Wert sollte die **PR_RENDERING_POSITION** -Eigenschaft der ersten Anlage zugewiesen werden in der formatierte Text angezeigt wird; der höchste Wert auf die letzte Anlage.</span><span class="sxs-lookup"><span data-stu-id="09946-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

