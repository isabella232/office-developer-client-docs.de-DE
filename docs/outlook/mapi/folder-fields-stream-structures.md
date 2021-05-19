---
title: Ordnerfelder Streamstrukturen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96051bd2b62fd7c0e908a1018aac0225e44986be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336890"
---
# <a name="folder-fields-stream-structures"></a>Ordnerfelder Streamstrukturen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die [PidTagUserFields-Eigenschaft](pidtaguserfields-canonical-property.md) einer Nachricht enthält einen binären Datenstrom, FolderUserFields, der die benutzerdefinierten Felddefinitionen des Ordners enthält. In diesem Thema werden die Streamstrukturen für benutzerdefinierte Felddefinitionen für Ordner beschrieben. 

Eine FolderUserFields-Streamstruktur besteht entweder aus einer FolderUserFieldsA-Struktur oder einer FolderUserFieldsA-Struktur gefolgt von einer FolderUserFieldsW-Struktur.
  
Datenelemente in diesem Datenstrom werden unmittelbar aufeinander folgend in der folgenden angegebenen Reihenfolge gespeichert:
  
- **FolderUserFieldsAnsi**: Eine FolderUserFieldsA-Streamstruktur.
    
- **FolderUserFieldsUnicode** (optional): Eine FolderUserFieldsW-Streamstruktur.
    
Das Vorhandensein von FolderUserFieldsUnicode wird durch die Gesamtlänge der FolderUserFields erkannt, die größer als die Länge von FolderUserFieldsAnsi ist.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi wird zur Kompatibilität mit älteren Versionen von MAPI-Clients verwendet, die nicht unicode sind. Wenn FolderUserFieldsUnicode vorhanden ist, wird der Inhalt von FolderUserFieldsAnsi ignoriert. Um mögliche Datenverluste bei der ANSI-Konvertierung zu vermeiden, schließen Sie beim Erstellen eines FolderUserFields-Datenstroms immer den FolderUserFieldsW-Teil ein. 
  
## <a name="folderuserfieldsa-stream-structure"></a>FolderUserFieldsA Stream Structure

Eine FolderUserFieldsA-Streamstruktur ist ein Array von FolderFieldDefinitionA-Streamstrukturen, die Definitionen für alle benutzerdefinierten Felder in einem Outlook-Ordner enthalten, es sei denn, der FolderUserFieldsW-Teil der FolderUserFields-Struktur überschreiben.
  
Datenelemente in diesem Datenstrom werden in der Bytereihenfolge little-endian gespeichert, die in der folgenden angegebenen Reihenfolge unmittelbar aufeinander folgt:
  
- **FieldDefinitionCount**: DWORD (4 Byte), die Anzahl der Felddefinitionen in diesem Datenstrom. Dies ist die Anzahl der Elemente im **FieldDefinitions-Array.**
    
- **FieldDefinitions**: Ein Array von FolderFieldDefinitionA-Streamstrukturen. Die Anzahl dieses Arrays entspricht dem **FieldDefinitionCount-Datenelement.**
    
Wenn diese FolderUserFieldsA nicht vom FolderUserFieldsW-Teil der FolderUserFields-Struktur überschrieben wird, muss das **FieldDefinitions-Array** "null-terminated" sein, indem das Common.FieldType-Feld des letzten FolderFieldDefinitionA-Elements dem Feld "ftNull" entspricht.
  
## <a name="folderuserfieldsw-stream-structure"></a>FolderUserFieldsW Stream Structure

Eine FolderUserFieldsW-Streamstruktur ist ein Array von FolderFieldDefinitionW-Streamstrukturen, die Definitionen für alle benutzerdefinierten Felder in einem Outlook-Ordner enthalten.
  
Datenelemente in diesem Datenstrom werden in der Bytereihenfolge little-endian gespeichert, die in der folgenden angegebenen Reihenfolge unmittelbar aufeinander folgt:
  
- **FieldDefinitionCount**: DWORD (4 Byte), die Anzahl der Felddefinitionen in diesem Datenstrom. Dies ist die Anzahl der Elemente im **FieldDefinitions-Array.**
    
- **FieldDefinitions**: Ein Array von FolderFieldDefinitionW-Streamstrukturen. Die Anzahl dieses Arrays entspricht dem **FieldDefinitionCount-Datenelement.**
    
Das **FieldDefinitions-Array** muss "null-terminated" sein, indem das Common.FieldType-Feld des letzten FolderFieldDefinitionW-Elements dem Wert ftNull entspricht.
  
## <a name="folderfielddefinitiona-stream-structure"></a>FolderFieldDefinitionA Stream Structure

Eine FolderFieldDefinitionA-Streamstruktur enthält eine Definition eines benutzerdefinierten Felds mit dem in ANSI gespeicherten Feldnamen.
  
Datenelemente in diesem Datenstrom werden in der Bytereihenfolge little-endian gespeichert, die in der folgenden angegebenen Reihenfolge unmittelbar aufeinander folgt:
  
- **FieldType**: FldType (4 Byte), der Typ dieses Felds.
    
- **FieldNameLength**: WORD (2 Byte), die Anzahl der Elemente im **FieldName-Array.**
    
- **FieldName**: Ein Array von CHAR. Dies ist die ANSI-CP_ACP Codepagedarstellung des Feldnamens. Die Anzahl dieses Arrays ist gleich **FieldNameLength**. Der Feldname muss die Einschränkungen für den Parameter Name erfüllen, wie in der [UserProperties.Add-Methode](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) angegeben. 
    
   > [!NOTE]
   > Aus Gründen der Legacykompatibilität kann Outlook möglicherweise einige **FieldName-Werte** verarbeiten, die diese Einschränkungen nicht erfüllen. Solche Fälle werden jedoch nicht in diesem Thema behandelt. 
  
- **Common**: Eine FolderFieldDefinitionCommon-Streamstruktur.
    
## <a name="folderfielddefinitionw-stream-structure"></a>FolderFieldDefinitionW Stream Structure

Eine FolderFieldDefinitionW-Streamstruktur enthält eine Definition eines benutzerdefinierten Felds mit dem in Unicode gespeicherten Feldnamen.
  
Datenelemente in diesem Datenstrom werden in der Bytereihenfolge little-endian gespeichert, die in der folgenden angegebenen Reihenfolge unmittelbar aufeinander folgt:
  
- **FieldType**: FldType (4 Byte), der Typ dieses Felds.
    
- **FieldNameLength**: WORD (2 Byte), die Anzahl der Elemente im **FieldName-Array.**
    
- **FieldName**: Ein Array von WCHAR. Dies ist die Unicode-Darstellung (UTF-16) des Feldnamens. Die Anzahl dieses Arrays ist gleich **FieldNameLength**. Der Feldname muss die Einschränkungen für den Parameter Name erfüllen, wie in der [UserProperties.Add-Methode](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) angegeben. 
    
   > [!NOTE]
   > Aus Gründen der Legacykompatibilität kann Outlook möglicherweise einige **FieldName-Werte** verarbeiten, die diese Einschränkungen nicht erfüllen, aber solche Fälle werden in diesem Thema nicht behandelt. 
  
- **Common**: Eine FolderFieldDefinitionCommon-Streamstruktur.
    
## <a name="fldtype-enumeration"></a>FldType-Aufzählung

**Die Werte der FldType-Enumeration** sind in der folgenden Tabelle aufgeführt. 
  
|Name|Wert|Bedeutung|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |Dieser Feldtyp wird verwendet, um ein Array von Felddefinitionen zu beenden.  <br/> |
|ftString  <br/> |0x1  <br/> |Text  <br/> |
|ftInteger  <br/> |0x3  <br/> |Ganze Zahl  <br/> |
|ftTime  <br/> |0x5  <br/> |Datum/Uhrzeit  <br/> |
|ftBoolean  <br/> |0x6  <br/> |Ja/Nein  <br/> |
|ftDuration  <br/> |0x7  <br/> |Dauer  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Schlüsselwörter  <br/> |
|ftFloat  <br/> |0xC  <br/> |Zahl oder Prozent  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Währung  <br/> |
|ftCalc  <br/> |0x12  <br/> |Formel  <br/> |
|ftSwitch  <br/> |0x13  <br/> |Kombination des Typs, der nur das erste nicht leere Feld zeigt , wobei nachfolgende ignoriert werden.  <br/> |
|ftConcat  <br/> |0x17  <br/> |Kombination aus Typ verbindenden Feldern und textfragmenten miteinander.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>FolderFieldDefinitionCommon Stream Structure

Eine FolderFieldDefinitionCommon-Streamstruktur enthält die Daten einer benutzerdefinierten Felddefinition, die sowohl für FolderFieldDefinitionA als auch für FolderFieldDefinitionW verwendet wird.
  
Datenelemente in diesem Datenstrom werden in der Bytereihenfolge little-endian gespeichert, die in der folgenden angegebenen Reihenfolge unmittelbar aufeinander folgt:
  
- **PropSetGuid**: GUID (16 Byte), die GuiD des entsprechenden MAPI-Eigenschaftsnamens des Ordnerfelds festlegen. Der Wert dieses Felds muss gleich PS_PUBLIC_STRINGS sein, es sei denn, der Feldtyp ist **ftNone,** in diesem Fall muss der Wert dieses Felds gleich GUID_NULL. 
    
   > [!NOTE]
   > Aus Gründen der Legacykompatibilität kann Outlook möglicherweise einige **PropSetGuid-Werte** verarbeiten, die diese Einschränkung nicht erfüllen. Solche Fälle werden jedoch nicht in diesem Thema behandelt. 
  
- **fcapm**: DWORD (4 Byte), eine Kombination aus Null oder mehr kennzeichnet die Werte, deren Werte und Bedeutungen in der folgenden Tabelle aufgeführt sind. Flags mit demselben Wert haben Bedeutungen, die vom Typ des Felds abhängen, d. h. vom FldType-Wert.
    
    |Kennzeichenname|Wert|Bedeutung|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |Das Feld kann bearbeitet werden.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |Das Feld kann sortiert werden.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |Das Feld kann gruppieren.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |Das Feld kann mehrere Textzeilen enthalten.  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |Dieses Feld vom Typ ftFloat ist ein Prozentfeld.  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |Dieses Feld vom Typ "ftTime" ist ein Datums-/Uhrzeitfeld.  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |Für dieses Feld vom Typ ftInteger ist keine Einheit im Anzeigeformat zulässig. z. B. Formate wie "Computer - 640 K..." sind nicht zulässig.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |Das Feld kann im Element bearbeitet werden: Dies gilt speziell für benutzerdefinierte Formulare.  <br/> |
   
- **dwString**: DWORD (4 Byte). Weitere Informationen finden Sie im ersten Hinweis.
    
- **dwBitmap**: DWORD (4 Byte). Weitere Informationen finden Sie im ersten Hinweis.
    
- **dwDisplay**: DWORD (4 Byte). Weitere Informationen finden Sie im ersten Hinweis.
    
- **iFmt**: INT (4 Byte). Für die Feldtypen mit dem Kombinationsfeld "Format:" im Dialogfeld "Neues Feld", "Feld bearbeiten" und "Feldeigenschaften" ist der 0-basierte Index des in diesem Kombinationsfeld ausgewählten Formats. Für die Feldtypen ohne dieses Kombinationsfeld muss dies 0 sein. Der Wert des Felds zusammen mit dem Feldtyp bestimmt die Werte der Felder **dwString,** **dwBitmap** und **dwDisplay** eindeutig. Weitere Informationen finden Sie im ersten hinweis.
    
- **wszFormulaLength**: WORD (2 Byte), die Anzahl der Elemente im **wszFormulaLength-Array.**
    
- **wszFormulaLength**: Ein Array von WCHAR. Dies ist die Unicode-Darstellung (UTF-16) der Formelzeichenfolge des Felds im Standardformat. Im zweiten Hinweis finden Sie eine Beschreibung der Standard- und Benutzeroberflächenformate der Formel eines Felds. Die Anzahl dieses Arrays ist gleich **wszFormulaLength**. Die Formelzeichenfolge muss eine leere Zeichenfolge sein, es sei denn, der Feldtyp ist **ftCalc,** **ftSwitch** oder **ftConcat**.
    
> [!NOTE]
> Obwohl die Werte von **dwString,** **dwBitmap** und **dwDisplay** basierend auf dem **FldType-Wert** und dem **redundanten iFmt-Wert** eindeutig bestimmt werden, sind die richtigen Werte weiterhin für die ordnungsgemäße Verarbeitung der Felddefinition durch Outlook erforderlich. Es gibt keine einfache Beschreibung des Algorithmus, der diese Bestimmung ausführt. 
> 
> Um herauszufinden, welche **Werte für dwString,** **dwBitmap** und **dwDisplay** einem bestimmten **FldType-** und **iFmt-Wert** entsprechen, führen Sie daher einen Test durch, indem Sie ein benutzerdefiniertes Feld dieses Typs erstellen, und überprüfen Sie den resultierenden **FolderUserFields-Datenstrom,** den Outlook für dieses benutzerdefinierte Feld erstellt, mit dem im Kombinationsfeld **Format** ausgewählten Format unter Annahme seiner Anwendbarkeit. 
  
Die Formel des Felds im Benutzeroberflächenformat wird im Textfeld **Formel** der Dialogfelder Neue **Feld-,** **Bearbeitungsfeld-** und **Feldeigenschaften** für das benutzerdefinierte Feld bearbeitet. Der Algorithmus zum Konvertieren einer Formel aus dem Benutzeroberflächenformat in das Standardformat hängt vom Feldtyp ab, wie im Folgenden beschrieben: 
- Bei Feldern der Typen **ftCalc** und **ftSwitch** wird das Standardformat für integrierte Felder, bei denen die entsprechenden MAPI-Eigenschaften keine Benannteigenschaften der Art MNID STRING sind, durch Ersetzen von Feldnamenfragmenten, d. h. durch Fragmente, \_ `[<field_name>]` `[_<field_dispid_decimal>]` erhalten. 

  Wenn z. B. das Benutzeroberflächenformat einer Formel für ein Feld vom Typ **Formula**, d. h. **ftCalc,** mit der Office-Ui-Sprache `[Business Phone] & [My custom field]` US-Englisch ist, ist , wobei der Name eines benutzerdefinierten Felds ist, wäre das Standardformat einer solchen Formel `My custom field` `[_14856] & [My custom field]` .

- Für Felder vom Typ **ftConcat** wird das Standardformat durch Ausführen der folgenden Schritte erhalten:

  1. Vor- und Nachgestellter Whitespace abschneiden. 
  2. Analysieren Sie die Formel in eine Abfolge von Fragmenten der folgenden beiden Arten: 
     - Ein Feldname in eckigen Klammern, d. h. `[<field_name>]` . 
     - Eine Teilzeichenfolge, die keine eckigen Klammern enthält.   
      Stellen Sie sicher, dass in der Sequenz keine zwei Fragmente der zweiten Art nebeneinander liegen. Wenn die Formel nicht auf diese Weise analysiert werden kann, wird sie als ungültig betrachtet. 
  3. Führen Sie denselben Ersatz für Fragmente der ersten Art aus wie für **die Felder ftCalc** und **ftSwitch.** 
  4. Escapen Sie für jedes Fragment der zweiten Art alle Doppelanführungszeichen (""") mit zwei aufeinander folgenden Doppelanführungszeichen, und setzen Sie es in doppelte Anführungszeichen. 
  5. Fügen Sie zwischen jedem Paar benachbarter Fragmente eine kaufmännische Zeichenfolge ( `&` ) ein.
 
  Wenn z. B. die Office-UI-Sprache US-Englisch verwendet wird, wenn das Benutzeroberflächenformat einer Formel für ein Feld vom Typ **ftConcat** ist, wobei der Name eines benutzerdefinierten Felds ist, ist das Standardformat für eine solche Formel `text1 [Business Phone] "text2" [My custom field]` `My custom field` `""text1" & [_14856] & """text2""" & [My custom field]"` . 
  
## <a name="see-also"></a>Siehe auch

- [FolderUserFields-Streambeispiel](folderuserfields-stream-sample.md)
- [Hinzufügen einer Definition für ein new User-Defined Field](how-to-add-a-definition-for-a-new-user-defined-field.md)

