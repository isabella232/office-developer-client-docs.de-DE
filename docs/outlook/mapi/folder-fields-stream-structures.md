---
title: Streamstrukturen für Ordnerfelder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 22b0b3678b5c0cd5690bfb76ed7680b259cf9039
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561796"
---
# <a name="folder-fields-stream-structures"></a>Streamstrukturen für Ordnerfelder

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die [PidTagUserFields-Eigenschaft](pidtaguserfields-canonical-property.md) einer Nachricht enthält einen binären Datenstrom, FolderUserFields, der die benutzerdefinierten Felddefinitionen des Ordners enthält. In diesem Thema werden die Datenstromstrukturen für benutzerdefinierte Ordnerfelddefinitionen beschrieben. 

Eine FolderUserFields-Streamstruktur besteht entweder aus einer FolderUserFieldsA-Struktur oder einer FolderUserFieldsA-Struktur gefolgt von einer FolderUserFieldsW-Struktur.
  
Datenelemente in diesem Datenstrom werden unmittelbar nacheinander in der folgenden angegebenen Reihenfolge gespeichert:
  
- **FolderUserFieldsAnsi**: Eine FolderUserFieldsA-Datenstromstruktur.
    
- **FolderUserFieldsUnicode** (optional): Eine FolderUserFieldsW-Streamstruktur.
    
Das Vorhandensein von FolderUserFieldsUnicode wird dadurch erkannt, dass die Gesamtlänge der FolderUserFields größer als die Länge von FolderUserFieldsAnsi ist.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi wird aus Gründen der Kompatibilität mit älteren, nicht unicodefähigen Versionen von MAPI-Clients verwendet. Wenn FolderUserFieldsUnicode vorhanden ist, wird der Inhalt von FolderUserFieldsAnsi ignoriert. Um möglichen Datenverlust bei der ANSI-Konvertierung zu vermeiden, schließen Sie beim Erstellen eines FolderUserFields-Datenstroms immer den FolderUserFieldsW-Teil ein. 
  
## <a name="folderuserfieldsa-stream-structure"></a>FolderUserFieldsA-Streamstruktur

Eine FolderUserFieldsA-Datenstromstruktur ist ein Array von FolderFieldDefinitionA-Datenstromstrukturen, die Definitionen für alle benutzerdefinierten Felder in einem Outlook Ordner enthalten, es sei denn, sie wird vom FolderUserFieldsW-Teil der FolderUserFields-Struktur außer Kraft gesetzt.
  
Datenelemente in diesem Datenstrom werden in kleiner endischer Bytereihenfolge gespeichert und folgen einander in der folgenden angegebenen Reihenfolge:
  
- **FieldDefinitionCount**: DWORD (4 Bytes), die Anzahl der Felddefinitionen in diesem Datenstrom. Dies ist die Anzahl der Elemente im **FieldDefinitions-Array.**
    
- **FieldDefinitions**: Ein Array von FolderFieldDefinitionA-Datenstromstrukturen. Die Anzahl dieses Arrays entspricht dem **FieldDefinitionCount-Datenelement.**
    
Wenn dieses FolderUserFieldsA-Objekt nicht vom FolderUserFieldsW-Teil der FolderUserFields-Struktur überschrieben wird, muss das **FieldDefinitions-Array** "null-terminated" sein, indem das Common.FieldType-Feld des letzten FolderFieldDefinitionA-Elements gleich ftNull ist.
  
## <a name="folderuserfieldsw-stream-structure"></a>FolderUserFieldsW-Streamstruktur

Eine FolderUserFieldsW-Datenstromstruktur ist ein Array von FolderFieldDefinitionW-Datenstromstrukturen, die Definitionen für alle benutzerdefinierten Felder in einem Outlook Ordner enthalten.
  
Datenelemente in diesem Datenstrom werden in kleiner endischer Bytereihenfolge gespeichert und folgen einander in der folgenden angegebenen Reihenfolge:
  
- **FieldDefinitionCount**: DWORD (4 Bytes), die Anzahl der Felddefinitionen in diesem Datenstrom. Dies ist die Anzahl der Elemente im **FieldDefinitions-Array.**
    
- **FieldDefinitions**: Ein Array von FolderFieldDefinitionW-Datenstromstrukturen. Die Anzahl dieses Arrays entspricht dem **FieldDefinitionCount-Datenelement.**
    
The **FieldDefinitions** array must be "null-terminated" by having its last FolderFieldDefinitionW element's Common.FieldType field equal to ftNull.
  
## <a name="folderfielddefinitiona-stream-structure"></a>FolderFieldDefinitiona-Datenstromstruktur

Eine FolderFieldDefinitionA-Datenstromstruktur enthält eine Definition eines benutzerdefinierten Felds mit dem in ANSI gespeicherten Feldnamen.
  
Datenelemente in diesem Datenstrom werden in kleiner endischer Bytereihenfolge gespeichert und folgen einander in der folgenden angegebenen Reihenfolge:
  
- **FieldType**: FldType (4 Bytes), der Typ dieses Felds.
    
- **FieldNameLength**: WORD (2 Bytes), die Anzahl der Elemente im **FieldName-Array.**
    
- **FieldName**: Ein Array von CHAR. Dies ist die ANSI-CP_ACP Codepage-Darstellung des Feldnamens. Die Anzahl dieses Arrays ist gleich **FieldNameLength**. Der Feldname muss die Einschränkungen für den Name-Parameter erfüllen, wie in der [UserProperties.Add-Methode](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) angegeben. 
    
   > [!NOTE]
   > Aus Gründen der Legacykompatibilität können Outlook möglicherweise einige **FieldName-Werte** verarbeiten, die diese Einschränkungen nicht erfüllen, aber solche Fälle werden in diesem Thema nicht behandelt. 
  
- **Häufig:** Eine FolderFieldDefinitionCommon-Datenstromstruktur.
    
## <a name="folderfielddefinitionw-stream-structure"></a>FolderFieldDefinitionW-Streamstruktur

Eine FolderFieldDefinitionW-Datenstromstruktur enthält eine Definition eines benutzerdefinierten Felds mit dem in Unicode gespeicherten Feldnamen.
  
Datenelemente in diesem Datenstrom werden in kleiner endischer Bytereihenfolge gespeichert und folgen einander in der folgenden angegebenen Reihenfolge:
  
- **FieldType**: FldType (4 Bytes), der Typ dieses Felds.
    
- **FieldNameLength**: WORD (2 Bytes), die Anzahl der Elemente im **FieldName-Array.**
    
- **FieldName**: Ein Array von WCHAR. Dies ist die Unicode-Darstellung (UTF-16) des Feldnamens. Die Anzahl dieses Arrays ist gleich **FieldNameLength**. Der Feldname muss die Einschränkungen für den Name-Parameter erfüllen, wie in der [UserProperties.Add-Methode](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) angegeben. 
    
   > [!NOTE]
   > Aus Gründen der Legacykompatibilität können Outlook möglicherweise einige **FieldName-Werte** verarbeiten, die diese Einschränkungen nicht erfüllen, aber solche Fälle werden in diesem Thema nicht behandelt. 
  
- **Häufig:** Eine FolderFieldDefinitionCommon-Datenstromstruktur.
    
## <a name="fldtype-enumeration"></a>FldType-Enumeration

**FldType-Enumerationswerte** sind in der folgenden Tabelle aufgeführt. 
  
|Name|Wert|Bedeutung|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |Dieser Feldtyp wird verwendet, um ein Array von Felddefinitionen mit Null zu beenden.  <br/> |
|ftString  <br/> |0x1  <br/> |Text  <br/> |
|ftInteger  <br/> |0x3  <br/> |Ganze Zahl  <br/> |
|ftTime  <br/> |0x5  <br/> |Datum/Uhrzeit  <br/> |
|ftBoolean  <br/> |0x6  <br/> |Ja/Nein  <br/> |
|ftDuration  <br/> |0x7  <br/> |Dauer  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Schlüsselwörter  <br/> |
|ftFloat  <br/> |0xC  <br/> |Zahl oder Prozent  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Währung  <br/> |
|ftCalc  <br/> |0x12  <br/> |Formel  <br/> |
|ftSwitch  <br/> |0x13  <br/> |Kombination aus Typ, der nur das erste nicht leere Feld anzeigt– ignoriert nachfolgende Felder.  <br/> |
|ftConcat  <br/> |0x17  <br/> |Kombination aus Typ, der Felder und alle Textfragmente miteinander verknüpfen.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>FolderFieldDefinitionCommon-Streamstruktur

Eine FolderFieldDefinitionCommon-Datenstromstruktur enthält die Daten einer benutzerdefinierten Felddefinition, die sowohl einem FolderFieldDefinitionA- als auch einem FolderFieldDefinitionW-Objekt gemeinsam ist.
  
Datenelemente in diesem Datenstrom werden in kleiner endischer Bytereihenfolge gespeichert und folgen einander in der folgenden angegebenen Reihenfolge:
  
- **PropSetGuid**: GUID (16 Bytes), die Guid des Eigenschaftssatzes des entsprechenden MAPI-Eigenschaftsnamens des Ordnerfelds. Der Wert dieses Felds muss PS_PUBLIC_STRINGS entsprechen, es sei denn, der Feldtyp ist **"ftNone",** in diesem Fall muss der Wert dieses Felds gleich GUID_NULL sein. 
    
   > [!NOTE]
   > Aus Gründen der Legacykompatibilität können Outlook möglicherweise einige **PropSetGuid-Werte** verarbeiten, die diese Einschränkung nicht erfüllen, aber solche Fälle werden in diesem Thema nicht behandelt. 
  
- **fcapm**: DWORD (4 Bytes), eine Kombination aus Null oder mehr Flags, deren Werte und Bedeutungen in der folgenden Tabelle aufgeführt sind. Flags mit demselben Wert haben Bedeutungen, die vom Typ des Felds abhängig sind, d. h. dem FldType-Wert.
    
    |Kennzeichenname|Wert|Bedeutung|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |Das Feld kann bearbeitet werden.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |Das Feld kann sortiert werden.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |Das Feld kann gruppiert werden.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |Das Feld kann mehrere Textzeilen enthalten.  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |Dieses Feld vom Typ "ftFloat" ist ein Prozentfeld.  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |Dieses Feld vom Typ "ftTime" ist ein datumsgeschütztes Zeitfeld.  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |Für dieses Feld vom Typ "ftInteger" ist keine Einheit im Anzeigeformat zulässig. z. B. Formate wie "Computer - 640 K..." sind nicht zulässig.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |Das Feld kann im Element bearbeitet werden: Dies gilt speziell für benutzerdefinierte Formulare.  <br/> |
   
- **zeichenfolge**: DWORD (4 Bytes). Siehe den ersten folgenden Hinweis.
    
- **orbitBitmap**: DWORD (4 Bytes). Siehe den ersten folgenden Hinweis.
    
- **wetterDisplay**: DWORD (4 Byte). Siehe den ersten folgenden Hinweis.
    
- **iFmt**: INT (4 Bytes). Für die Feldtypen mit dem Kombinationsfeld "Format:" in den Dialogfeldern "Neues Feld", "Feld bearbeiten" und "Feldeigenschaften" der 0-basierte Index des in diesem Kombinationsfeld ausgewählten Formats. Für die Feldtypen ohne dieses Kombinationsfeld muss dies 0 sein. Der Wert des Felds und der Feldtyp bestimmen eindeutig die Werte der Felder **wetterString,** **wetterBitmap** und wetterDisplay. 
    
- **wszFormulaLength**: WORD (2 Bytes), die Anzahl der Elemente im **wszFormulaLength-Array.**
    
- **wszFormulaLength**: Ein Array von WCHAR. Dies ist die Unicode-Darstellung (UTF-16) der Formelzeichenfolge des Felds im Standardformat. Im zweiten folgenden Hinweis finden Sie eine Beschreibung der Standard- und Ui-Formate der Formel eines Felds. Die Anzahl dieses Arrays ist gleich **wszFormulaLength**. Die Formelzeichenfolge muss eine leere Zeichenfolge sein, es sei denn, der Feldtyp ist **ftCalc**, **ftSwitch** oder **ftConcat**.
    
> [!NOTE]
> Obwohl die Werte von **"wetterString",** **"wetterBitmap"** und **"wetterDisplay"** eindeutig anhand des **FldType-Werts** und des **redundanten iFmt-Werts** bestimmt werden, sind ihre korrekten Werte dennoch für die korrekte Verarbeitung der Felddefinition durch Outlook erforderlich. Es gibt keine einfache Beschreibung des Algorithmus, der diese Bestimmung durchführt. 
> 
> Um herauszufinden, welche **Werte für "rehString",** **"wetterBitmap"** und **"wetterDisplay"** einem bestimmten **FldType-** und **iFmt-Wert** entsprechen, führen Sie einen Test durch, indem Sie ein benutzerdefiniertes Feld dieses Typs erstellen und mit diesem Format, das im Kombinationsfeld **Format** ausgewählt ist, unter der Voraussetzung, dass es anwendbar ist, den resultierenden **FolderUserFields-Datenstrom** überprüfen, den Outlook für dieses benutzerdefinierte Feld erstellt. 
  
Die Formel des Felds im Ui-Format wird im **Textfeld Formel** des Dialogfelds **Neues** Feld, Feld **bearbeiten** und Feldeigenschaften für das benutzerdefinierte Feld bearbeitet.  Der Algorithmus zum Konvertieren einer Formel aus dem BENUTZERoberflächenformat in das Standardformat hängt vom Feldtyp ab, wie in den folgenden Schritten beschrieben: 
- Für Felder der Typen **ftCalc** und **ftSwitch** wird das Standardformat für integrierte Felder, bei denen die entsprechenden MAPI-Eigenschaften keine benannten Eigenschaften der Art MNID \_ STRING sind, durch Ersetzen von Feldnamenfragmenten, d. h. `[<field_name>]` durch Fragmente, `[_<field_dispid_decimal>]` abgerufen. 

  Wenn z. B. das Benutzeroberflächenformat einer Formel für ein Feld vom Typ Formula, d. h. **ftCalc,** mit Office us-englischer Sprache (US-Englisch) entspricht, wobei der Name eines  `[Business Phone] & [My custom field]` `My custom field` benutzerdefinierten Felds angegeben ist, lautet das Standardformat einer solchen Formel `[_14856] & [My custom field]` .

- Für Felder vom Typ **"ftConcat"** wird das Standardformat abgerufen, indem Folgendes ausgeführt wird:

  1. Führende und nachfolgende Leerzeichen abschneiden. 
  2. Analysieren Sie die Formel in eine Sequenz von Fragmenten der folgenden beiden Arten: 
     - Ein Feldname in eckigen Klammern, d. h. `[<field_name>]` . 
     - Eine Teilzeichenfolge, die keine eckigen Klammern enthält.   
      Stellen Sie sicher, dass in der Sequenz keine zwei Fragmente der zweiten Art nebeneinander angeordnet sind. Wenn die Formel nicht auf diese Weise analysiert werden kann, wird sie als ungültig betrachtet. 
  3. Führen Sie den gleichen Ersatz für Fragmente der ersten Art wie für die **Felder "ftCalc"** und **"ftSwitch" aus.** 
  4. Für jedes Fragment der zweiten Art escapen Sie alle Zeichen mit doppeltem Anführungszeichen ("""), falls vorhanden, mit zwei aufeinander folgenden doppelten Anführungszeichen, und schließen Sie es in doppelte Anführungszeichen ein. 
  5. Fügen Sie eine kaufmännische Und-Zeichenfolge ( `&` ) zwischen jedem Paar benachbarter Fragmente ein.
 
  Wenn z. B. die Office BENUTZERoberflächensprache US-Englisch verwendet wird, wenn das Benutzeroberflächenformat einer Formel für ein Feld vom Typ **"ftConcat"** den `text1 [Business Phone] "text2" [My custom field]` Namen eines `My custom field` benutzerdefinierten Felds aufweist, lautet das Standardformat für eine solche Formel `""text1" & [_14856] & """text2""" & [My custom field]"` . 
  
## <a name="see-also"></a>Siehe auch

- [FolderUserFields Stream-Beispiel](folderuserfields-stream-sample.md)
- [Hinzufügen einer Definition für ein Neues User-Defined Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)

