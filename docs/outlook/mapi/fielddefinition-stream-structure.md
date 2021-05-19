---
title: FieldDefinition-Streamstruktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 98584e450bb820dbce05b0f8d2c6d15551586130
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334895"
---
# <a name="fielddefinition-stream-structure"></a>FieldDefinition-Streamstruktur

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine FieldDefinition-Datenstromstruktur enthält entweder die Felddefinition eines benutzerdefinierten Felds oder eine Reihe von Datenbindungseinstellungen für ein integriertes Feld.
  
Sie können eine FieldDefinition-Streamstruktur programmgesteuert bearbeiten, wenn die Struktur die Felddefinition eines benutzerdefinierten Felds enthält. Sie sollten nicht versuchen, eine FieldDefinition-Struktur programmgesteuert zu erstellen oder zu ändern, wenn die Struktur Einstellungen für ein integriertes Feld enthält. Verwenden Sie den Microsoft Outlook Forms Designer, um diese Einstellungen für integrierte Felder zu verwalten.
  
> [!NOTE]
> Outlook unterstützt zwei Formate von Felddefinitionen: PropDefV1 und PropDefV2. Das PropDefV1-Format von Felddefinitionen enthält die folgenden Datenelemente: Flags, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI und ErrorANSI. Das PropDefV2-Format enthält dieselben Elemente sowie die Elemente InternalType und SkipBlocks. 
>
> Outlook enthält keine Unicode-Version für die Datenelemente FormulaANSI, ValidationRuleANSI und ValidationTextANSI im PropDefV2-Felddefinitionsformat. Wenn diese Elemente Nicht-ASCII-Zeichen enthalten, können diese Zeichen abhängig von der ANSI-Codeseite des Computers, auf dem Outlook ausgeführt wird, inkonsistent interpretiert werden. Daher sollten Sie nur Zeichenfolgenwerte verwenden, die vollständig aus ASCII-Zeichen für diese Datenelemente bestehen. 
  
Datenelemente in diesem Datenstrom werden in der Bytereihenfolge des Little-Endian-Elements gespeichert und folgen sofort in der unten angegebenen Reihenfolge aufeinander.
  
- Flags: DWORD (4 Byte), eine Kombination aus Null oder mehr Flags, deren Werte und Bedeutungen in der folgenden Tabelle aufgeführt sind.
    
    |**Kennzeichenname**|**Wert**|**Beschreibung**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |Die FieldDefinition-Struktur enthält eine Definition eines benutzerdefinierten Felds.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Für ein an dieses Feld gebundenes Formularsteuerelement ist das Kontrollkästchen **A-Wert** für dieses Feld auf der Registerkarte Überprüfung des Dialogfelds **Eigenschaften** aktiviert.   <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |Für ein an dieses Feld gebundenes  Formularsteuerelement ist das Kontrollkästchen Dieses  Feld zum Drucken hinzufügen und Speichern unter auf der Registerkarte Validierung des Dialogfelds **Eigenschaften** aktiviert.  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |Für ein an dieses Feld gebundenes  Formularsteuerelement wird das Kontrollkästchen Für diese Formel automatisch berechnen auf der Registerkarte **Wert** des Dialogfelds **Eigenschaften** aktiviert.  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |Dies ist ein Feld vom Typ **Combination,** und es sind die **Verknüpfungsfelder** und alle Textfragmente miteinander im Dialogfeld **Kombinationsformelfeld** ausgewählt.  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |Dieses Feld hat den Typ **Kombination** und hat die Option Nur das erste nicht leere Feld **anzeigen,** wobei nachfolgende Optionen im Dialogfeld Kombinationsformelfeld ignoriert werden.   <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Dieses Flag wird nicht von Outlook verwendet, es ist jedoch für alle benutzerdefinierten Felddefinitionen enthalten.  <br/> |
   
- VT: WORD (2 Byte), der Datentyp des Felds, bei dem es sich um eine Konstante aus der [VARENUM-Enumeration](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) handelt. 
    
- DispId: DWORD (4 Byte), der Verteilerbezeichner des Felds. Für ein benutzerdefiniertes Feld ist der Wert 0.
    
- NmidNameLength: WORD (2 Byte), die Anzahl der Elemente im NmidName-Array.
    
- NmidName: Ein Array von WCHAR. Bei einer benutzerdefinierten Felddefinition ist dies die Unicode-Darstellung (UTF-16) des Feldnamens. Die Anzahl dieses Arrays ist gleich NmidNameLength.
    
- NameANSI: Eine [PackedAnsiString-Streamstruktur.](packedansistring-stream-structure.md) Dies ist die ANSI-Darstellung des Feldnamens. 
    
- FormulaANSI: Eine PackedAnsiString-Streamstruktur. Dies ist eine ANSI-Darstellung der Berechnungsformel für das Feld. Sie wird im Abschnitt **Initial Value** der Registerkarte **Wert** des Dialogfelds **Eigenschaften** eines Formularsteuerelements angezeigt, das an dieses Feld gebunden ist. 
    
- ValidationRuleANSI: Eine PackedAnsiString-Streamstruktur. Dies ist eine ANSI-Darstellung der Validierungsformel des Felds. Sie wird im Textfeld  für Validierungsformel auf der Registerkarte Validierung des Dialogfelds **Eigenschaften** eines Formularsteuerelements angezeigt, das an dieses Feld gebunden ist.  
    
- ValidationTextANSI: Eine PackedAnsiString-Streamstruktur. Dies ist eine ANSI-Darstellung des Überprüfungsfehlertexts des Felds. Sie wird im Textfeld  für Diese Meldung anzeigen angezeigt, wenn die Überprüfung auf der Registerkarte Überprüfung des Dialogfelds **Eigenschaften** eines an dieses Feld gebundenen Formularsteuerelements fehlschlägt.  
    
- ErrorANSI: Eine PackedAnsiString-Streamstruktur. Outlook verwendet dieses Element nicht. Sie sollten dieses Element auf eine leere Zeichenfolge festlegen.
    
- InternalType: DWORD (4 Byte), der interne Typ des Felds. Dieses Datenelement ist nur vorhanden, wenn das Felddefinitionsformat PropDefV2 ist. Der interne Typ ist einer der folgenden Werte, von denen jeder einem Typ im Dialogfeld Neues **Feld** für benutzerdefinierte Felder entspricht. 
    
    |**Interner Typname**|**Wert**|**Entsprechender Typ im **Dialogfeld Neues** Feld**|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**Number** <br/> |
    |iTypePercent  <br/> |2  <br/> |**Percent** <br/> |
    |Währung  <br/> |3  <br/> |**Currency** <br/> |
    |iTypeBool  <br/> |4   <br/> |**Yes/No** <br/> |
    |iTypeDateTime  <br/> |5   <br/> |**Datum/Uhrzeit** <br/> |
    |iTypeDuration  <br/> |6   <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7   <br/> |**Kombination** mit der Option Nur das erste nicht leere Feld **anzeigen,** wobei nachfolgende Optionen ignoriert werden, die im Dialogfeld Kombinationsformelfeld ausgewählt sind.   <br/> |
    |iTypeFormula  <br/> |8   <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |9   <br/> |Dieser Typ wird nicht für benutzerdefinierte Felder verwendet.  <br/> |
    |iTypeVariant  <br/> |10  <br/> |Dieser Typ wird nicht für benutzerdefinierte Felder verwendet.  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |Dieser Typ wird nicht für benutzerdefinierte Felder verwendet.  <br/> |
    |iTypeConcat  <br/> |12   <br/> |**Kombination** mit den **Verknüpfungsfeldern und** allen Textfragmenten, die im Dialogfeld **Kombinationsformelfeld** ausgewählt sind.  <br/> |
    |iTypeKeywords  <br/> |13  <br/> |**Schlüsselwort** <br/> |
    |iTypeInteger  <br/> |14   <br/> |**Integer** <br/> |
   
- SkipBlocks: Eine Reihe von einer oder [mehreren SkipBlock-Streamstrukturen.](skipblock-stream-structure.md) Dieses Datenelement ist nur vorhanden, wenn das Felddefinitionsformat PropDefV2 ist. Wenn das Felddefinitionsformat PropDefV2 ist, sollte die Datenreihe mindestens eine SkipBlock-Struktur enthalten, die SkipBlock-Struktur mit dem Size-Datenelement gleich 0, und die Datenreihe sollte mit dieser SkipBlock-Struktur beginnen und beenden. 
    
   Der Zweck einer SkipBlock-Struktur hängt von der relativen Position in der SkipBlocks-Reihe ab. Wenn die Felddefinition im PropDefV2-Format ist und die erste Struktur nicht die Abschlussstruktur ist (das Size-Datenelement ist größer als 0), geht Outlook davon aus, dass die erste SkipBlock-Struktur den Feldnamen in Unicode (UTF-16) angibt. 
    
   > [!IMPORTANT]
   > Wenn der erste SkipBlock die Abschlussstruktur ist, wird das NameANSI-Datenelement verwendet, um den Feldnamen zu bestimmen. Wenn diese Zeichenfolge Keine-ASCII-Zeichen enthält, können diese Zeichen abhängig von der ANSI-Codeseite des Computers, auf dem Outlook ausgeführt wird, inkonsistent interpretiert werden. Um solche Inkonsistenzen zu verhindern, müssen Sie immer den ersten SkipBlock in von Ihnen erstellten Felddefinitionen angeben, zumindest wenn der Feldname Nicht-ASCII-Zeichen enthält. 
  
   Wenn in einer zukünftigen Version eines Felddefinitionsformats zusätzliche Datenteile im FieldDefinition-Stream enthalten sind, können diese Daten als zusätzliche SkipBlock-Streamstrukturen in der SkipBlocks-Reihe gespeichert werden, bevor die SkipBlock-Struktur beendet wird, die das Size-Datenelement gleich 0 hat. Frühere Versionen von Outlook können diese zusätzlichen SkipBlock-Strukturen bis zur abschließenden SkipBlock-Struktur ignorieren und dennoch alle unterstützten Blöcke ordnungsgemäß verarbeiten.
    
## <a name="see-also"></a>Siehe auch

- [Outlook Elemente und Felder](outlook-items-and-fields.md)
- [Streamstrukturen](stream-structures.md)
- [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md)

