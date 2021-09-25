---
title: FieldDefinition-Datenstromstruktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2277d66a4f46a64f6e5fce9cad747fb98e767701
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588035"
---
# <a name="fielddefinition-stream-structure"></a>FieldDefinition-Datenstromstruktur

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine FieldDefinition-Datenstromstruktur enthält entweder die Felddefinition eines benutzerdefinierten Felds oder eine Reihe von Datenbindungseinstellungen für ein integriertes Feld.
  
Sie können eine FieldDefinition-Datenstromstruktur programmgesteuert bearbeiten, wenn die Struktur die Felddefinition eines benutzerdefinierten Felds enthält. Sie sollten nicht versuchen, eine FieldDefinition-Struktur programmgesteuert zu erstellen oder zu ändern, wenn die Struktur Einstellungen für ein integriertes Feld enthält. Verwenden Sie den Microsoft Outlook Forms Designer, um solche Einstellungen für integrierte Felder beizubehalten.
  
> [!NOTE]
> Outlook unterstützt zwei Formate von Felddefinitionen: PropDefV1 und PropDefV2. Das PropDefV1-Format von Felddefinitionen enthält die folgenden Datenelemente: Flags, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI und ErrorANSI. Das PropDefV2-Format enthält dieselben Elemente sowie die Elemente InternalType und SkipBlocks. 
>
> Outlook verwaltet keine Unicode-Version für die FormulaANSI-, ValidationRuleANSI- und ValidationTextANSI-Datenelemente im PropDefV2-Felddefinitionsformat. Wenn diese Elemente Nicht-ASCII-Zeichen enthalten, können diese Zeichen abhängig von der ANSI-Codepage des Computers, auf dem Outlook ausgeführt wird, inkonsistent interpretiert werden. Daher sollten Sie für diese Datenelemente nur Zeichenfolgenwerte verwenden, die vollständig aus ASCII-Zeichen bestehen. 
  
Datenelemente in diesem Datenstrom werden in kleiner endischer Bytereihenfolge gespeichert und folgen sich direkt in der unten angegebenen Reihenfolge.
  
- Flags: DWORD (4 Bytes), eine Kombination aus null oder mehr Flags, deren Werte und Bedeutungen in der folgenden Tabelle aufgeführt sind.
    
    |**Kennzeichenname**|**Wert**|**Beschreibung**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |Die FieldDefinition-Struktur enthält eine Definition eines benutzerdefinierten Felds.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Für ein Formularsteuerelement, das an dieses Feld gebunden ist, ist das Kontrollkästchen für **A-Wert erforderlich, damit dieses Feld** auf der Registerkarte **Gültigkeit** des Dialogfelds **Eigenschaften** aktiviert ist.  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |Für ein Formularsteuerelement, das an dieses Feld gebunden ist, ist das Kontrollkästchen für **"Dieses Feld zum Drucken einschließen" und "Speichern unter"** auf der Registerkarte **"Überprüfung"** des Dialogfelds **"Eigenschaften"** aktiviert.  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |Bei einem Formularsteuerelement, das an dieses Feld gebunden ist, wird das Kontrollkästchen für **die automatische Berechnung dieser Formel** auf der Registerkarte **Wert** des Dialogfelds **Eigenschaften** aktiviert.  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |Hierbei handelt es sich um ein Feld vom Typ Kombination, bei dem die  **Verknüpfungsfelder und alle Textfragmente beieinander** im Dialogfeld Kombinationsformelfeld ausgewählt sind.   <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |Dieses Feld ist vom Typ Kombination und zeigt **nur das erste nicht leere Feld an, wobei nachfolgende** Optionen ignoriert werden, die im Dialogfeld **Kombinationsformelfeld** ausgewählt sind.   <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Dieses Flag wird nicht von Outlook verwendet, ist jedoch für alle benutzerdefinierten Felddefinitionen enthalten.  <br/> |
   
- VT: WORD (2 Bytes), der Datentyp des Felds, bei dem es sich um eine Konstante aus der [VARENUM-Enumeration](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) handelt. 
    
- DispId: DWORD (4 Bytes), der Verteilerbezeichner des Felds. Für ein benutzerdefiniertes Feld ist der Wert 0.
    
- NmidNameLength: WORD (2 Bytes), die Anzahl der Elemente im NmidName-Array.
    
- NmidName: Ein Array von WCHAR. Bei einer benutzerdefinierten Felddefinition ist dies die Unicode-Darstellung (UTF-16) des Feldnamens. Die Anzahl dieses Arrays ist gleich NmidNameLength.
    
- NameANSI: Eine [PackedAnsiString-Datenstromstruktur.](packedansistring-stream-structure.md) Dies ist die ANSI-Darstellung des Feldnamens. 
    
- FormulaANSI: Eine PackedAnsiString-Datenstromstruktur. Dies ist eine ANSI-Darstellung der Berechnungsformel für das Feld. Sie wird im  Abschnitt Initial Value der Registerkarte **Wert** des Dialogfelds Eigenschaften eines Formularsteuerelements angezeigt, das an dieses Feld gebunden ist.  
    
- ValidationRuleANSI: Eine PackedAnsiString-Datenstromstruktur. Dies ist eine ANSI-Darstellung der Gültigkeitsprüfungsformel des Felds. Sie wird im Textfeld für die **Gültigkeitsprüfungsformel** auf der Registerkarte **Überprüfung** des Dialogfelds **Eigenschaften** eines Formularsteuerelements angezeigt, das an dieses Feld gebunden ist. 
    
- ValidationTextANSI: Eine PackedAnsiString-Datenstromstruktur. Dies ist eine ANSI-Darstellung des Überprüfungsfehlertexts des Felds. Sie wird im Textfeld zum Anzeigen dieser Meldung angezeigt, wenn die Überprüfung auf der Registerkarte **"Überprüfung"** des Dialogfelds **"Eigenschaften"** eines An dieses Feld gebundenen Formularsteuerelements **fehlschlägt.** 
    
- ErrorANSI: Eine PackedAnsiString-Datenstromstruktur. Outlook verwendet dieses Element nicht; Sie sollten dieses Element auf eine leere Zeichenfolge festlegen.
    
- InternalType: DWORD (4 Bytes), der interne Feldtyp. Dieses Datenelement ist nur vorhanden, wenn das Felddefinitionsformat PropDefV2 lautet. Der interne Typ ist einer der folgenden Werte, von denen jeder einem Typ im Dialogfeld **Neues Feld** für benutzerdefinierte Felder entspricht. 
    
    |**Interner Typname**|**Wert**|**Entsprechender Typ im Dialogfeld **"Neues Feld"****|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**Number** <br/> |
    |iTypePercent  <br/> |2  <br/> |**Percent** <br/> |
    |Währung  <br/> |3  <br/> |**Currency** <br/> |
    |iTypeBool  <br/> |4   <br/> |**Yes/No** <br/> |
    |iTypeDateTime  <br/> |5  <br/> |**Datum/Uhrzeit** <br/> |
    |iTypeDuration  <br/> |6   <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7   <br/> |**Kombination**, wobei **nur das erste nicht leere Feld angezeigt wird, wobei nachfolgende Optionen ignoriert werden,** die im Dialogfeld **Kombinationsformelfeld** ausgewählt sind.  <br/> |
    |iTypeFormula  <br/> |8   <br/> |**Formel** <br/> |
    |iTypeResult  <br/> |9   <br/> |Dieser Typ wird nicht für benutzerdefinierte Felder verwendet.  <br/> |
    |iTypeVariant  <br/> |10  <br/> |Dieser Typ wird nicht für benutzerdefinierte Felder verwendet.  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |Dieser Typ wird nicht für benutzerdefinierte Felder verwendet.  <br/> |
    |iTypeConcat  <br/> |12   <br/> |**Kombination**, wobei die **Verknüpfungsfelder und alle Textfragmente miteinander** im Dialogfeld **Kombinationsformelfeld** ausgewählt sind.  <br/> |
    |iTypeKeywords  <br/> |13  <br/> |**Schlüsselwort** <br/> |
    |iTypeInteger  <br/> |14   <br/> |**Integer** <br/> |
   
- SkipBlocks: Eine Reihe von einer oder mehreren [SkipBlock-Streamstrukturen.](skipblock-stream-structure.md) Dieses Datenelement ist nur vorhanden, wenn das Felddefinitionsformat PropDefV2 lautet. Wenn das Felddefinitionsformat PropDefV2 lautet, sollte die Datenreihe mindestens eine SkipBlock-Struktur enthalten, die SkipBlock-Struktur, deren Size-Datenelement gleich 0 ist, und die Datenreihe sollte mit dieser SkipBlock-Struktur beginnen und beenden. 
    
   Der Zweck einer SkipBlock-Struktur hängt von ihrer relativen Position in der SkipBlocks-Reihe ab. Wenn die Felddefinition im PropDefV2-Format vorliegt und die erste Struktur nicht die endende Struktur ist (das Size-Datenelement ist größer als 0), geht Outlook davon aus, dass die erste SkipBlock-Struktur den Feldnamen in Unicode (UTF-16) angibt. 
    
   > [!IMPORTANT]
   > Wenn der erste SkipBlock die Abbruchstruktur ist, wird das NameANSI-Datenelement verwendet, um den Feldnamen zu bestimmen. Wenn diese Zeichenfolge Nicht-ASCII-Zeichen enthält, können diese Zeichen abhängig von der ANSI-Codeseite des Computers, auf dem Outlook ausgeführt wird, inkonsistent interpretiert werden. Um solche Inkonsistenzen zu vermeiden, müssen Sie immer den ersten SkipBlock in felddefinitionen angeben, die Sie erstellen, zumindest wenn der Feldname Nicht-ASCII-Zeichen enthält. 
  
   Wenn eine zukünftige Version eines Felddefinitionsformats zusätzliche Datenelemente im FieldDefinition-Datenstrom einführt, können diese Daten als zusätzliche SkipBlock-Datenstromstrukturen in der SkipBlocks-Reihe gespeichert werden, bevor die SkipBlock-Struktur beendet wird, deren Size-Datenelement gleich 0 ist. Frühere Versionen von Outlook können diese zusätzlichen SkipBlock-Strukturen bis zur abbruchenden SkipBlock-Struktur problemlos ignorieren und trotzdem alle unterstützten Blöcke ordnungsgemäß verarbeiten.
    
## <a name="see-also"></a>Siehe auch

- [Outlook Elemente und Felder](outlook-items-and-fields.md)
- [Stream-Strukturen](stream-structures.md)
- [PropertyDefinition-Datenstromstruktur](propertydefinition-stream-structure.md)

