---
title: Nachrichteninhalt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5e8debcd5a60357f05dfb7b6bde1faf972e50a26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793256"
---
# <a name="message-content"></a>Nachrichteninhalt

  
  
**Betrifft**: Outlook 
  
Es gibt zwei mögliche Codierung für den Nachrichteninhalt: eine Verwendung von MIME, die andere mit Uuencode. MIME ist die bevorzugte Codierung. Darüber hinaus definiert MAPI eine Eigenschaft pro Empfänger, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), der steuert, ob die TNEF-Informationen in eine ausgehende Nachricht enthalten sein sollen oder nicht. Es bestehen nun also insgesamt vier Arten der Codierung Nachrichteninhalt:
  
- Mit TNEF MIME-Ermittlung
    
- Ohne TNEF MIME-Ermittlung
    
- UUENCODE mit TNEF
    
- UUENCODE ohne TNEF
    
Auswählen von MIME oder Uuencode für ausgehende Nachrichten wurde nicht angegeben.
  
Die folgenden Eigenschaften werden von TNEF ausgeschlossen: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**. Alle anderen Übertragungseinehit Nachrichteneigenschaften sind im TNEF-Datenstrom enthalten.
  
Die folgenden Vorschläge sind vorgesehen, um eine Liste der Parameter bereitzustellen, die die Implementierung entscheiden kann, wie unterstützt:
  
- Ob zum Codieren mithilfe von MIME oder Uuencode für ausgehende Nachrichten: boolean.
    
- Zeichensatz für ausgehende Nachrichten: Zeichenfolge (kopiert direkt an Charset-Parameter) oder -Enumeration (intern übersetzt Charset-Zeichenfolge).
    

