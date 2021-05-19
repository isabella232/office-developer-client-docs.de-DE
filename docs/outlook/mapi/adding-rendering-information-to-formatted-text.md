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
# <a name="adding-rendering-information-to-formatted-text"></a>Hinzufügen von Renderinginformationen zum formatierten Text

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um die Position im formatierten Text anzugeben, an der eine Anlage gerendert wird, müssen Sie eine Sequenz von Platzhalterzeichen in die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft der Nachricht einfügen. Die Platzhaltersequenz besteht aus den folgenden Zeichen:  `\objattph` .
  
 **So fügen Sie Dem formatierten Nachrichtentext Renderinginformationen hinzu**
  
- Fügen Sie beim Schreiben des Textstroms in die **PR_RTF_COMPRESSED-Eigenschaft** der Nachricht die Platzhaltersequenz und ein Leerzeichen an der Position ein, an der die Anlage gerendert werden soll. 
    
- Legen Sie **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) -Eigenschaft jeder Anlage auf einen numerischen Wert fest. Der niedrigste Wert sollte der PR_RENDERING_POSITION **der** ersten Anlage zugewiesen werden, die im formatierten Text angezeigt wird. der höchste Wert für die letzte Anlage. 
    

