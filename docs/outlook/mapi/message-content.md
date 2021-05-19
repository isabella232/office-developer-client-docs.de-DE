---
title: Nachrichteninhalt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435460"
---
# <a name="message-content"></a>Nachrichteninhalt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt zwei mögliche Codierungen für den Nachrichteninhalt: eine mit MIME, die andere mit uuencode. MIME ist die bevorzugte Codierung. Darüber hinaus definiert MAPI die Eigenschaft **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), die bestimmt, ob #A0 in eine ausgehende Nachricht eingeschlossen werden sollen. Es gibt also insgesamt vier Möglichkeiten zum Codieren von Nachrichteninhalten:
  
- MIME mit TNEF
    
- MIME ohne TNEF
    
- uuencode mit TNEF
    
- uuencode ohne TNEF
    
Es wird nicht angegeben, wie Sie MIME oder uuencode für ausgehende Nachrichten auswählen.
  
Die folgenden Eigenschaften werden von TNEF **ausgeschlossen: \* PR_SENDER_**, **PR_ATTACH_DATA_ \***, **PR_BODY**. Alle anderen nachrichtendurchlässigen Eigenschaften sind im TNEF-Stream enthalten.
  
Die folgenden Vorschläge sollen eine Liste von Parametern bereitstellen, die von der Implementierung unterstützt werden können:
  
- Gibt an, ob mit MIME oder Uuencode für ausgehende Nachrichten codiert werden soll: boolean.
    
- Zeichensatz, der für ausgehende Nachrichten verwendet werden soll: Zeichenfolge (direkt in charset-Parameter kopiert) oder Enumeration (intern in Zeichensatzzeichenfolge übersetzt).
    

