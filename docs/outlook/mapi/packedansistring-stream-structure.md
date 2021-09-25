---
title: PackedAnsiString-Datenstromstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 053983e7909c850bd18e023af43bb5a7acd52e6a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555902"
---
# <a name="packedansistring-stream-structure"></a>PackedAnsiString-Datenstromstruktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die PackedAnsiString-Datenstromstruktur enthält eine ANSI-Darstellung einer Zeichenfolge, basierend auf der ANSI-Codeseite des Computers, auf dem Microsoft Outlook ausgeführt wird. Diese Zeichenfolge wird nicht durch ein NULL-Zeichen beendet. Datenelemente in diesem Datenstrom werden in der Reihenfolge der kleinen Endbytes gespeichert und folgen einander in der unten aufgeführten Reihenfolge. Die tatsächlichen Datenelemente, die vorhanden sind, hängen von der Länge der Zeichenfolge in der ANSI-Darstellung ab.
  
- Für eine Zeichenfolge, deren ANSI-Darstellung weniger als 255 Byte enthält, sind die Datenelemente wie folgt:
    
  - Length: BYTE (1 Byte), die Länge der ANSI-Darstellung der Zeichenfolge in Byte.
    
  - Zeichen: Ein Array von CHAR. Die Anzahl dieses Arrays entspricht dem Length-Datenelement. Die Daten im Array sind die ANSI-Darstellung der Zeichenfolge.
    
- Für eine Zeichenfolge, deren ANSI-Darstellung 255 bis 65535 Byte enthält, sind die Datenelemente wie folgt:
    
  - Präfix: BYTE (1 Byte), der Wert von 255 (0xff).
    
  - Länge: WORD (2 Bytes), die Länge der ANSI-Darstellung der Zeichenfolge in Byte.
    
  - Zeichen: Ein Array von CHAR. Die Anzahl dieses Arrays entspricht dem Length-Datenelement. Die Daten im Array sind die ANSI-Darstellung der Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[Outlook Elemente und Felder](outlook-items-and-fields.md)
  
[Stream-Strukturen](stream-structures.md)
  
[FieldDefinition-Datenstromstruktur](fielddefinition-stream-structure.md)

