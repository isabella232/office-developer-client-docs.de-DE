---
title: FieldDefinition streamstruktur-Datenstrom Struktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 98584e450bb820dbce05b0f8d2c6d15551586130
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334895"
---
# <a name="fielddefinition-stream-structure"></a>FieldDefinition streamstruktur-Datenstrom Struktur

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine FieldDefinition streamstruktur-Datenstrom Struktur enthält entweder die Felddefinition eines benutzerdefinierten Felds oder eine Gruppe von Datenbindungseinstellungen für ein integriertes Feld.
  
Sie können eine FieldDefinition streamstruktur-Datenstrom Strukturprogramm gesteuert bearbeiten, wenn die Struktur die Felddefinition eines benutzerdefinierten Felds enthält. Sie sollten nicht versuchen, eine FieldDefinition streamstruktur-Strukturprogramm gesteuert zu erstellen oder zu ändern, wenn die Struktur Einstellungen für ein integriertes Feld enthält. Sie sollten den Microsoft Outlook-Formular-Designer verwenden, um solche Einstellungen für integrierte Felder zu verwalten.
  
> [!NOTE]
> Outlook unterstützt zwei Formate von Felddefinitionen: PropDefV1 und PropDefV2. Das PropDefV1-Format der Felddefinitionen enthält die folgenden Datenelemente: Flags, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI und ErrorANSI. Das PropDefV2-Format enthält die gleichen Elemente und die internaltype-und SkipBlocks-Elemente. 
>
> In Outlook wird für die FormulaANSI-, ValidationRuleANSI-und ValidationTextANSI-Datenelemente im PropDefV2-Feld Definitionsformat keine Unicode-Version beibehalten. Wenn diese Elemente nicht-ASCII-Zeichen enthalten, können diese Zeichen in Abhängigkeit von der ANSI-codeSeite des Computers, auf dem Outlook läuft, inkonsistent interpretiert werden. Daher sollten Sie nur Zeichenfolgenwerte verwenden, die ausschließlich aus ASCII-Zeichen für diese Datenelemente bestehen. 
  
Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar folgen einander in der angegebenen Reihenfolge.
  
- Flags: DWORD (4 Bytes), eine Kombination aus null oder mehr Flags, deren Werte und Bedeutungen in der folgenden Tabelle aufgeführt sind.
    
    |**FlagName**|**Wert**|**Beschreibung**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |Die FieldDefinition streamstruktur-Struktur enthält eine Definition eines benutzerdefinierten Felds.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Für ein an dieses Feld gebundenes Formularsteuerelement wird auf der Registerkarte **Validierung** des Dialogfelds **Eigenschaften** das Kontrollkästchen für **einen Wert benötigt, um dieses Feld** auszuwählen.  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |Für ein an dieses Feld gebundenes Formularsteuerelement wird auf der Registerkarte **Validierung** des Dialogfelds **Eigenschaften** das Kontrollkästchen **dieses Feld für Drucken und speichern unter Hinzufügen** ausgewählt.  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |Für ein an dieses Feld gebundenes Formularsteuerelement wird auf der Registerkarte **Wert** des Dialogfelds **Eigenschaften** das Kontrollkästchen für **Diese Formel automatisch berechnen** ausgewählt.  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |Hierbei handelt es sich um ein Feld vom Typ **Kombination** , das die **Verbindungsfelder und alle Textfragmente** enthält, die im Dialogfeld **Kombinations Formelfeld** ausgewählt sind.  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |Dieses Feld hat den Typ **Kombination** und **zeigt nur das erste nicht leere Feld an, wobei die nachfolgenden Optionen ignoriert werden,** die im Dialogfeld Kombinations **Formelfeld** ausgewählt wurden.  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Dieses Flag wird von Outlook nicht verwendet, ist jedoch für alle benutzerdefinierten Felddefinitionen enthalten.  <br/> |
   
- VT: WORD (2 Bytes), der Datentyp des Felds, das eine Konstante aus der [VarEnum](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) -Aufzählung ist. 
    
- DispId: DWORD (4 Bytes), der Dispatch-Bezeichner des Felds. Für ein benutzerdefiniertes Feld ist der Wert 0.
    
- NmidNameLength: WORD (2 Bytes), die Anzahl der Elemente im NmidName-Array.
    
- NmidName: ein Array von Typ WCHAR. Bei einer benutzerdefinierten Felddefinition ist dies die Unicode (UTF-16)-Darstellung des Feldnamens. Die Anzahl dieses Arrays ist gleich NmidNameLength.
    
- NameANSI: eine [packedansistring streamstruktur](packedansistring-stream-structure.md) -Datenstrom Struktur. Dies ist die ANSI-Darstellung des Feldnamens. 
    
- FormulaANSI: eine Packedansistring streamstruktur-Datenstrom Struktur. Dies ist eine ANSI-Darstellung der Berechnungsformel für das Feld. Sie wird im Abschnitt **Anfangswert** der Registerkarte **Wert** des Dialogfelds **Eigenschaften** eines Formularsteuerelements angezeigt, das an dieses Feld gebunden ist. 
    
- ValidationRuleANSI: eine Packedansistring streamstruktur-Datenstrom Struktur. Dies ist eine ANSI-Darstellung der Validierungs Formel des Felds. Sie wird im Dialogfeld **Eigenschaften** eines Formularsteuerelements, das an dieses Feld gebunden ist, im Textfeld für **Validierungs Formel** auf der Registerkarte **Validierung** angezeigt. 
    
- ValidationTextANSI: eine Packedansistring streamstruktur-Datenstrom Struktur. Dies ist eine ANSI-Darstellung des Validierungsfehlers des Felds. Sie wird im Textfeld für **Diese Meldung anzeigen angezeigt, wenn die Überprüfung** auf der Registerkarte **Validierung** des Dialogfelds **Eigenschaften** eines Formularsteuerelements, das an dieses Feld gebunden ist, fehlschlägt. 
    
- ErrorANSI: eine Packedansistring streamstruktur-Datenstrom Struktur. Outlook verwendet dieses Element nicht; Sie sollten dieses Element auf eine leere Zeichenfolge festlegen.
    
- Internaltype: DWORD (4 Bytes), der interne Feldtyp. Dieses Data-Element ist nur vorhanden, wenn das Feld Definitionsformat PropDefV2 ist. Der interne Typ ist einer der folgenden Werte, von denen jeder einem Typ im Dialogfeld **Neues Feld** für benutzerdefinierte Felder entspricht. 
    
    |**Interner Typname**|**Wert**|**Entsprechende Art im Dialogfeld " **Neues Feld** "**|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**Number** <br/> |
    |iTypePercent  <br/> |2  <br/> |**Percent** <br/> |
    |Währung  <br/> |3  <br/> |**Currency** <br/> |
    |iTypeBool  <br/> |4  <br/> |**Yes/No** <br/> |
    |iTypeDateTime  <br/> |5  <br/> |**Datum/Uhrzeit** <br/> |
    |iTypeDuration  <br/> |6  <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7  <br/> |**Kombination**, wobei **nur das erste nicht leere Feld angezeigt wird, wobei die nachfolgenden Optionen ignoriert werden,** die im Dialogfeld **Kombinations Formelfeld** ausgewählt wurden.  <br/> |
    |iTypeFormula  <br/> |8  <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |9  <br/> |Dieser Typ wird nicht für benutzerdefinierte Felder verwendet.  <br/> |
    |iTypeVariant  <br/> |10  <br/> |Dieser Typ wird nicht für benutzerdefinierte Felder verwendet.  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |Dieser Typ wird nicht für benutzerdefinierte Felder verwendet.  <br/> |
    |iTypeConcat  <br/> |12  <br/> |**Kombination**, wobei die **Verbindungsfelder und alle Textfragmente mit jeder anderen** Option im Dialogfeld **Kombinations Formelfeld** ausgewählt werden.  <br/> |
    |iTypeKeywords  <br/> |13  <br/> |**Schlüsselwort** <br/> |
    |iTypeInteger  <br/> |14  <br/> |**Integer** <br/> |
   
- SkipBlocks: eine Reihe von einer oder mehreren [SkipBlock streamstruktur](skipblock-stream-structure.md) -Stream-Strukturen. Dieses Data-Element ist nur vorhanden, wenn das Feld Definitionsformat PropDefV2 ist. Wenn das Feld Definitionsformat PropDefV2 ist, sollte die Reihe mindestens eine SkipBlock streamstruktur-Struktur enthalten, die SkipBlock streamstruktur-Struktur, die das size-Datenelement gleich 0 hat, und die Reihe sollte mit dieser SkipBlock streamstruktur-Struktur beginnen und enden. 
    
   Der Zweck einer SkipBlock streamstruktur-Struktur hängt von der relativen Position in der SkipBlocks-Reihe ab. Wenn die Felddefinition im PropDefV2-Format vorliegt und die erste Struktur nicht die abschließende Struktur ist (das size-Datenelement ist größer als 0), geht Outlook davon aus, dass die erste SkipBlock streamstruktur-Struktur den Feldnamen in Unicode (UTF-16) angibt. 
    
   > [!IMPORTANT]
   > Wenn der erste SkipBlock streamstruktur die abschließende Struktur ist, wird das NameANSI-Datenelement verwendet, um den Feldnamen zu bestimmen. Wenn diese Zeichenfolge nicht-ASCII-Zeichen enthält, können diese Zeichen in Abhängigkeit von der ANSI-Codeseite des Computers, auf dem Outlook läuft, inkonsistent interpretiert werden. Um solche Inkonsistenzen zu vermeiden, stellen Sie sicher, dass Sie immer die erste SkipBlock streamstruktur in Felddefinitionen angeben, die Sie erstellen, zumindest wenn der Feldname nicht-ASCII-Zeichen enthält. 
  
   Wenn eine zukünftige Version eines Feld Definitions Formats zusätzliche Daten im FieldDefinition streamstruktur-Stream einführt, können diese Daten als zusätzliche SkipBlock streamstruktur-Stream-Strukturen in der SkipBlocks-Reihe gespeichert werden, bevor die abschließende SkipBlock streamstruktur-Struktur mit der Size-Datenelement gleich 0. Frühere Versionen von Outlook können diese zusätzlichen SkipBlock streamstruktur-Strukturen bis zur abschließenden SkipBlock streamstruktur-Struktur ignorieren und trotzdem alle unterstützten Blöcke ordnungsgemäß verarbeiten.
    
## <a name="see-also"></a>Siehe auch

- [Outlook-Elemente und-Felder](outlook-items-and-fields.md)
- [Stream-Strukturen](stream-structures.md)
- [PropertyDefinition-Datenstrom Struktur](propertydefinition-stream-structure.md)

