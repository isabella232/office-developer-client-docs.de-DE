---
title: PropertyDefinition-Datenstrombeispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a027967bfe73e04a554733e041c31875e74733c4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550162"
---
# <a name="propertydefinition-stream-sample"></a>PropertyDefinition-Datenstrombeispiel

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird ein Beispiel für einen PropertyDefinition-Datenstrom beschrieben. Der Datenstrom enthält eine Definition eines benutzerdefinierten Felds,  `TextField1` . Der Typ ist **Text,** und die Definition hat das PropDefV2-Format.
  
## <a name="data-dump"></a>Datenabbild

Es folgt ein Datenabbild des Datenstroms, wie es in einem binären Editor angezeigt wird.
  
|Datenstromversatz|Datenbytes|ASCII-Daten|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
Es folgt eine Analyse der Beispieldaten für den PropertyDefinition-Datenstrom:
  
- Version: Offset 0x0, 2 Bytes: 0x0103 (PropDefV2).
    
- FieldDefinitionCount: Offset 0x2, 4 Bytes: 0x1 (1).
    
- FieldDefinitions: Offset 0x6, Array von 1 FieldDefinition-Datenstrom.
    
  - Flags: Offset 0x6, 4 Bytes: 0x45 (PDO_IS_CUSTOM| PDO_PRINT_SAVEAS| PDO_PRINT_SAVEAS_DEF).
    
  - VT: Offset 0xA, 2 Bytes: 0x8 (**VT_BSTR**).
    
  - DispId: Offset 0xC, 4 Bytes: 0x0 (0).
    
  - NmidNameLength: Offset 0x10, 2 Bytes: 0xA (10).
    
  - NmidName: Offset 0x12, Array von 10 WCHARs. Unicode-Zeichenfolgenwert: "TextField1".
    
  - NameANSI: Offset 0x26, PackedAnsiString-Datenstrom.
    
    - Länge: Offset 0x26, 1 Byte: 0xA (10).
      
    - Zeichen: Offset 0x27, Array von 10 CHARs. ANSI-Zeichenfolgenwert: "TextField1".
    
  - FormulaANSI: Offset 0x31, PackedAnsiString-Datenstrom.
    
    - Länge: Offset 0x31, 1 Byte: 0x0 (0).
      
    - Zeichen: Offset 0x32, Array von 0 CHARs. Leere ANSI-Zeichenfolge.
    
  - ValidationRuleANSI: Offset 0x32, PackedAnsiString-Datenstrom.
    
    - Länge: Offset 0x32, 1 Byte: 0x0 (0).
      
    - Zeichen: Offset 0x33, Array von 0 CHARs. Leere ANSI-Zeichenfolge.
    
  - ValidationTextANSI: Offset 0x33, PackedAnsiString-Datenstrom.
    
    - Länge: Offset 0x33, 1 Byte: 0x0 (0).
      
    - Zeichen: Offset 0x34, Array von 0 CHARs. Leere ANSI-Zeichenfolge.
    
  - ErrorANSI: Offset 0x34, PackedAnsiString-Datenstrom.
    
    - Länge: Offset 0x34, 1 Byte: 0x0 (0).
      
    - Zeichen: Offset 0x35, Array von 0 CHARs. Leere ANSI-Zeichenfolge.
    
  - InternalType: Offset 0x35, 4 Bytes: 0x0 (iTypeString).
    
  - SkipBlocks: Offset 0x39, Reihe von SkipBlock-Datenströmen.
    
  - First SkipBlock
    
    - Größe: Offset 0x39, 4 Bytes: 0x15 (21).
      
    - Inhalt: Offset 0x3D, Array von 21 Byte. Dies ist der erste SkipBlock-Stream, daher enthält dieses Array einen FirstSkipBlockContent-Stream.
      
      - FieldName: Offset 0x3D, PackedUnicodeString-Datenstrom.
        
        - Länge: Offset 0x3D, 1 Byte: 0xA (10).
          
        - Zeichen: Offset 0x3E, Array von 10 WCHARs. Unicode-Zeichenfolgenwert: "TextField1".
    
  - Second SkipBlock
    
    - Größe: Offset 0x52, 4 Bytes: 0x0 (0). Dies ist der beendende SkipBlock-Stream.
    
## <a name="see-also"></a>Siehe auch

- [Outlook Elemente und Felder](outlook-items-and-fields.md)
- [Stream-Strukturen](stream-structures.md)
- [PropertyDefinition-Datenstromstruktur](propertydefinition-stream-structure.md)
- [FieldDefinition-Datenstromstruktur](fielddefinition-stream-structure.md)
- [SkipBlock-Streamstruktur](skipblock-stream-structure.md)
- [FirstSkipBlockContent-Streamstruktur](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString-Datenstromstruktur](packedansistring-stream-structure.md)
- [PackedUnicodeString-Datenstromstruktur](packedunicodestring-stream-structure.md)

