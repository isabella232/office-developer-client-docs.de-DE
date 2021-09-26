---
title: Hinzufügen von Renderinginformationen zu formatiertem Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d19ff541ac13a5d18216cc512f2824176ca7727a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631104"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Hinzufügen von Renderinginformationen zu formatiertem Text

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um die Position in formatiertem Text anzugeben, an der eine Anlage gerendert wird, müssen Sie eine Folge von Platzhalterzeichen in die **Eigenschaft PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) der Nachricht einfügen. Die Platzhaltersequenz besteht aus den folgenden Zeichen:  `\objattph` .
  
 **So fügen Sie dem formatierten Nachrichtentext Renderinginformationen hinzu**
  
- Wenn Sie den Textstrom in die **PR_RTF_COMPRESSED** Eigenschaft der Nachricht schreiben, fügen Sie die Platzhaltersequenz und ein Leerzeichen an der Position ein, an der die Anlage gerendert werden soll. 
    
- Legen Sie die **eigenschaft PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) jeder Anlage auf einen numerischen Wert fest. Der niedrigste Wert sollte der **PR_RENDERING_POSITION** Eigenschaft der ersten Anlage zugewiesen werden, die im formatierten Text angezeigt wird. der höchste Wert für die letzte Anlage. 
    

