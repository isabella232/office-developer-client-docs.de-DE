---
title: PackedUnicodeString-Datenstromstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fc20c259f30ded2f96f3bf314e74207bebcac980
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422614"
---
# <a name="packedunicodestring-stream-structure"></a>PackedUnicodeString-Datenstromstruktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Datenstromstruktur PackedUnicodeString enthält eine Unicode-Darstellung (UTF-16) einer Zeichenfolge. Diese Zeichenfolge wird nicht durch ein Nullzeichen beendet. Datenelemente in diesem Datenstrom werden in der Reihenfolge des Little-Endian-Bytes gespeichert und folgen in der unten aufgeführten Reihenfolge unmittelbar aufeinander. Die tatsächlich vorhandenen Datenelemente hängen von der Länge der Zeichenfolge in der UTF-16-Darstellung ab.
  
- Für eine Zeichenfolge, deren UTF-16-Darstellung weniger als 255 WCHARs enthält, sind die Datenelemente wie folgt:
    
  - Länge: BYTE (1 Byte), die Länge in der Anzahl der WCHARs der UTF-16-Darstellung der Zeichenfolge.
    
  - Characters: Ein Array von WCHAR. Die Anzahl dieses Arrays entspricht dem Length-Datenelement. Die Daten im Array sind die UTF-16-Darstellung der Zeichenfolge.
    
- Für eine Zeichenfolge, deren UTF-16-Darstellung 255 bis 65535 WCHARs enthält, sind die Datenelemente wie folgt:
    
  - Präfix: BYTE (1 Byte), wert 255 (0xff).
    
  - Länge: WORD (2 Byte), die Länge in der Anzahl der WCHARs der UTF-16-Darstellung der Zeichenfolge.
    
  - Characters: Ein Array von WCHAR. Die Anzahl dieses Arrays entspricht dem Length-Datenelement. Die Daten im Array sind die UTF-16-Darstellung der Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[Outlook Elemente und Felder](outlook-items-and-fields.md)
  
[Streamstrukturen](stream-structures.md)
  
[FieldDefinition Stream Structure](fielddefinition-stream-structure.md)

