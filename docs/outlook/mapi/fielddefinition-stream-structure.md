---
title: FieldDefinition Stream-Struktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 775dc1b5fdcf40867f67fbab25879bd97de24f4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791669"
---
# <a name="fielddefinition-stream-structure"></a>FieldDefinition Stream-Struktur

**Betrifft**: Outlook 
  
Eine FieldDefinition Stream-Datenstruktur enthält entweder die Felddefinition eines benutzerdefinierten Felds oder einer Gruppe von Einstellungen für ein Feld integrierten Datenbindung.
  
Sie können eine FieldDefinition Stream Struktur programmgesteuert ändern, wenn die Struktur die Felddefinition eines benutzerdefinierten Felds enthält. Sie sollten nicht versuchen, programmgesteuert erstellen oder ändern eine FieldDefinition-Struktur aus, wenn die Datenstruktur Einstellungen für ein integrierter Feld enthält. Sie sollten im Microsoft Outlook-Formular-Designer verwenden, um diese Einstellungen für integrierte Felder verwalten.
  
> [!NOTE]
> Outlook unterstützt die folgenden beiden Formate der Felddefinitionen: PropDefV1 und PropDefV2. Das Format PropDefV1 Felddefinitionen enthält die folgenden Elemente: Flags, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI und ErrorANSI. Das Format PropDefV2 enthält die gleichen Elemente und Elemente InternalType und SkipBlocks. 
>
> Outlook verwaltet keine Unicode-Version für die Datenelemente FormulaANSI, ValidationRuleANSI und ValidationTextANSI im Format Definition PropDefV2 dar. Wenn diese Elemente nicht-ASCII-Zeichen enthalten, können diese Zeichen inkonsistent je nach der ANSI-Codeseite des Computers interpretiert werden auf denen Outlook ausgeführt wird. Aus diesem Grund sollten Sie nur Zeichenfolgenwerte verwenden, die ausschließlich ASCII-Zeichen für diese Datenelemente bestehen. 
  
Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der angegebenen Reihenfolge gespeichert.
  
- Flags: DWORD-Wert (4 Bytes), eine Kombination aus null oder mehr Flags, deren Werte und Bedeutung in der folgenden Tabelle aufgeführt sind.
    
    |**Namen des Kennzeichens**|**Wert**|**Beschreibung**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |Die FieldDefinition-Datenstruktur enthält eine Definition eines benutzerdefinierten Felds.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Für ein Formularsteuerelement an dieses Feld gebunden ist wird in die Registerkarte **Gültigkeit** im Dialogfeld **Eigenschaften** das Kontrollkästchen für **ein Wert für dieses Feld erforderlich ist** ausgewählt.  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0 x 00000004  <br/> |Für ein Webformular-Steuerelement gebunden, in dieses Feld, das Kontrollkästchen für **Feld für das Drucken und speichern unter** in die Registerkarte **Gültigkeit** im Dialogfeld **Eigenschaften** aktiviert ist.  <br/> |
    |PDO_CALC_AUTO  <br/> |0 x 00000008  <br/> |Für ein Formularsteuerelement an dieses Feld gebunden ist ist in der Registerkarte **Wert** im Dialogfeld **Eigenschaften** das Kontrollkästchen für die **Formel automatisch berechnen** ausgewählt.  <br/> |
    |PDO_FT_CONCAT  <br/> |0 x 00000010  <br/> |Hierbei handelt es sich um ein Feld vom Typ **Kombination aus** , und die Option **Aneinanderfügen von Feldern und Textabschnitte miteinander** in das Dialogfeld **Formel Kombinationsfeld** ausgewählt hat.  <br/> |
    |PDO_FT_SWITCH  <br/> |0 x 00000020  <br/> |Dieses Feld ist vom Typ **Kombination aus** , und die Option zum **Anzeigen der ersten nicht leeren Feldes und Ignorieren nachfolgender Felder** im Dialogfeld **Formel Kombinationsfeld** ausgewählt.  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0 x 00000040  <br/> |Dieses Kennzeichen werden von Outlook nicht verwendet, aber es ist für alle benutzerdefinierten Felddefinitionen enthalten.  <br/> |
   
- VT: Wort (2 Bytes) der Datentyp des Felds, eine Konstante aus der [VARENUM](http://msdn.microsoft.com/en-us/library/system.runtime.interopservices.varenum.aspx) -Aufzählung. 
    
- DispId: DWORD-Wert (4 Bytes) der Versendung Bezeichner des Felds. Für ein benutzerdefiniertes Feld ist der Wert 0.
    
- NmidNameLength: Wort (2 Bytes), die Anzahl der Elemente im Array NmidName.
    
- NmidName: Ein Array von WCHAR. Bei der Definition eines benutzerdefinierten Felds ist dies die Unicode (UTF-16)-Darstellung der Name des Felds. Die Anzahl der dieses Array ist gleich NmidNameLength.
    
- NameANSI: Eine [PackedAnsiString](packedansistring-stream-structure.md) Stream-Struktur. Dies ist die ANSI-Darstellung der Name des Felds. 
    
- FormulaANSI: Eine PackedAnsiString Stream-Struktur. Dies ist eine ANSI-Darstellung der die Formel für das Feld. Es wird im Abschnitt **Anfangswert** der Registerkarte **Wert** im Dialogfeld **Eigenschaften** des Formularsteuerelements an dieses Feld gebunden angezeigt. 
    
- ValidationRuleANSI: Eine PackedAnsiString Stream-Struktur. Dies ist eine ANSI-Darstellung der gültigkeitsprüfung das dar. Es wird in das Textfeld für die **Gültigkeitsprüfung** auf die Registerkarte **Gültigkeit** im Dialogfeld **Eigenschaften** des Formularsteuerelements an dieses Feld gebunden angezeigt. 
    
- ValidationTextANSI: Eine PackedAnsiString Stream-Struktur. Dies ist eine ANSI-Darstellung des Felds Gültigkeitsprüfungstext Fehler. Es wird in das Textfeld für die **Anzeige dieser Nachricht, wenn die Überprüfung fehlschlägt** auf die Registerkarte **Gültigkeit** im Dialogfeld **Eigenschaften** des Formularsteuerelements an dieses Feld gebunden angezeigt. 
    
- ErrorANSI: Eine PackedAnsiString Stream-Struktur. Dieses Element wird von Outlook nicht verwendet. Sie sollten dieses Element auf eine leere Zeichenfolge festgelegt.
    
- InternalType: DWORD-Wert (4 Bytes) der internen Art des Felds. Dieses Datenelement ist nur vorhanden, wenn das Feld Definition Format PropDefV2 ist. Der interne Typ ist eine der folgenden Werte an, von die jedes auf einen Typ für benutzerdefinierte Felder im Dialogfeld **Neues Feld** entspricht. 
    
    |**Interne Typnamen**|**Wert**|**Entsprechende Typ im Dialogfeld **Neues Feld****|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**Nummer** <br/> |
    |iTypePercent  <br/> |2  <br/> |**Percent** <br/> |
    |Währung  <br/> |3  <br/> |**Currency** <br/> |
    |iTypeBool  <br/> |4  <br/> |**Ja/Nein** <br/> |
    |iTypeDateTime  <br/> |5  <br/> |**Datum/Uhrzeit** <br/> |
    |iTypeDuration  <br/> |6  <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7  <br/> |**Kombination**mit der Option **Anzeigen der ersten nicht leeren Feldes und Ignorieren nachfolgender Felder** im Dialogfeld **Formel Kombinationsfeld** ausgewählt.  <br/> |
    |iTypeFormula  <br/> |8  <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |9  <br/> |Dieser Typ ist nicht für benutzerdefinierte Felder verwendet werden.  <br/> |
    |iTypeVariant  <br/> |10  <br/> |Dieser Typ ist nicht für benutzerdefinierte Felder verwendet werden.  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |Dieser Typ ist nicht für benutzerdefinierte Felder verwendet werden.  <br/> |
    |iTypeConcat  <br/> |12  <br/> |**Kombination**mit der **Aneinanderfügen von Feldern und Textabschnitte miteinander** Option im Dialogfeld **Kombination Formel dar** .  <br/> |
    |iTypeKeywords  <br/> |13  <br/> |**Schlüsselwort** <br/> |
    |iTypeInteger  <br/> |14  <br/> |**Integer** <br/> |
   
- SkipBlocks: Eine Reihe von mindestens [SkipBlock](skipblock-stream-structure.md) Stream Strukturen. Dieses Datenelement ist nur vorhanden, wenn das Feld Definition Format PropDefV2 ist. Wenn das Feld Definition Format PropDefV2 ist, der Datenreihe sollte mindestens eine SkipBlock-Struktur, die SkipBlock-Struktur, die das Größe der Data-Element gleich 0 ist, hat enthalten, und die Datenreihe beginnen und beenden mit diese Struktur SkipBlock sollten. 
    
   Der Zweck der eine SkipBlock Struktur hängt die relative Position in der Datenreihe SkipBlocks. Wenn die Felddefinition in PropDefV2 Format ist und die erste Struktur nicht der Abbruch Struktur ist (das Element für die Größe ist größer als 0), wird Outlook davon ausgegangen, dass die erste SkipBlock-Struktur in Unicode (UTF-16) der Name des Felds angibt. 
    
   > [!IMPORTANT]
   > Ist der erste SkipBlock Abbruch Struktur, wird das Element für die NameANSI der Name des Felds bestimmt. Wenn diese Zeichenfolge alle nicht-ASCII-Zeichen enthält, können diese Zeichen inkonsistent je nach der ANSI-Codeseite des Computers interpretiert werden auf denen Outlook ausgeführt wird. Um zu verhindern, dass derartige Inkonsistenzen, achten Sie darauf, dass Sie immer die erste SkipBlock in Felddefinitionen angeben, die Sie erstellen, enthält mindestens Wenn der Name des Felds nicht-ASCII-Zeichen. 
  
   Wenn eine zukünftige Version von einem Feld Definition Format zusätzlichen Datenelemente im Datenstrom FieldDefinition eingeführt wird, können diese Daten gespeichert werden, als zusätzliche SkipBlock Stream Strukturen in der Datenreihe SkipBlocks vor den Abbruch SkipBlock-Struktur, die Größe der Data-Element gleich 0. Frühere Versionen von Outlook können ignorieren diese zusätzlichen SkipBlock Strukturen bis zu den Abbruch SkipBlock Struktur und die Blöcke, die sie unterstützen weiterhin ordnungsgemäß verarbeiten können.
    
## <a name="see-also"></a>Siehe auch

- [Elemente und Felder in Outlook](outlook-items-and-fields.md)
- [Streamstrukturen](stream-structures.md)
- [PropertyDefinition-Streamstruktur](propertydefinition-stream-structure.md)

