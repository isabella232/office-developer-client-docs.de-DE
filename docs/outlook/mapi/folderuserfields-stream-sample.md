---
title: FolderUserFields Stream-Beispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 72c71a6109f55f7ec06499e214a1aa11292a9e52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791702"
---
# <a name="folderuserfields-stream-sample"></a>FolderUserFields Stream-Beispiel

**Betrifft**: Outlook 
  
In diesem Thema wird ein Beispiel eines FolderUserFields Stream-Objekts. Das Stream-Objekt enthält eine Definition eines benutzerdefinierten Felds `TextField1`. Der **Text**ist, und der Stream FolderUserFields FolderUserFieldsAnsi und FolderUserFieldsUnicode Teile enthält. Weitere Informationen finden Sie unter [Ordner Felder Stream Strukturen](folder-fields-stream-structures.md).
  
## <a name="data-dump"></a>Daten dump

Im folgenden finden ein Abbild der Daten des Stream-Objekts, wie er in einem binären-Editor angezeigt.
  
|Stream-offset|Datenbytes|ASCII-Daten|
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
   

Es folgt eine Analyse der Beispieldaten für den Datenstrom **FolderUserFields** :
  
- FolderUserFieldsAnsi: Offset 0 x 0.
    
  - FieldDefinitionCount: Offset 0 x 0, 4 Bytes: 0 x 00000002 (2).
    
  - FieldDefinitions: Offset 0 x 4, Array 2 FolderFieldDefinitionA Datenströme.
    
    **Erste Arrayelement**:
    
    - FieldType: Offset 0, 4 Bytes x 4: 0 x 00000001 (FtString).
      
    - FieldNameLength: Offset 0 x 8, 2 Bytes: 0x000A (10)
      
    - FieldName: Offset 0xA Array von 10 Zeichen. ANSI-String-Wert: "TextField1".
      
    - Allgemeine: Offset 0 x 14.
    
      - PropSetGuid: Offset 0 x 14, 16 Byte: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - Fcapm: Offset 0 x 24, 4 Bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - DwString: Offset 0, 4 Bytes x 28: 0 x 00000000.
        
      - DwBitmap: Offset 0x2C 4 Bytes: 0 x 00000000.
        
      - DwDisplay: Offset 0, 4 Bytes x 30: 0 x 00000000.
        
      - iFmt: Offset 0 x 34, 4 Bytes: 0 x 00000000.
        
      - WszFormulaLength: Offset 0x38 2 Bytes: 0 x 0000 (0).
        
      - WszFormula: Offset 0x3A, Array von 0 WCHARs so lang wie. Leerer String-Wert.
    
    **Zweite Arrayelement**:
    
    - FieldType: Offset 0x3A 4 Bytes: 0 x 00000000 (FtNone).
      
    - FieldNameLength: Offset 0x3E 2 Bytes: 0 x 0000 (0).
      
    - FieldName: Offset 0 x 40, 0 char-Array. Leerer String-Wert.
      
    - Allgemeine: Offset 0 x 40.
    
      - PropSetGuid: Offset 0 x 40, 16 Byte: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - Fcapm: Offset 0 x 50, 4 Bytes: 0 x 00000000 (0).
        
      - DwString: Offset 0, 4 Bytes x 54: 0 x 00000000.
        
      - DwBitmap: Offset 0x58 4 Bytes: 0 x 00000000.
        
      - DwDisplay: Offset 0x5C 4 Bytes: 0 x 00000000.
        
      - iFmt: Offset 0 x 60, 4 Bytes: 0 x 00000000.
        
      - WszFormulaLength: Offset 0x64 2 Bytes: 0 x 0000 (0).
        
      - WszFormula: Offset 0x66, Array von 0 WCHARs so lang wie. Leerer String-Wert.
    
- FolderUserFieldsUnicode: Offset 0x66.
    
  - FieldDefinitionCount: Offset 0x66 4 Bytes: 0 x 00000002 (2).
    
  - FieldDefinitions: Offset 0x6A Array 2 FolderFieldDefinitionW Datenströme.
    
    **Erste Arrayelement**:
    
    - FieldType: Offset 0x6A 4 Bytes: 0 x 00000001 (FtString).
      
    - FieldNameLength: Offset 0x6E 2 Bytes: 0x000A (10).
      
    - FieldName: Offset 0x70 Array von 10 WCHARs so lang wie. Unicode-Zeichenfolgenwert: "TextField1".
      
    - Allgemeine: Offset 0 x 84.
    
      - PropSetGuid: Offset 0 x 84, 16 Byte: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - Fcapm: Offset 0x94 4 Bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - DwString: Offset 0x98 4 Bytes: 0 x 00000000.
        
      - DwBitmap: Offset 0x9C MACHINE_CHECK_EXCEPTION, 4 Bytes: 0 x 00000000.
        
      - DwDisplay: Offset 0xA0 4 Bytes: 0 x 00000000.
        
      - iFmt: Offset 0xA4 4 Bytes: 0 x 00000000.
        
      - WszFormulaLength: Offset 0xA8 2 Bytes: 0 x 0000 (0).
        
      - WszFormula: Offset 0xAA, Array von 0 WCHARs so lang wie. Leerer String-Wert.
    
    **Zweite Arrayelement**:
    
    - FieldType: Offset 0xAA 4 Bytes: 0 x 00000000 (FtNone).
      
    - FieldNameLength: Offset 0xAE 2 Bytes: 0 x 0000 (0).
      
    - FieldName: Offset 0xB0 Array von 0 WCHARs so lang wie. Leerer String-Wert.
      
    - Allgemeine: Offset 0xB0.
    
      - PropSetGuid: Offset 0xB0 16 Byte: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - Fcapm: Offset "0xC0", 4 Bytes: 0 x 00000000 (0).
        
      - DwString: Offset 0xC4 4 Bytes: 0 x 00000000.
        
      - DwBitmap: Offset 0xC8 4 Bytes: 0 x 00000000.
        
      - DwDisplay: Offset 0xCC 4 Bytes: 0 x 00000000.
        
      - iFmt: Offset 0xD0 4 Bytes: 0 x 00000000.
        
      - WszFormulaLength: Offset 0xD4 2 Bytes: 0 x 0000 (0).
        
      - WszFormula: Offset 0xD6, Array von 0 WCHARs so lang wie. Leerer String-Wert.
    
## <a name="see-also"></a>Siehe auch

- [Elemente und Felder in Outlook](outlook-items-and-fields.md)
- [PropertyDefinition-Streamstruktur](propertydefinition-stream-structure.md)
- [FieldDefinition-Streamstruktur](fielddefinition-stream-structure.md)
- [SkipBlock-Streamstruktur](skipblock-stream-structure.md)
- [FirstSkipBlockContent-Streamstruktur](firstskipblockcontent-stream-structure.md)
- [PackedAnsiString-Streamstruktur](packedansistring-stream-structure.md)
- [PackedUnicodeString-Streamstruktur](packedunicodestring-stream-structure.md)

