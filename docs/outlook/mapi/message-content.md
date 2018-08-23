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
ms.openlocfilehash: 85bd3f7db53f195295405fb0b02c25f084786a67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586081"
---
# <a name="message-content"></a>Nachrichteninhalt

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    

