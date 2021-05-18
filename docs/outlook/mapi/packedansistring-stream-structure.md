---
title: PackedAnsiString-Streamstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404505"
---
# <a name="packedansistring-stream-structure"></a>PackedAnsiString-Streamstruktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Datenstromstruktur PackedAnsiString enthält eine ANSI-Darstellung einer Zeichenfolge basierend auf der ANSI-Codeseite des Computers, auf dem Microsoft Outlook ausgeführt wird. Diese Zeichenfolge wird nicht durch ein Nullzeichen beendet. Datenelemente in diesem Datenstrom werden in der Reihenfolge des Little-Endian-Bytes gespeichert und folgen in der unten aufgeführten Reihenfolge unmittelbar aufeinander. Die tatsächlich vorhandenen Datenelemente hängen von der Länge der Zeichenfolge in der ANSI-Darstellung ab.
  
- Für eine Zeichenfolge, deren ANSI-Darstellung weniger als 255 Byte enthält, sind die Datenelemente wie folgt:
    
  - Length: BYTE (1 Byte), die Länge der ANSI-Darstellung der Zeichenfolge in Bytes.
    
  - Characters: Ein Array von CHAR. Die Anzahl dieses Arrays entspricht dem Length-Datenelement. Die Daten im Array sind die ANSI-Darstellung der Zeichenfolge.
    
- Für eine Zeichenfolge, deren ANSI-Darstellung 255 bis 65535 Byte enthält, sind die Datenelemente wie folgt:
    
  - Präfix: BYTE (1 Byte), wert 255 (0xff).
    
  - Länge: WORD (2 Byte), die Länge der ANSI-Darstellung der Zeichenfolge in Bytes.
    
  - Characters: Ein Array von CHAR. Die Anzahl dieses Arrays entspricht dem Length-Datenelement. Die Daten im Array sind die ANSI-Darstellung der Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[Outlook Elemente und Felder](outlook-items-and-fields.md)
  
[Streamstrukturen](stream-structures.md)
  
[FieldDefinition Stream Structure](fielddefinition-stream-structure.md)

