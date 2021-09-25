---
title: SkipBlock-Streamstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fd4dfba1aaa13294fc1a238e9d4cfac28831849e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624209"
---
# <a name="skipblock-stream-structure"></a>SkipBlock-Streamstruktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine SkipBlock-Datenstromstruktur ist ein Datenblock, der mit einer ganzen Zahl beginnt, die die Länge des verbleibenden Teils des Blocks angibt. Diese Datenstromstruktur ist in einem [FieldDefinition-Datenstrom](fielddefinition-stream-structure.md) vorhanden, wenn die Felddefinition das PropDefV2-Format aufweist. 
  
Der Zweck einer SkipBlock-Datenstromstruktur hängt von ihrer relativen Position in einer Reihe von ähnlichen Strukturen im SkipBlocks-Datenelement eines FieldDefinition-Datenstroms ab. Die SkipBlocks-Datenreihe sollte mindestens eine SkipBlock-Struktur enthalten, die die Datenreihe beendet und das Size-Datenelement gleich 0 aufweist. Wenn es sich bei der ersten Struktur nicht um die Endstruktur handelt (das heißt, das Size-Datenelement ist größer als 0), Outlook geht davon aus, dass die erste Struktur den Feldnamen in Unicode (UTF-16) angibt.
  
Datenelemente in diesem Datenstrom werden in kleiner endischer Bytereihenfolge gespeichert und folgen sich direkt in der unten angegebenen Reihenfolge.
  
- Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.
    
- Inhalt: Ein Bytearray. Die Anzahl dieses Arrays ist gleich dem Size-Datenelement. Die Bedeutung des Inhaltsdatenelements hängt vom Speicherort der SkipBlock-Struktur in der Datenreihe und der Version von Outlook ab. Wenn die erste SkipBlock-Struktur nicht die Endstruktur ist, betrachtet Outlook die erste SkipBlock-Struktur als [die FirstSkipBlockContent-Datenstromstruktur,](firstskipblockcontent-stream-structure.md) die den Feldnamen in Unicode angibt. 
    
## <a name="see-also"></a>Siehe auch



[Outlook Elemente und Felder](outlook-items-and-fields.md)
  
[Stream-Strukturen](stream-structures.md)
  
[FieldDefinition-Datenstromstruktur](fielddefinition-stream-structure.md)
  
[FirstSkipBlockContent-Streamstruktur](firstskipblockcontent-stream-structure.md)

