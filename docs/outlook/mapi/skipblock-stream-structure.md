---
title: SkipBlock Stream Structure
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435544"
---
# <a name="skipblock-stream-structure"></a>SkipBlock Stream Structure

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine SkipBlock-Streamstruktur ist ein Datenblock, der mit einer ganzen Zahl beginnt, die die Länge des verbleibenden Teils des Blocks angibt. Diese Datenstromstruktur ist in einem [FieldDefinition-Stream](fielddefinition-stream-structure.md) vorhanden, wenn die Felddefinition im PropDefV2-Format ist. 
  
Der Zweck einer SkipBlock-Streamstruktur hängt von ihrer relativen Position in einer Reihe von gleich großen Strukturen im SkipBlocks-Datenelement eines FieldDefinition-Datenstroms ab. Die SkipBlocks-Reihe sollte mindestens eine SkipBlock-Struktur enthalten, die die Datenreihe beendet und das Size-Datenelement gleich 0 hat. Wenn die erste Struktur nicht die Abschlussstruktur ist (d. h. das Size data-Element ist größer als 0), geht Outlook davon aus, dass die erste Struktur den Feldnamen in Unicode (UTF-16) angibt.
  
Datenelemente in diesem Datenstrom werden in der Bytereihenfolge des Little-Endian-Elements gespeichert und folgen sofort in der unten angegebenen Reihenfolge aufeinander.
  
- Größe: DWORD (4 Byte), die Größe des Content-Datenelements in Bytes.
    
- Inhalt: Ein Array von BYTE. Die Anzahl dieses Arrays entspricht dem Size-Datenelement. Die Bedeutung des Inhaltsdatenelements hängt vom Speicherort der SkipBlock-Struktur in der Datenreihe und der Version des Outlook. Wenn die erste SkipBlock-Struktur nicht die Abschlussstruktur ist, betrachtet Outlook die erste SkipBlock-Struktur als [FirstSkipBlockContent-Streamstruktur,](firstskipblockcontent-stream-structure.md) die den Feldnamen in Unicode angibt. 
    
## <a name="see-also"></a>Siehe auch



[Outlook Elemente und Felder](outlook-items-and-fields.md)
  
[Streamstrukturen](stream-structures.md)
  
[FieldDefinition Stream Structure](fielddefinition-stream-structure.md)
  
[FirstSkipBlockContent Stream Structure](firstskipblockcontent-stream-structure.md)

