---
title: PropertyDefinition-Stream-Beispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328504"
---
# <a name="propertydefinition-stream-sample"></a>PropertyDefinition-Stream-Beispiel

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird ein Beispiel für einen PropertyDefinition-Stream beschrieben. Der Stream enthält eine Definition eines benutzerdefinierten Felds `TextField1`. Der Typ ist **Text**, und die Definition befindet sich im PropDefV2-Format.
  
## <a name="data-dump"></a>Daten Dump

Es folgt ein Daten Dump des Streams, wie er in einem binären Editor angezeigt würde.
  
|Datenstrom Offset|Datenbytes|ASCII-Daten|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
Es folgt eine Analyse der Beispieldaten für den PropertyDefinition-Stream:
  
- Version: Offset 0x0 festlegen, 2 Bytes: 0x0103 (PropDefV2).
    
- FieldDefinitionCount: Offset 0x2, 4 Bytes: 0x1 (1).
    
- FieldDefinitions: Offset 0x6, Array of 1 FieldDefinition streamstruktur Stream.
    
  - Flags: Offset 0x6 bytes: 0x45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).
    
  - VT: Offset 0xA, 2 Bytes: 0x8 (**VT_BSTR**).
    
  - DispId: Offset 0xC bytes: 0x0 festlegen (0).
    
  - NmidNameLength: Offset 0x10, 2 Bytes: 0xA (10).
    
  - NmidName: Offset 0x12, Array von 10 WCHARs. Unicode-Zeichenfolgenwert: "TextField1".
    
  - NameANSI: Offset 0x26, Packedansistring streamstruktur-Stream.
    
    - Length: Offset 0x26, 1 Byte: 0xA (10).
      
    - Characters: Offset 0x27, Array of 10 CHARs. ANSI-Zeichenfolgenwert: "TextField1".
    
  - FormulaANSI: Offset 0x31, Packedansistring streamstruktur-Stream.
    
    - Length: Offset 0x31, 1 Byte: 0x0 festlegen (0).
      
    - Characters: Offset 0x32, Array of 0 CHARs. Leere ANSI-Zeichenfolge.
    
  - ValidationRuleANSI: Offset 0x32, Packedansistring streamstruktur-Stream.
    
    - Length: Offset 0x32, 1 Byte: 0x0 festlegen (0).
      
    - Characters: Offset 0x33, Array of 0 CHARs. Leere ANSI-Zeichenfolge.
    
  - ValidationTextANSI: Offset 0x33, Packedansistring streamstruktur-Stream.
    
    - Length: Offset 0x33, 1 Byte: 0x0 festlegen (0).
      
    - Characters: Offset 0x34, Array of 0 CHARs. Leere ANSI-Zeichenfolge.
    
  - ErrorANSI: Offset 0x34, Packedansistring streamstruktur-Stream.
    
    - Length: Offset 0x34, 1 Byte: 0x0 festlegen (0).
      
    - Characters: Offset 0x35, Array of 0 CHARs. Leere ANSI-Zeichenfolge.
    
  - Internaltype: Offset 0x35 bytes: 0x0 festlegen (iTypeString).
    
  - SkipBlocks: Offset-0x39, Reihe von SkipBlock streamstruktur-Streams.
    
  - Erster SkipBlock streamstruktur
    
    - Größe: Offset 0x39 bytes: 0x15 (21).
      
    - Inhalt: Offset 0x3D, Array mit 21 bytes. Dies ist der erste SkipBlock streamstruktur-Datenstrom, daher enthält dieses Array einen Firstskipblockcontent streamstruktur-Stream.
      
      - FieldName: Offset 0x3D, Packedunicodestring streamstruktur Stream.
        
        - Length: Offset 0x3D, 1 Byte: 0xA (10).
          
        - Characters: Offset 0x3E, Array of 10 WCHARs. Unicode-Zeichenfolgenwert: "TextField1".
    
  - Zweite SkipBlock streamstruktur
    
    - Größe: Offset 0x52 bytes: 0x0 festlegen (0). Dies ist der abschließende SkipBlock streamstruktur-Stream.
    
## <a name="see-also"></a>Siehe auch

- [Outlook-Elemente und-Felder](outlook-items-and-fields.md)
- [Stream-Strukturen](stream-structures.md)
- [PropertyDefinition-Datenstrom Struktur](propertydefinition-stream-structure.md)
- [FieldDefinition streamstruktur-Datenstrom Struktur](fielddefinition-stream-structure.md)
- [SkipBlock streamstruktur-Datenstrom Struktur](skipblock-stream-structure.md)
- [Firstskipblockcontent streamstruktur-Datenstrom Struktur](firstskipblockcontent-stream-structure.md)
- [Packedansistring streamstruktur-Datenstrom Struktur](packedansistring-stream-structure.md)
- [Packedunicodestring streamstruktur-Datenstrom Struktur](packedunicodestring-stream-structure.md)

