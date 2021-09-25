---
title: PackedUnicodeString-Datenstromstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 73a3f6f8ca3dd23326f28ea18228c09cf310d444
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625119"
---
# <a name="packedunicodestring-stream-structure"></a>PackedUnicodeString-Datenstromstruktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die PackedUnicodeString-Datenstromstruktur enthält eine Unicode-Darstellung (UTF-16) einer Zeichenfolge. Diese Zeichenfolge wird nicht durch ein NULL-Zeichen beendet. Datenelemente in diesem Datenstrom werden in der Reihenfolge der kleinen Endbytes gespeichert und folgen einander in der unten aufgeführten Reihenfolge. Die tatsächlich vorhandenen Datenelemente hängen von der Länge der Zeichenfolge in der UTF-16-Darstellung ab.
  
- Für eine Zeichenfolge, deren UTF-16-Darstellung weniger als 255 WCHARs enthält, sind die Datenelemente wie folgt:
    
  - Length: BYTE (1 Byte), die Länge der UTF-16-Darstellung der Zeichenfolge in Anzahl der WCHARs.
    
  - Zeichen: Ein Array von WCHAR. Die Anzahl dieses Arrays entspricht dem Length-Datenelement. Die Daten im Array sind die UTF-16-Darstellung der Zeichenfolge.
    
- Für eine Zeichenfolge, deren UTF-16-Darstellung 255 bis 65535 WCHARs enthält, sind die Datenelemente wie folgt:
    
  - Präfix: BYTE (1 Byte), der Wert von 255 (0xff).
    
  - Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.
    
  - Zeichen: Ein Array von WCHAR. Die Anzahl dieses Arrays entspricht dem Length-Datenelement. Die Daten im Array sind die UTF-16-Darstellung der Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[Outlook Elemente und Felder](outlook-items-and-fields.md)
  
[Stream-Strukturen](stream-structures.md)
  
[FieldDefinition-Datenstromstruktur](fielddefinition-stream-structure.md)

