---
title: PropertyDefinition Stream-Beispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fc216302cb68be4b0e9d57f60f491adebcba1975
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573929"
---
# <a name="propertydefinition-stream-sample"></a>PropertyDefinition Stream-Beispiel

**Betrifft**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird ein Beispiel eines PropertyDefinition Stream-Objekts. Das Stream-Objekt enthält eine Definition eines benutzerdefinierten Felds `TextField1`. Der **Text**ist, und die Definition im Format PropDefV2 ist.
  
## <a name="data-dump"></a>Daten dump

Im folgenden finden ein Abbild der Daten des Stream-Objekts, wie er in einem binären-Editor angezeigt.
  
|Stream-offset|Datenbytes|ASCII-Daten|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
Es folgt eine Analyse der Beispieldaten für den Datenstrom PropertyDefinition:
  
- Version: Offset 0 x 0, 2 Bytes: 0x0103 (PropDefV2).
    
- FieldDefinitionCount: Offset 0 x 2, 4 Bytes: 0 x 1 (1).
    
- FieldDefinitions: Offset 0 x 6, Array 1 FieldDefinition Stream-Objekts.
    
  - Flags: Offset 0, 4 Bytes x 6: 0 x 45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).
    
  - VT: Offset 0xA 2 Bytes: 0 x 8 (**VT_BSTR**).
    
  - DispId: Offset 0xC 4 Bytes: 0 x 0 (0).
    
  - NmidNameLength: Offset 0 x 10, 2 Bytes: 0xA (10).
    
  - NmidName: Offset 0 x 12, Array von 10 WCHARs so lang wie. Unicode-Zeichenfolgenwert: "TextField1".
    
  - NameANSI: Offset 0 x 26, PackedAnsiString-Stream.
    
    - Länge: Offset 0 x 26, 1 Byte: 0xA (10).
      
    - Zeichen: Offset 0 x 27, Array von 10 Zeichen. ANSI-String-Wert: "TextField1".
    
  - FormulaANSI: Offset 0x31, PackedAnsiString-Stream.
    
    - Länge: Offset 0x31, 1 Byte: 0 x 0 (0).
      
    - Zeichen: Offset 0 x 32, Array von 0 Zeichen. Leere ANSI-Zeichenfolge.
    
  - ValidationRuleANSI: Offset 0 x 32, PackedAnsiString-Stream.
    
    - Länge: Offset 0 x 32, 1 Byte: 0 x 0 (0).
      
    - Zeichen: Offset 0 x 33, Array von 0 Zeichen. Leere ANSI-Zeichenfolge.
    
  - ValidationTextANSI: Offset 0 x 33, PackedAnsiString-Stream.
    
    - Länge: Offset 0 x 33, 1 Byte: 0 x 0 (0).
      
    - Zeichen: Offset 0 x 34, 0 char-Array. Leere ANSI-Zeichenfolge.
    
  - ErrorANSI: Offset 0 x 34, PackedAnsiString-Stream.
    
    - Länge: Offset 0 x 34, 1 Byte: 0 x 0 (0).
      
    - Zeichen: Offset 0x35 Array von 0 Zeichen. Leere ANSI-Zeichenfolge.
    
  - InternalType: Offset 0x35 4 Bytes: 0 x 0 (iTypeString).
    
  - SkipBlocks: Offset 0 x 39, Serie SkipBlock Datenströme.
    
  - Erste SkipBlock
    
    - Größe: Offset 0, 4 Bytes x 39: 0x15 (21).
      
    - Inhalt: Offset 0x3D 21 Bytearray. Dies ist der erste SkipBlock Datenstrom dieses Array einen FirstSkipBlockContent Stream enthält.
      
      - FieldName: Offset 0x3D, PackedUnicodeString-Stream.
        
        - Länge: Offset 0x3D, 1 Byte: 0xA (10).
          
        - Zeichen: Offset 0x3E Array von 10 WCHARs so lang wie. Unicode-Zeichenfolgenwert: "TextField1".
    
  - Zweite SkipBlock
    
    - Größe: Offset 0, 4 Bytes x 52: 0 x 0 (0). Dies ist der abschließende SkipBlock-Stream.
    
## <a name="see-also"></a>Siehe auch

- [Elemente und Felder in Outlook](outlook-items-and-fields.md)
- [Streamstrukturen](stream-structures.md)
- [PropertyDefinition-Streamstruktur](propertydefinition-stream-structure.md)
- [FieldDefinition-Streamstruktur](fielddefinition-stream-structure.md)
- [SkipBlock-Streamstruktur](skipblock-stream-structure.md)
- [FirstSkipBlockContent-Streamstruktur](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString-Streamstruktur](packedansistring-stream-structure.md)
- [PackedUnicodeString-Streamstruktur](packedunicodestring-stream-structure.md)

