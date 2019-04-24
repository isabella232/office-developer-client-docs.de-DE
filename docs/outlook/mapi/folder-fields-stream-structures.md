---
title: Ordnerfelder Stream-Strukturen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 96051bd2b62fd7c0e908a1018aac0225e44986be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336890"
---
# <a name="folder-fields-stream-structures"></a>Ordnerfelder Stream-Strukturen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die [pidtaguserfields (](pidtaguserfields-canonical-property.md) -Eigenschaft einer Nachricht enthält einen binären Stream Beispiel für folderuserfields, der die benutzerdefinierten Felddefinitionen des Ordners enthält. In diesem Thema werden die Datenstrom Strukturen für benutzerdefinierte Ordner Felddefinitionen beschrieben. 

Eine Beispiel für folderuserfields-Datenstrom Struktur besteht entweder aus einer FolderUserFieldsA-Struktur oder einer FolderUserFieldsA-Struktur, gefolgt von einer FolderUserFieldsW-Struktur.
  
Datenelemente in diesem Stream werden unmittelbar nach einander in der folgenden angegebenen Reihenfolge gespeichert:
  
- **FolderUserFieldsAnsi**: eine FolderUserFieldsA-Datenstrom Struktur.
    
- **FolderUserFieldsUnicode** (optional): eine FolderUserFieldsW-Datenstrom Struktur.
    
Das vorhanden sein von FolderUserFieldsUnicode wird durch die Gesamtlänge der Beispiel für folderuserfields erkannt, die größer als die Länge von FolderUserFieldsAnsi ist.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi wird zur Kompatibilität mit älteren, nicht-Unicode-Versionen von MAPI-Clients verwendet, daher wird der Inhalt von FolderUserFieldsAnsi ignoriert, wenn FolderUserFieldsUnicode vorhanden ist. Um mögliche Datenverluste bei der ANSI-Konvertierung zu vermeiden, müssen Sie beim Erstellen eines Beispiel für folderuserfields-Streams immer den FolderUserFieldsW-Teil verwenden. 
  
## <a name="folderuserfieldsa-stream-structure"></a>FolderUserFieldsA-Datenstrom Struktur

Eine FolderUserFieldsA-Datenstrom Struktur ist ein Array von FolderFieldDefinitionA-Datenstrom Strukturen, die Definitionen für alle benutzerdefinierten Felder in einem Outlook-Ordner enthalten, es sei denn, der FolderUserFieldsW-Teil der Beispiel für folderuserfields-Struktur wird außer Kraft gesetzt.
  
Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar nach einander in der folgenden angegebenen Reihenfolge:
  
- **FieldDefinitionCount**: DWORD (4 Bytes), die Anzahl der Felddefinitionen in diesem Stream. Dies ist die Anzahl der Elemente im **FieldDefinitions** -Array.
    
- **FieldDefinitions**: ein Array von FolderFieldDefinitionA-Stream-Strukturen. Die Anzahl dieses Arrays ist gleich dem **FieldDefinitionCount** -Datenelement.
    
Sofern diese FolderUserFieldsA nicht durch den FolderUserFieldsW-Teil der Beispiel für folderuserfields-Struktur überschrieben wird, muss das **FieldDefinitions** -Array "NULL-terminiert" werden, indem das allgemeine Feld des FolderFieldDefinitionA-Elements mit dem Common. FieldType-Feld gleich ist. zu ftNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>FolderUserFieldsW-Datenstrom Struktur

Eine FolderUserFieldsW-Datenstrom Struktur ist ein Array von FolderFieldDefinitionW-Datenstrom Strukturen, die Definitionen für alle benutzerdefinierten Felder in einem Outlook-Ordner enthalten.
  
Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar nach einander in der folgenden angegebenen Reihenfolge:
  
- **FieldDefinitionCount**: DWORD (4 Bytes), die Anzahl der Felddefinitionen in diesem Stream. Dies ist die Anzahl der Elemente im **FieldDefinitions** -Array.
    
- **FieldDefinitions**: ein Array von FolderFieldDefinitionW-Stream-Strukturen. Die Anzahl dieses Arrays ist gleich dem **FieldDefinitionCount** -Datenelement.
    
Das **FieldDefinitions** -Array muss "null-terminated" sein, indem das gemeinsame. FieldType-Feld des letzten FolderFieldDefinitionW-Elements ftNull entspricht.
  
## <a name="folderfielddefinitiona-stream-structure"></a>FolderFieldDefinitionA-Datenstrom Struktur

Eine FolderFieldDefinitionA-Datenstrom Struktur enthält eine Definition eines benutzerdefinierten Felds mit dem in ANSI gespeicherten Feldnamen.
  
Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar nach einander in der folgenden angegebenen Reihenfolge:
  
- **FieldType**: FldType (4 Bytes), der Typ dieses Felds.
    
- **FieldNameLength**: Word (2 Bytes), die Anzahl der Elemente im **FieldName** -Array.
    
- **FieldName**: ein Array von Char. Dies ist die ANSI-CP_ACP-Codepage-Darstellung des Feldnamens. Die Anzahl dieses Arrays ist gleich **FieldNameLength**. Der Feldname muss die Einschränkungen des Parameters Name erfüllen, wie in der [UserProperties. Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) -Methode angegeben. 
    
   > [!NOTE]
   > Aus Gründen der Kompatibilität mit Legacyversionen kann Outlook möglicherweise einige **FieldName** -Werte verarbeiten, die diese Einschränkungen nicht erfüllen, aber solche Fälle werden in diesem Thema nicht behandelt. 
  
- **Common**: eine FolderFieldDefinitionCommon-Datenstrom Struktur.
    
## <a name="folderfielddefinitionw-stream-structure"></a>FolderFieldDefinitionW-Datenstrom Struktur

Eine FolderFieldDefinitionW-Datenstrom Struktur enthält eine Definition eines benutzerdefinierten Felds mit dem in Unicode gespeicherten Feldnamen.
  
Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar nach einander in der folgenden angegebenen Reihenfolge:
  
- **FieldType**: FldType (4 Bytes), der Typ dieses Felds.
    
- **FieldNameLength**: Word (2 Bytes), die Anzahl der Elemente im **FieldName** -Array.
    
- **FieldName**: ein Array von Typ WCHAR. Dies ist die Unicode (UTF-16)-Darstellung des Feldnamens. Die Anzahl dieses Arrays ist gleich **FieldNameLength**. Der Feldname muss die Einschränkungen des Parameters Name erfüllen, wie in der [UserProperties. Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) -Methode angegeben. 
    
   > [!NOTE]
   > Aus Gründen der Legacy Kompatibilität kann Outlook möglicherweise einige FieldName **** -Werte verarbeiten, die diese Einschränkungen nicht erfüllen, aber solche Fälle werden in diesem Thema nicht behandelt. 
  
- **Common**: eine FolderFieldDefinitionCommon-Datenstrom Struktur.
    
## <a name="fldtype-enumeration"></a>FldType-aufZählung

**FldType** -Enumerationswerte sind in der folgenden Tabelle aufgeführt. 
  
|Name|Wert|Bedeutung|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |Dieser Feldtyp wird verwendet, um ein Array von Felddefinitionen mit NULL zu beenden.  <br/> |
|ftString  <br/> |0x1  <br/> |Text  <br/> |
|ftInteger  <br/> |0x3  <br/> |Ganze Zahl  <br/> |
|ftTime  <br/> |0x5  <br/> |Datum/Uhrzeit  <br/> |
|ftBoolean  <br/> |0x6  <br/> |Ja/Nein  <br/> |
|ftDuration  <br/> |0x7  <br/> |Dauer  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Schlüsselwörter  <br/> |
|ftFloat  <br/> |0xC  <br/> |Zahl oder Prozent  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Währung  <br/> |
|ftCalc  <br/> |0x12  <br/> |Formel  <br/> |
|ftSwitch  <br/> |0x13  <br/> |Kombination aus Typ, der nur das erste nicht leere Feld anzeigt, das nachfolgende ignoriert.  <br/> |
|ftConcat  <br/> |0x17  <br/> |Kombination von Typ-Join-Feldern und Textfragmenten miteinander.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>FolderFieldDefinitionCommon-Datenstrom Struktur

Eine FolderFieldDefinitionCommon-streamstruktur enthält die Daten einer benutzerdefinierten Felddefinition, die sowohl für eine FolderFieldDefinitionA als auch für eine FolderFieldDefinitionW gilt.
  
Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar nach einander in der folgenden angegebenen Reihenfolge:
  
- **PropSetGuid**: GUID (16 Bytes), die Eigenschaftensatz-GUID des entsprechenden MAPI-Eigenschaftsnamens des Folder-Felds. Der Wert dieses Felds muss PS_PUBLIC_STRINGS sein, es sei denn, der Feldtyp ist **ftNone** , und in diesem Fall muss der Wert dieses Felds GUID_NULL entsprechen. 
    
   > [!NOTE]
   > Aus Gründen der Kompatibilität mit Legacyversionen kann Outlook möglicherweise einige **PropSetGuid** -Werte verarbeiten, die diese Einschränkung nicht erfüllen, aber solche Fälle werden in diesem Thema nicht behandelt. 
  
- **fcapm**: DWORD (4 Bytes), eine Kombination aus null oder mehr Flags die Werte, die und Bedeutungen in der folgenden Tabelle aufgeführt sind. Flags mit demselben Wert haben Bedeutungen, die vom Typ des Felds abhängig sind, also FldType-Wert.
    
    |FlagName|Wert|Bedeutung|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |Das Feld kann bearbeitet werden.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |Das Feld ist sortierbar.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |Das Feld ist Gruppierungs basiert.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |Das Feld kann mehrere Textzeilen enthalten.  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |Dieses Feld vom Typ ftFloat ist ein Prozentfeld.  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |Dieses Feld vom Typ ftTime ist ein Datum-nur-Zeitfeld.  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |Für dieses Feld vom Typ ftInteger ist keine Einheit im Anzeigeformat zulässig; zum Beispiel solche Formate wie "Computer-640 K..." sind nicht zulässig.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |Das Feld kann im Element bearbeitet werden: Dies ist speziell für benutzerdefinierte Formulare.  <br/> |
   
- **dwString**: DWORD (4 Bytes). Sehen Sie sich die erste folgende Notiz an.
    
- **dwBitmap**: DWORD (4 Bytes). Sehen Sie sich die erste folgende Notiz an.
    
- **dwDisplay**: DWORD (4 Bytes). Sehen Sie sich die erste folgende Notiz an.
    
- **iFmt**: int (4 Bytes). Für die Feldtypen, die das "Format:"-Kombinationsfeld in den Dialogfeldern "neues Feld", "Feld bearbeiten" und "Feldeigenschaften" aufweisen, ist der 0-basierte Index des in diesem Kombinationsfeld ausgewählten Formats. Für die Feldtypen ohne dieses Kombinationsfeld muss es sich um 0 handeln. Der Wert des Felds zusammen mit dem Feldtyp bestimmt die Werte der Felder **dwString**, **dwBitmap**und **dwDisplay** eindeutig, indem Sie die erste folgende Notiz lesen.
    
- **wszFormulaLength**: Word (2 Bytes), die Anzahl der Elemente im **wszFormulaLength** -Array.
    
- **wszFormulaLength**: ein Array von Typ WCHAR. Dies ist die Unicode (UTF-16)-Darstellung der Formel Zeichenfolge des Felds im Standardformat. Die Beschreibung der Standard-und Benutzeroberflächen Formate der Formel eines Felds finden Sie im zweiten folgenden Hinweis. Die Anzahl dieses Arrays ist gleich **wszFormulaLength**. Die Formel Zeichenfolge muss eine leere Zeichenfolge sein, es sei denn, der Feldtyp ist **ftCalc**, **ftSwitch** oder **ftConcat**.
    
> [!NOTE]
> Obwohl die Werte von **dwString**, **dwBitmap**und **dwDisplay** basierend auf dem **FldType** -Wert und dem **iFmt** -Wert, die redundant sind, eindeutig bestimmt werden, sind ihre korrekten Werte weiterhin für die korrekte Verarbeitung der Felddefinition durch Outlook. Es gibt keine einfache Beschreibung des Algorithmus, der diese Bestimmung ausführt. 
> 
> Um herauszufinden, welche **dwString**-, **DwBitmap**-und **DwDisplay** -Werte einem bestimmten **FldType** -Wert und **iFmt** -Wert entsprechen, führen Sie einen Test durch, indem Sie ein benutzerdefiniertes Feld dieses Typs erstellen und dieses Format auswählen. untersuchen Sie im Kombinationsfeld **Format** den resultierenden **Beispiel für folderuserfields** -Datenstrom, den Outlook für dieses benutzerdefinierte Feld erstellt. 
  
Die Formel des Felds im Benutzeroberflächenformat wird im Textfeld **Formel** der Felder **Neues Feld**, Feld **Bearbeiten**und **Feldeigenschaften** für das Feld User-Defined bearbeitet. Der Algorithmus zum Konvertieren einer Formel vom Benutzeroberflächenformat in das Standardformat hängt vom Feldtyp ab, wie im folgenden beschrieben: 
- Bei Feldern der Typen **ftCalc** und **ftSwitch**wird das Standardformat für integrierte Felder, deren MAPI-Eigenschaften keine Eigenschaften der Art MNID\_-Zeichenfolge sind, durch Ersetzen von Feld Namen Fragmenten abgerufen, d. `[<field_name>]` mit Fragmenten `[_<field_dispid_decimal>]`. 

  Wenn beispielsweise das Benutzeroberflächenformat einer Formel für ein Feld der typFormel, **** also **ftCalc**, mit der Office-Benutzeroberflächensprache Englisch ist, ist `[Business Phone] & [My custom field]`, wobei `My custom field` es sich um den Namen eines benutzerdefinierten Felds handelt, wäre das Standardformat einer solchen Formel `[_14856] & [My custom field]`.

- Für Felder vom Typ **ftConcat**wird das Standardformat durch Ausführen der folgenden Schritte abgerufen:

  1. AbSchneiden von führenden und nachgestellten Leerzeichen 
  2. Analysieren Sie die Formel in eine Sequenz von Fragmenten der folgenden beiden Arten: 
     - Ein Feldname in eckigen Klammern, also `[<field_name>]`. 
     - Eine Teilzeichenfolge, die keine eckigen Klammern enthält.   
      Stellen Sie sicher, dass in der Sequenz keine zwei Fragmente der zweiten Art benachbart sind. Wenn die Formel nicht auf diese Weise analysiert werden kann, wird Sie als ungültig betrachtet. 
  3. Führen Sie dieselbe Ersetzung für Fragmente der ersten Art wie für die Felder **ftCalc** und **ftSwitch** aus. 
  4. Escapen Sie für jedes Fragment der zweiten Art alle doppelten Anführungszeichen ("" "), sofern vorhanden, mit zwei aufeinander folgenden doppelten Anführungszeichen, und setzen Sie es in doppelte Anführungsstriche. 
  5. Fügen Sie ein kaufmännisches`&`und-Zeichen () zwischen jedem Paar benachbarter Fragmente ein.
 
  Verwenden Sie beispielsweise die Office-Benutzeroberflächensprache Englisch, wenn das Benutzeroberflächenformat einer Formel für ein Feld vom Typ **ftConcat** ist `text1 [Business Phone] "text2" [My custom field]`, wobei `My custom field` es sich um den Namen eines benutzerdefinierten Felds handelt, wäre das Standardformat für eine solche Formel `""text1" & [_14856] & """text2""" & [My custom field]"`. 
  
## <a name="see-also"></a>Siehe auch

- [Beispiel für folderuserfields-Stream-Beispiel](folderuserfields-stream-sample.md)
- [Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)

