---
title: Hinzufügen von Renderinformationen zu formatiertem Text
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
# <a name="adding-rendering-information-to-formatted-text"></a>Hinzufügen von Renderinformationen zu formatiertem Text

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um die Position in formatiertem Text anzugeben, an dem eine Anlage gerendert wird, müssen Sie in der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft der Nachricht eine Sequenz von Platzhalterzeichen einfügen. Die Platzhalter Sequenz besteht aus den folgenden Zeichen: `\objattph`.
  
 **So fügen Sie dem formatierten Nachrichtentext Renderinginformationen hinzu**
  
- Beim Schreiben des Textflusses in die **PR_RTF_COMPRESSED** -Eigenschaft der Nachricht fügen Sie die Platzhalter Sequenz und ein Leerzeichen an der Position ein, an der die Anlage gerendert werden soll. 
    
- Legen Sie die **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md))-Eigenschaft jeder Anlage auf einen numerischen Wert fest. Der niedrigste Wert sollte der **PR_RENDERING_POSITION** -Eigenschaft der ersten Anlage zugewiesen werden, die im formatierten Text angezeigt werden soll. der höchste Wert für die letzte Anlage. 
    

