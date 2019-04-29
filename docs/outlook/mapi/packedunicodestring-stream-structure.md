---
title: Packedunicodestring streamstruktur-Datenstrom Struktur
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
# <a name="packedunicodestring-stream-structure"></a>Packedunicodestring streamstruktur-Datenstrom Struktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Packedunicodestring streamstruktur-Datenstrom Struktur enthält eine Unicode-Darstellung (UTF-16) einer Zeichenfolge. Diese Zeichenfolge wird nicht durch ein NULL-Zeichen beendet. Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar nach einander in der unten aufgeführten Reihenfolge. Die vorhandenen Datenelemente hängen von der Länge der Zeichenfolge in der UTF-16-Darstellung ab.
  
- Für eine Zeichenfolge, deren UTF-16-Darstellung kleiner als 255 WCHARs, sind die folgenden Datenelemente enthalten:
    
  - Length: BYTE (1 Byte), die Länge in der Anzahl von WCHARs, der UTF-16-Darstellung der Zeichenfolge.
    
  - Characters: ein Array von Typ WCHAR. Die Anzahl dieses Arrays ist gleich dem length-Datenelement. Die Daten im Array sind die UTF-16-Darstellung der Zeichenfolge.
    
- Für eine Zeichenfolge, deren UTF-16-Darstellung 255 bis 65535 WCHARs enthält, lauten die folgenden Datenelemente:
    
  - Prefix: BYTE (1 Byte), der Wert von 255 (0xFF).
    
  - Length: WORD (2 Bytes), die Länge (in WCHARs) der UTF-16-Darstellung der Zeichenfolge.
    
  - Characters: ein Array von Typ WCHAR. Die Anzahl dieses Arrays ist gleich dem length-Datenelement. Die Daten im Array sind die UTF-16-Darstellung der Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[Outlook-Elemente und-Felder](outlook-items-and-fields.md)
  
[Stream-Strukturen](stream-structures.md)
  
[FieldDefinition streamstruktur-Datenstrom Struktur](fielddefinition-stream-structure.md)

