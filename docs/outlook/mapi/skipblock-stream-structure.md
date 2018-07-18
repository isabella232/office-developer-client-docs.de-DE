---
title: SkipBlock-Streamstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d84704300602bada4cf93c9d3f6622feaf16f352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795562"
---
# <a name="skipblock-stream-structure"></a>SkipBlock-Streamstruktur

  
  
**Betrifft**: Outlook 
  
Eine SkipBlock Stream-Struktur ist ein Block von Daten, die mit einer ganzen Zahl beginnt, der die Länge des den verbleibenden Teil des Blocks angibt. Diese Struktur Stream ist in einem Stream [FieldDefinition](fielddefinition-stream-structure.md) vorhanden, wenn die Felddefinition im PropDefV2-Format vorliegt. 
  
Der Zweck der eine SkipBlock Stream-Struktur hängt die relative Position in einer Reihe von wie Strukturen in der SkipBlocks Data-Element eines FieldDefinition Stream-Objekts. Die Datenreihe SkipBlocks sollte mindestens eine SkipBlock Struktur enthalten, die beendet die Datenreihe und hat das Datenelement Größe gleich 0. Wenn die erste Struktur nicht die abschließende Struktur ist (d. h., das Größe der Data-Element ist größer als 0), Outlook geht davon aus, die erste Struktur gibt der Name des Felds in Unicode (UTF-16).
  
Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der angegebenen Reihenfolge gespeichert.
  
- Größe: DWORD-Wert (4 Bytes), die Größe des Elements Inhaltsdaten als Byteanzahl angegeben.
    
- Inhalt: Ein Array von BYTE. Die Anzahl der dieses Array ist gleich der Größe der Data-Element. Die Bedeutung des Elements Inhaltsdaten hängt davon ab, den Speicherort der SkipBlock Struktur in der Datenreihe und die Version von Outlook. Ist die erste SkipBlock-Struktur nicht den Abbruch Struktur, betrachtet Outlook die erste SkipBlock Struktur als der [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) Stream-Struktur, die in Unicode der Name des Felds angibt. 
    
## <a name="see-also"></a>Siehe auch



[Elemente und Felder in Outlook](outlook-items-and-fields.md)
  
[Streamstrukturen](stream-structures.md)
  
[FieldDefinition-Streamstruktur](fielddefinition-stream-structure.md)
  
[FirstSkipBlockContent-Streamstruktur](firstskipblockcontent-stream-structure.md)

