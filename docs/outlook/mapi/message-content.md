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
  
Für den Nachrichteninhalt gibt es zwei mögliche Codierungen: eine mit MIME, die andere mit UUEncode. MIME ist die bevorzugte Codierung. Darüber hinaus definiert MAPI eine empfängerspezifische Eigenschaft, **PR_SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md)), die bestimmt, ob TNEF-Informationen in eine ausgehende Nachricht aufgenommen werden sollen. Es gibt also insgesamt vier Möglichkeiten zum Codieren von Nachrichteninhalten:
  
- MIME mit TNEF
    
- MIME ohne TNEF
    
- UUEncode mit TNEF
    
- UUEncode ohne TNEF
    
Das Auswählen von MIME oder UUENCODE für ausgehende Nachrichten wird nicht angegeben.
  
Die folgenden Eigenschaften sind aus TNEF ausgeschlossen: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**. Alle anderen übertragenen Nachrichteneigenschaften sind im TNEF-Stream enthalten.
  
Die folgenden Vorschläge sollen eine Liste von Parametern enthalten, die die Implementierung für die Unterstützung entscheiden kann:
  
- Ob mit MIME oder UUENCODE für ausgehende Nachrichten codiert werden soll: Boolean.
    
- Zeichensatz für ausgehende Nachrichten: Zeichenfolge (direkt in den Charset-Parameter kopiert) oder Enumeration (intern in charset-Zeichenfolge übersetzt).
    

