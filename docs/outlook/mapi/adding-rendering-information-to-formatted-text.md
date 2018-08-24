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
ms.openlocfilehash: a6018c05d1191211242066425e4ae546c1618094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594558"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Hinzufügen von Renderinformationen zu formatiertem Text

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um den Speicherort in formatierten Text anzugeben, in dem eine Anlage gerendert wird, müssen Sie in der Nachricht **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft eine Abfolge von Platzhalterzeichen einfügen. Die Platzhalter Sequenz besteht aus der folgenden Zeichen: `\objattph`.
  
 **Von Renderinginformationen zu formatierten Nachrichtentext hinzufügen**
  
- Beim Schreiben des Streams des Texts in der Nachricht **PR_RTF_COMPRESSED** -Eigenschaft fügen Sie die Platzhalter Sequenz und ein Leerzeichen an der Position, in dem die Anlage gerendert werden soll. 
    
- Legen Sie die **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft aller Anlagen in einen numerischen Wert. Der niedrigste Wert sollte die **PR_RENDERING_POSITION** -Eigenschaft der ersten Anlage zugewiesen werden in der formatierte Text angezeigt wird; der höchste Wert auf die letzte Anlage. 
    

