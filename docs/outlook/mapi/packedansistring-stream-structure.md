---
title: Packedansistring streamstruktur-Datenstrom Struktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348510"
---
# <a name="packedansistring-stream-structure"></a>Packedansistring streamstruktur-Datenstrom Struktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Packedansistring streamstruktur-Datenstrom Struktur enthält eine ANSI-Darstellung einer Zeichenfolge, die auf der ANSI-Codeseite des Computers basiert, auf dem Microsoft Outlook läuft. Diese Zeichenfolge wird nicht durch ein NULL-Zeichen beendet. Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar nach einander in der unten aufgeführten Reihenfolge. Die tatsächlichen Datenelemente, die vorhanden sind, hängen von der Länge der Zeichenfolge in der ANSI-Darstellung ab.
  
- Bei einer Zeichenfolge, deren ANSI-Darstellung kleiner als 255 Byte ist, sind die folgenden Datenelemente enthalten:
    
  - Length: BYTE (1 Byte), die Länge der ANSI-Darstellung der Zeichenfolge in Byte.
    
  - Characters: ein Array von CHAR. Die Anzahl dieses Arrays ist gleich dem length-Datenelement. Die Daten im Array sind die ANSI-Darstellung der Zeichenfolge.
    
- Für eine Zeichenfolge, deren ANSI-Darstellung 255 bis 65535 Byte enthält, lauten die folgenden Datenelemente:
    
  - Prefix: BYTE (1 Byte), der Wert von 255 (0xFF).
    
  - Length: WORD (2 Bytes), die Länge der ANSI-Darstellung der Zeichenfolge in Byte.
    
  - Characters: ein Array von CHAR. Die Anzahl dieses Arrays ist gleich dem length-Datenelement. Die Daten im Array sind die ANSI-Darstellung der Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[Outlook-Elemente und-Felder](outlook-items-and-fields.md)
  
[Stream-Strukturen](stream-structures.md)
  
[FieldDefinition streamstruktur-Datenstrom Struktur](fielddefinition-stream-structure.md)

