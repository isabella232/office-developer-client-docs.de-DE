---
title: Ordnerfelder-Streamstrukturen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96051bd2b62fd7c0e908a1018aac0225e44986be
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385088"
---
# <a name="folder-fields-stream-structures"></a>Ordnerfelder-Streamstrukturen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Nachricht [PidTagUserFields](pidtaguserfields-canonical-property.md) -Eigenschaft enthält einen binären Datenstrom, FolderUserFields, die die benutzerdefinierte Felddefinitionen Ordner enthält. In diesem Thema werden die Stream-Strukturen für benutzerdefinierte Felddefinitionen Ordner. 

Eine FolderUserFields Stream-Struktur besteht aus einer FolderUserFieldsA Struktur oder eine FolderUserFieldsA Struktur gefolgt von einer FolderUserFieldsW Struktur.
  
Data-Elemente in diesem Datenstrom werden gespeichert unmittelbar miteinander in der angegebenen Reihenfolge:
  
- **FolderUserFieldsAnsi**: eine FolderUserFieldsA stream Struktur.
    
- **FolderUserFieldsUnicode** (optional): eine FolderUserFieldsW stream Struktur.
    
Das Vorhandensein von FolderUserFieldsUnicode wird durch die Gesamtlänge des der FolderUserFields größer als die Länge des FolderUserFieldsAnsi erkannt.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi wird verwendet, um die Kompatibilität mit älteren, nicht-Unicode Versionen von MAPI-Clients, daher Wenn FolderUserFieldsUnicode vorhanden ist, wird der Inhalt der FolderUserFieldsAnsi ignoriert. Zur Vermeidung von möglichen Daten enthalten Verlust in ANSI-Konvertierung, beim Erstellen von eines Streams FolderUserFields immer das FolderUserFieldsW Teil. 
  
## <a name="folderuserfieldsa-stream-structure"></a>FolderUserFieldsA Stream-Struktur

Eine FolderUserFieldsA Stream-Struktur ist ein Array von FolderFieldDefinitionA Stream Strukturen, die Definitionen für alle benutzerdefinierten Felder in einem Outlook-Ordner enthalten, es sei denn, durch den FolderUserFieldsW Teil der Struktur FolderUserFields außer Kraft gesetzt.
  
Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der angegebenen Reihenfolge gespeichert:
  
- **FieldDefinitionCount**: DWORD-Wert (4 Bytes), die Anzahl der Felddefinitionen in diesen Stream. Dies ist die Anzahl der Elemente im Array **FieldDefinitions** .
    
- **FieldDefinitions**: ein Array von FolderFieldDefinitionA stream Strukturen. Die Anzahl der dieses Array ist gleich der **FieldDefinitionCount** Data-Element.
    
Sofern diese FolderUserFieldsA durch den FolderUserFieldsW Teil der Struktur FolderUserFields überschrieben wird, muss das Array **FieldDefinitions** "auf Null endende" sein, dass das letzte Element des FolderFieldDefinitionA Common.FieldType Feld gleich Um FtNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>FolderUserFieldsW Stream-Struktur

Eine FolderUserFieldsW Stream-Struktur ist ein Array von FolderFieldDefinitionW Stream Strukturen, die Definitionen für alle benutzerdefinierten Felder in einem Outlook-Ordner enthalten.
  
Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der angegebenen Reihenfolge gespeichert:
  
- **FieldDefinitionCount**: DWORD-Wert (4 Bytes), die Anzahl der Felddefinitionen in diesen Stream. Dies ist die Anzahl der Elemente im Array **FieldDefinitions** .
    
- **FieldDefinitions**: ein Array von FolderFieldDefinitionW stream Strukturen. Die Anzahl der dieses Array ist gleich der **FieldDefinitionCount** Data-Element.
    
Das Array **FieldDefinitions** muss "auf Null endende", wenn das letzte Element des FolderFieldDefinitionW Common.FieldType Feld FtNull gleich.
  
## <a name="folderfielddefinitiona-stream-structure"></a>FolderFieldDefinitionA Stream-Struktur

Eine FolderFieldDefinitionA Stream-Struktur enthält eine Definition eines benutzerdefinierten Felds mit der Name des Felds in ANSI gespeichert.
  
Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der angegebenen Reihenfolge gespeichert:
  
- **FieldType**: FldType (4 Bytes) der Typ dieses Felds.
    
- **FieldNameLength**: WORD (2 Bytes), die Anzahl der Elemente im Array **FieldName** .
    
- **FieldName**: ein Array von CHAR. Dies ist die Codepage ANSI CP_ACP Darstellung der Name des Felds. Die Anzahl der dieses Array ist gleich **FieldNameLength**. Der Name des Felds erfüllen muss, auf dem Name-Parameter in der [UserProperties.Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) -Methode gemäß die Einschränkungen. 
    
   > [!NOTE]
   > Aus Gründen der Kompatibilität mit Vorversionen Outlook möglicherweise einige **FieldName** -Werte, die diese Einschränkung nicht erfüllen, jedoch solchen Fällen fallen nicht unter in diesem Thema behandelt. 
  
- **Allgemeine**: eine FolderFieldDefinitionCommon stream Struktur.
    
## <a name="folderfielddefinitionw-stream-structure"></a>FolderFieldDefinitionW Stream-Struktur

Eine FolderFieldDefinitionW Stream-Struktur enthält eine Definition eines benutzerdefinierten Felds mit der Name des Felds im Unicode-Format gespeichert.
  
Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der angegebenen Reihenfolge gespeichert:
  
- **FieldType**: FldType (4 Bytes) der Typ dieses Felds.
    
- **FieldNameLength**: WORD (2 Bytes), die Anzahl der Elemente im Array **FieldName** .
    
- **FieldName**: ein Array von WCHAR. Dies ist der Name des Felds die Darstellung Unicode (UTF-16). Die Anzahl der dieses Array ist gleich **FieldNameLength**. Der Name des Felds erfüllen muss, auf dem Name-Parameter in der [UserProperties.Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) -Methode gemäß die Einschränkungen. 
    
   > [!NOTE]
   > Aus Gründen der Kompatibilität mit Vorversionen Outlook möglicherweise einige **FieldName** -Werte, die nicht den Eigenschaften dieser Beschränkungen verarbeiten, jedoch solchen Fällen unterliegen nicht in diesem Thema. 
  
- **Allgemeine**: eine FolderFieldDefinitionCommon stream Struktur.
    
## <a name="fldtype-enumeration"></a>FldType-Aufzählung

**FldType** Enumeration-Werte werden in der folgenden Tabelle aufgeführt. 
  
|Name|Wert|Bedeutung|
|:-----|:-----|:-----|
|ftNull  <br/> |0 x 0  <br/> |In diesem Feldtyp wird verwendet, um ein Array von Felddefinitionen Null beenden.  <br/> |
|ftString  <br/> |0 x 1  <br/> |Text  <br/> |
|ftInteger  <br/> |0 x 3  <br/> |Ganze Zahl  <br/> |
|ftTime  <br/> |0 x 5  <br/> |Datum/Uhrzeit  <br/> |
|ftBoolean  <br/> |0 x 6  <br/> |Ja/Nein  <br/> |
|ftDuration  <br/> |0 x 7  <br/> |Duration  <br/> |
|ftMultiString  <br/> |0xb  <br/> |Schlüsselwörter  <br/> |
|ftFloat  <br/> |0xC  <br/> |Zahl oder einen Prozentsatz  <br/> |
|ftCurrency  <br/> |0xE zurückgeliefert  <br/> |Währung  <br/> |
|ftCalc  <br/> |0 x 12  <br/> |Formel  <br/> |
|ftSwitch  <br/> |0 x 13  <br/> |Die Kombination des Typs das erste nicht leeren Feld - Ignorieren nachfolgender Felder angezeigt.  <br/> |
|ftConcat  <br/> |0 x 17  <br/> |Kombination von Typ Felder und Textabschnitte miteinander verknüpfen.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>FolderFieldDefinitionCommon Stream-Struktur

Eine FolderFieldDefinitionCommon Stream-Struktur enthält die Daten der Definition eines benutzerdefinierten Felds, das in eine FolderFieldDefinitionA und eine FolderFieldDefinitionW Abfragesprache ist.
  
Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der angegebenen Reihenfolge gespeichert:
  
- **PropSetGuid**: GUID (16 Byte), die Eigenschaftensatz-GUID der entsprechenden MAPI-Eigenschaftennamen im Feld Ordner. Wert des Felds muss PS_PUBLIC_STRINGS, gleich sein, es sei denn, der Feldtyp **FtNone** ist in diesem Fall der Wert des Felds GUID_NULL gleich sein muss. 
    
   > [!NOTE]
   > Aus Gründen der Kompatibilität mit Vorversionen Outlook möglicherweise einige **PropSetGuid** -Werte, die diese Einschränkung nicht erfüllen, jedoch solchen Fällen fallen nicht unter in diesem Thema behandelt. 
  
- **Fcapm**: DWORD-Wert (4 Bytes), eine Kombination aus null oder mehr Flags, die in der folgenden Tabelle werden die Werte der und Bedeutung aufgeführt. Flags mit demselben Wert haben Bedeutungen hängt von dem Feld Typ, d. h., FldType-Wert.
    
    |Namen des Kennzeichens|Wert  |Bedeutung|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |Das Feld kann bearbeitet werden.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |Das Feld ist sortierbar.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0 x 00000004  <br/> |Das Feld ist Gruppierbare.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0 x 00000100  <br/> |Das Feld kann mehrere Textzeilen enthalten.  <br/> |
    |FCAPM_PERCENT  <br/> |0 x 01000000  <br/> |In diesem Feld der der Typ FtFloat ist ein Prozentsatz-Feld.  <br/> |
    |FCAPM_DATEONLY  <br/> |0 x 01000000  <br/> |Dieses Feld von der FtTime Typ ist nur Date-Time-Feld ein.  <br/> |
    |FCAPM_UNITLESS  <br/> |0 x 01000000  <br/> |Für dieses Feld die FtInteger Typ ist keine Einheit in Anzeigeformat zulässig ist; beispielsweise Formate wie "Computer - 640 k.." sind nicht zulässig.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0 x 80000000  <br/> |Das Feld kann im Element bearbeitet werden: Dies ist insbesondere für benutzerdefinierte Formulare.  <br/> |
   
- **DwString**: DWORD-Wert (4 Bytes). Finden Sie im ersten folgenden Hinweis.
    
- **DwBitmap**: DWORD-Wert (4 Bytes). Finden Sie im ersten folgenden Hinweis.
    
- **DwDisplay**: DWORD-Wert (4 Bytes). Finden Sie im ersten folgenden Hinweis.
    
- **iFmt**: INT (4 Bytes). Für die Feldtypen, die die "Format:" Kombinationsfeld "Neues Feld", "Feld bearbeiten" und "Feldeigenschaften" dialogs, der 0-basierter Indexwert des Formats in diesem Kombinationsfeld ausgewählt. Für die Feldtypen ohne, Kombinationsfeld muss dies 0 sein. Der Wert des Feldes zusammen mit den Feldtyp können die Werte der **DwString**, **DwBitmap**, eindeutig bestimmt und **DwDisplay** Felder, finden Sie unter der ersten folgende Hinweis.
    
- **WszFormulaLength**: WORD (2 Bytes), die Anzahl der Elemente im Array **WszFormulaLength** .
    
- **WszFormulaLength**: ein Array von WCHAR. Dies ist die Darstellung Unicode (UTF-16) das Feld Formel Zeichenfolge in seinem standard-Format. Finden Sie im zweiten folgenden Hinweis für die Beschreibung des Standards und Benutzeroberflächenformate ein Feld Formel ein. Die Anzahl der dieses Array ist gleich **WszFormulaLength**. Die Formel Zeichenfolge muss eine leere Zeichenfolge sein, es sei denn, der Feldtyp **FtCalc**, **FtSwitch** oder **FtConcat**ist.
    
> [!NOTE]
> Obwohl die Werte der **DwString**, **DwBitmap**und **DwDisplay** eindeutig basierend auf der **FldType** und dem Wert der **iFmt** , die redundant sind bestimmt werden, sind die richtigen Werte weiterhin erforderlich für richtigen Verarbeitung der Felddefinition von Outlook. Es ist keine einfache Beschreibung des Algorithmus, der diese Ermittlung durchführt. 
> 
> Führen Sie daher, um herauszufinden, welche Werte **DwString**, **DwBitmap**und **DwDisplay** einer bestimmten **FldType** und dem Wert **iFmt** entsprechen, einen Test durch Erstellen eines benutzerdefinierten Felds dieses Typs und mit diesem Format ausgewählt das Kombinationsfeld **Format** vorausgesetzt, dessen Gültigkeit prüfen Sie in der den resultierenden **FolderUserFields** Stream, den für das benutzerdefinierte Feld Outlook erstellt. 
  
Das Feld Formel in seinem UI-Format wird in das Textfeld **Formel** von der **Neuen Felds**, **Feld bearbeiten**und **Feldeigenschaften** Dialogfeldern für das benutzerdefinierte Feld bearbeitet. Der Algorithmus zum Konvertieren einer Formel aus dem UI-Format in das standard-Format hängt von den Feldtyp wie im folgenden beschrieben: 
- Für die Felder der Typen **FtCalc** und **FtSwitch**, das Standardformat für integrierte Felder, die keine entsprechende MAPI-Eigenschaften sind benannte Eigenschaften für die Kind MNID\_Zeichenfolge ist, wird durch das Feld Namensfragmente, d. h. ersetzen abgerufen `[<field_name>]` mit Fragmenten `[_<field_dispid_decimal>]`. 

  Beispiel: bei einer Formel für ein Feld vom Typ **Formel**, die **FtCalc**mit der Sprache der Office-Benutzeroberfläche wird Englisch (USA), ist das UI-Format ist `[Business Phone] & [My custom field]`, wobei `My custom field` ist der Name eines benutzerdefinierten Felds wäre das Standardformat solche einer Formel `[_14856] & [My custom field]`.

- Für Felder des Typs, **FtConcat**ist das Standardformat durch Ausführen der folgenden ermittelt:

  1. Abschneiden Sie führende und nachfolgende Leerzeichen. 
  2. Analysieren Sie die Formel in einer Sequenz von Fragmenten mit den folgenden zwei Arten: 
     - Ein Feldname in eckige Klammern, d. h., `[<field_name>]`. 
     - Eine Teilzeichenfolge, die Klammern nicht enthalten.   
      Sicherstellen Sie, dass keine zwei Fragmente vom zweiten in der Reihenfolge angrenzen. Wenn die Formel auf diese Weise nicht analysiert werden kann, wird es als ungültig angesehen. 
  3. Führen Sie die gleiche Ersetzung für Fragmente der ersten Art wie für die Felder **FtCalc** und **FtSwitch** . 
  4. Für jedes Fragment vom zweiten, escape alle doppelte Anführungszeichen ("" ") Zeichen, gegebenenfalls mit zwei aufeinander folgenden Anführungszeichen Zeichen, und setzen Sie ihn in doppelte Anführungszeichen. 
  5. Fügen Sie eine Zeichenfolge kaufmännisches und-Zeichen (`&`) zwischen zwei angrenzenden Fragmente.
 
  Beispielsweise mithilfe der Office-Benutzeroberfläche Sprache Englisch (USA), wenn das Format der Benutzeroberfläche einer Formel für ein Feld vom Typ, **FtConcat** ist `text1 [Business Phone] "text2" [My custom field]`, wobei `My custom field` ist der Name eines benutzerdefinierten Felds, das Standardformat für eine solche Formel wäre `""text1" & [_14856] & """text2""" & [My custom field]"`. 
  
## <a name="see-also"></a>Siehe auch

- [Beispiel für FolderUserFields-Stream](folderuserfields-stream-sample.md)
- [Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)

