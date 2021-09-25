---
title: Nachrichteninhalt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b1523d230ae49e8ca779bab12e5ce6264f6300dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592060"
---
# <a name="message-content"></a>Nachrichteninhalt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt zwei mögliche Codierungen für den Nachrichteninhalt: eine mitHILFE von MIME, die andere mit uuencode. MIME ist die bevorzugte Codierung. Darüber hinaus definiert mapi eine Eigenschaft **pro** Empfänger, PR_SEND_RICH_INFO ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), die bestimmt, ob TNEF-Informationen in eine ausgehende Nachricht eingeschlossen werden sollen. Es gibt also insgesamt vier Möglichkeiten zum Codieren von Nachrichteninhalten:
  
- MIME mit TNEF
    
- MIME ohne TNEF
    
- uuencode with TNEF
    
- uuencode ohne TNEF
    
Es wird nicht angegeben, wie MIME oder uuencode für ausgehende Nachrichten ausgewählt wird.
  
Die folgenden Eigenschaften werden von TNEF ausgeschlossen: **PR_SENDER_ \* *_, _* PR_ATTACH_DATA_ \* *_, _* PR_BODY**. Alle anderen übertragungsfähigen Nachrichteneigenschaften sind im TNEF-Stream enthalten.
  
Die folgenden Vorschläge dienen zur Bereitstellung einer Liste von Parametern, die von der Implementierung unterstützt werden können:
  
- Gibt an, ob sie mithilfe von MIME oder uuencode für ausgehende Nachrichten codiert werden sollen: boolescher Wert.
    
- Zeichensatz für ausgehende Nachrichten: Zeichenfolge (direkt in charset-Parameter kopiert) oder Enumeration (intern in Zeichensatzzeichenfolge übersetzt).
    

