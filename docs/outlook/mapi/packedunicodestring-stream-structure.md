---
title: PackedUnicodeString-Streamstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2b4dcdcb50fb04410ed93940b46ea7a0d74fff41
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793333"
---
# <a name="packedunicodestring-stream-structure"></a>PackedUnicodeString-Streamstruktur

  
  
**Betrifft**: Outlook 
  
Die PackedUnicodeString Stream-Datenstruktur enthält eine Unicode (UTF-16) Darstellung einer Zeichenfolge. Diese Zeichenfolge wird durch ein Null-Zeichen nicht abgeschlossen. Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der folgenden Reihenfolge gespeichert. Die tatsächlichen Datenelemente, die vorhanden hängen die Länge der Zeichenfolge in UTF-16 Darstellung.
  
- Nach einer Zeichenfolge, deren Darstellung UTF-16 weniger als 255 WCHARs so lang wie enthält, werden die Elemente wie folgt:
    
  - Länge: BYTE (1 Byte), die Länge in WCHARs so lang wie, Anzahl der UTF-16 Darstellung der Zeichenfolge.
    
  - Zeichen: Ein Array von WCHAR. Die Anzahl der dieses Array ist gleich der Länge Data-Element. Die Daten im Array ist die UTF-16-Darstellung der Zeichenfolge.
    
- Nach einer Zeichenfolge, deren Darstellung UTF-16 255 und 65535 WCHARs so lang wie enthält, werden die Elemente wie folgt:
    
  - Präfix: BYTE (1 Byte) der Wert der 255 (0xff).
    
  - Länge: Wort (2 Bytes), die Länge in WCHARs so lang wie, Anzahl der UTF-16 Darstellung der Zeichenfolge.
    
  - Zeichen: Ein Array von WCHAR. Die Anzahl der dieses Array ist gleich der Länge Data-Element. Die Daten im Array ist die UTF-16-Darstellung der Zeichenfolge.
    
## <a name="see-also"></a>Siehe auch



[Elemente und Felder in Outlook](outlook-items-and-fields.md)
  
[Streamstrukturen](stream-structures.md)
  
[FieldDefinition-Streamstruktur](fielddefinition-stream-structure.md)

