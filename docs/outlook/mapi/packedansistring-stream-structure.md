---
title: PackedAnsiString-Streamstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4e919270efb196cda845581830cc4a918012b385
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578976"
---
# <a name="packedansistring-stream-structure"></a>PackedAnsiString-Streamstruktur

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die PackedAnsiString Stream-Datenstruktur enthält eine ANSI-Darstellung einer Zeichenfolge, die basierend auf der ANSI-Codeseite des Computers, auf dem Microsoft Outlook ausgeführt wird. Diese Zeichenfolge wird durch ein Null-Zeichen nicht abgeschlossen. Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der folgenden Reihenfolge gespeichert. Die tatsächlichen Datenelemente, die vorhanden hängen die Länge der Zeichenfolge in ANSI-Darstellung.
  
- Nach einer Zeichenfolge, deren Darstellung ANSI höchstens 255 Bytes enthält, werden die Elemente wie folgt:
    
  - Länge: BYTE (1 Byte), die Länge als Byteanzahl angegeben, der die ANSI-Darstellung der Zeichenfolge.
    
  - Zeichen: Ein Array von CHAR. Die Anzahl der dieses Array ist gleich der Länge Data-Element. Die Daten im Array ist die ANSI-Darstellung der Zeichenfolge.
    
- Nach einer Zeichenfolge, deren Darstellung ANSI 255 und 65535 Bytes enthält, werden die Elemente wie folgt:
    
  - Präfix: BYTE (1 Byte) der Wert der 255 (0xff).
    
  - Länge: Wort (2 Bytes), die Länge als Byteanzahl angegeben, der die ANSI-Darstellung der Zeichenfolge.
    
  - Zeichen: Ein Array von CHAR. Die Anzahl der dieses Array ist gleich der Länge Data-Element. Die Daten im Array ist die ANSI-Darstellung der Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[Elemente und Felder in Outlook](outlook-items-and-fields.md)
  
[Streamstrukturen](stream-structures.md)
  
[FieldDefinition-Streamstruktur](fielddefinition-stream-structure.md)

