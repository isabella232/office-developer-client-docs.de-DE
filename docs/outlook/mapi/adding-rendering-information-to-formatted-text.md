---
title: Hinzufügen von Renderinginformationen zum formatierten Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a67fc7cbb3be5c7a23cb85e60dc33d853614cda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420612"
---
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="3adb7-103">Hinzufügen von Renderinginformationen zum formatierten Text</span><span class="sxs-lookup"><span data-stu-id="3adb7-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="3adb7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3adb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3adb7-105">Um die Position im formatierten Text anzugeben, an der eine Anlage gerendert wird, müssen Sie eine Sequenz von Platzhalterzeichen in die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft der Nachricht einfügen.</span><span class="sxs-lookup"><span data-stu-id="3adb7-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="3adb7-106">Die Platzhaltersequenz besteht aus den folgenden Zeichen:  `\objattph` .</span><span class="sxs-lookup"><span data-stu-id="3adb7-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="3adb7-107">**So fügen Sie Dem formatierten Nachrichtentext Renderinginformationen hinzu**</span><span class="sxs-lookup"><span data-stu-id="3adb7-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="3adb7-108">Fügen Sie beim Schreiben des Textstroms in die **PR_RTF_COMPRESSED-Eigenschaft** der Nachricht die Platzhaltersequenz und ein Leerzeichen an der Position ein, an der die Anlage gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3adb7-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="3adb7-109">Legen Sie **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) -Eigenschaft jeder Anlage auf einen numerischen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="3adb7-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="3adb7-110">Der niedrigste Wert sollte der PR_RENDERING_POSITION **der** ersten Anlage zugewiesen werden, die im formatierten Text angezeigt wird. der höchste Wert für die letzte Anlage.</span><span class="sxs-lookup"><span data-stu-id="3adb7-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

