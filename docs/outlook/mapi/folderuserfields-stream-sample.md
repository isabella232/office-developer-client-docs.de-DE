---
title: FolderUserFields-Streambeispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eed1ad0e1f64af5bf07cc0ca3c842eed10c43c47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561789"
---
# <a name="folderuserfields-stream-sample"></a>FolderUserFields-Streambeispiel

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird ein Beispiel für einen FolderUserFields-Datenstrom beschrieben. Der Datenstrom enthält eine Definition eines benutzerdefinierten Felds,  `TextField1` . Der Typ ist **Text,** und der FolderUserFields-Stream enthält sowohl FolderUserFieldsAnsi- als auch FolderUserFieldsUnicode-Teile. Weitere Informationen finden Sie unter [Folder Fields Stream Structures](folder-fields-stream-structures.md).
  
## <a name="data-dump"></a>Datenabbild

Es folgt ein Datenabbild des Datenstroms, wie es in einem binären Editor angezeigt wird.
  
|Datenstromversatz|Datenbytes|ASCII-Daten|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

Es folgt eine Analyse der Beispieldaten für den **FolderUserFields-Stream:**
  
- FolderUserFieldsAnsi: Offset 0x0.
    
  - FieldDefinitionCount: Offset 0x0, 4 Bytes: 0x00000002 (2).
    
  - FieldDefinitions: Offset 0x4, Array von 2 FolderFieldDefinitionA-Datenströmen.
    
    **Erstes Arrayelement:**
    
    - FieldType: Offset 0x4, 4 Bytes: 0x00000001 (ftString).
      
    - FieldNameLength: Offset 0x8, 2 Bytes: 0x000A (10)
      
    - FieldName: Offset 0xA, Array von 10 CHARs. ANSI-Zeichenfolgenwert: "TextField1".
      
    - Häufig: Offset-0x14.
    
      - PropSetGuid: Offset 0x14, 16 Bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: Offset 0x24, 4 Bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).
        
      - zeichenfolge: Offset 0x28, 4 Bytes: 0x00000000.
        
      - orbitBitmap: Offset 0x2C, 4 Bytes: 0x00000000.
        
      - wetterDisplay: Offset 0x30, 4 Bytes: 0x00000000.
        
      - iFmt: Offset 0x34, 4 Bytes: 0x00000000.
        
      - wszFormulaLength: Offset 0x38, 2 Bytes: 0x0000 (0).
        
      - wszFormula: Offset 0x3A, Array von 0 WCHARs. Leerer Zeichenfolgenwert.
    
    **Zweites Arrayelement:**
    
    - FieldType: Offset 0x3A, 4 Bytes: 0x00000000 (ftNone).
      
    - FieldNameLength: Offset 0x3E, 2 Bytes: 0x0000 (0).
      
    - FieldName: Offset 0x40, Array von 0 CHARs. Leerer Zeichenfolgenwert.
      
    - Häufig: Offset 0x40.
    
      - PropSetGuid: Offset 0x40, 16 Bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: Offset 0x50, 4 Bytes: 0x00000000 (0).
        
      - zeichenfolge: Offset 0x54, 4 Bytes: 0x00000000.
        
      - orbitBitmap: Offset 0x58, 4 Bytes: 0x00000000.
        
      - wetterDisplay: Offset 0x5C, 4 Bytes: 0x00000000.
        
      - iFmt: Offset 0x60, 4 Bytes: 0x00000000.
        
      - wszFormulaLength: Offset 0x64, 2 Bytes: 0x0000 (0).
        
      - wszFormula: Offset 0x66, Array von 0 WCHARs. Leerer Zeichenfolgenwert.
    
- FolderUserFieldsUnicode: Offset 0x66.
    
  - FieldDefinitionCount: Offset 0x66, 4 Bytes: 0x00000002 (2).
    
  - FieldDefinitions: Offset 0x6A, Array von 2 FolderFieldDefinitionW-Datenströmen.
    
    **Erstes Arrayelement:**
    
    - FieldType: Offset 0x6A, 4 Bytes: 0x00000001 (ftString).
      
    - FieldNameLength: Offset 0x6E, 2 Bytes: 0x000A (10).
      
    - FieldName: Offset 0x70, Array von 10 WCHARs. Unicode-Zeichenfolgenwert: "TextField1".
      
    - Häufig: Offset 0x84.
    
      - PropSetGuid: Offset 0x84, 16 Bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: Offset 0x94, 4 Bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).
        
      - zeichenfolge: Offset 0x98, 4 Bytes: 0x00000000.
        
      - orbitBitmap: Offset 0x9C, 4 Bytes: 0x00000000.
        
      - wetterDisplay: Offset 0xA0, 4 Bytes: 0x00000000.
        
      - iFmt: Offset 0xA4, 4 Bytes: 0x00000000.
        
      - wszFormulaLength: Offset 0xA8, 2 Bytes: 0x0000 (0).
        
      - wszFormula: Offset 0xAA, Array von 0 WCHARs. Leerer Zeichenfolgenwert.
    
    **Zweites Arrayelement:**
    
    - FieldType: Offset 0xAA, 4 Bytes: 0x00000000 (ftNone).
      
    - FieldNameLength: Offset 0xAE, 2 Bytes: 0x0000 (0).
      
    - FieldName: Offset 0xB0, Array von 0 WCHARs. Leerer Zeichenfolgenwert.
      
    - Häufig: Offset 0xB0.
    
      - PropSetGuid: Offset 0xB0, 16 Bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: Offset 0xC0, 4 Bytes: 0x00000000 (0).
        
      - zeichenfolge: Offset 0xC4, 4 Bytes: 0x00000000.
        
      - orbitBitmap: Offset 0xC8, 4 Bytes: 0x00000000.
        
      - wetterDisplay: Offset 0xCC, 4 Bytes: 0x00000000.
        
      - iFmt: Offset 0xD0, 4 Bytes: 0x00000000.
        
      - wszFormulaLength: Offset 0xD4, 2 Bytes: 0x0000 (0).
        
      - wszFormula: Offset 0xD6, Array von 0 WCHARs. Leerer Zeichenfolgenwert.
    
## <a name="see-also"></a>Siehe auch

- [Outlook Elemente und Felder](outlook-items-and-fields.md)
- [PropertyDefinition-Datenstromstruktur](propertydefinition-stream-structure.md)
- [FieldDefinition-Datenstromstruktur](fielddefinition-stream-structure.md)
- [SkipBlock-Streamstruktur](skipblock-stream-structure.md)
- [FirstSkipBlockContent-Streamstruktur](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString-Datenstromstruktur](packedansistring-stream-structure.md)
- [PackedUnicodeString-Datenstromstruktur](packedunicodestring-stream-structure.md)

