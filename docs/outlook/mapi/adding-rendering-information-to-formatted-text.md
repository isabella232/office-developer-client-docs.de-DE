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
# <a name="adding-rendering-information-to-formatted-text"></a>Hinzufügen von Informationen zum Rendern formatierter Text

  
  
**Betrifft**: Outlook 
  
Um den Speicherort in formatierten Text anzugeben, in dem eine Anlage gerendert wird, müssen Sie in der Nachricht **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft eine Abfolge von Platzhalterzeichen einfügen. Die Platzhalter Sequenz besteht aus der folgenden Zeichen: `\objattph`.
  
 **Von Renderinginformationen zu formatierten Nachrichtentext hinzufügen**
  
- Beim Schreiben des Streams des Texts in der Nachricht **PR_RTF_COMPRESSED** -Eigenschaft fügen Sie die Platzhalter Sequenz und ein Leerzeichen an der Position, in dem die Anlage gerendert werden soll. 
    
- Legen Sie die **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft aller Anlagen in einen numerischen Wert. Der niedrigste Wert sollte die **PR_RENDERING_POSITION** -Eigenschaft der ersten Anlage zugewiesen werden in der formatierte Text angezeigt wird; der höchste Wert auf die letzte Anlage. 
    

