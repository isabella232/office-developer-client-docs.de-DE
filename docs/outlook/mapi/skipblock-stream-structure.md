---
title: SkipBlock streamstruktur-Datenstrom Struktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282670"
---
# <a name="skipblock-stream-structure"></a>SkipBlock streamstruktur-Datenstrom Struktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine SkipBlock streamstruktur-Stream-Struktur ist ein Datenblock, der mit einer ganzen Zahl beginnt, die die Länge des verbleibenden Blocks angibt. Diese Datenstrom Struktur ist in einem [FieldDefinition streamstruktur](fielddefinition-stream-structure.md) -Stream vorhanden, wenn die Felddefinition im PropDefV2-Format vorliegt. 
  
Der Zweck einer SkipBlock streamstruktur-Datenstrom Struktur hängt von der relativen Position in einer Reihe von like-Strukturen im SkipBlocks Data-Element eines FieldDefinition streamstruktur-Streams ab. Die SkipBlocks-Reihe sollte mindestens eine SkipBlock streamstruktur-Struktur enthalten, die die Reihe beendet und das size-Datenelement gleich 0 aufweist. Wenn die erste Struktur nicht die abschließende Struktur (das heißt, das size-Datenelement ist größer als 0) ist, wird davon ausgegangen, dass die erste Struktur den Feldnamen in Unicode (UTF-16) angibt.
  
Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar folgen einander in der angegebenen Reihenfolge.
  
- Größe: DWORD (4 Bytes), die Größe des Inhaltsdaten Elements in Byte.
    
- Inhalt: ein Bytearray. Die Anzahl dieses Arrays entspricht dem Size-Datenelement. Die Bedeutung des Inhaltsdaten Elements hängt vom Speicherort der SkipBlock streamstruktur-Struktur in der Reihe und der Version von Outlook ab. Wenn die erste SkipBlock streamstruktur-Struktur nicht die abschließende Struktur ist, berücksichtigt Outlook die erste SkipBlock streamstruktur-Struktur als [firstskipblockcontent streamstruktur](firstskipblockcontent-stream-structure.md) -Datenstrom Struktur, die den Feldnamen in Unicode angibt. 
    
## <a name="see-also"></a>Siehe auch



[Outlook-Elemente und-Felder](outlook-items-and-fields.md)
  
[Stream-Strukturen](stream-structures.md)
  
[FieldDefinition streamstruktur-Datenstrom Struktur](fielddefinition-stream-structure.md)
  
[Firstskipblockcontent streamstruktur-Datenstrom Struktur](firstskipblockcontent-stream-structure.md)

