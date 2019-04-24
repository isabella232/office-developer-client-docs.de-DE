---
title: DataRecordset-Element (DataRecordSets_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.
ms.openlocfilehash: e2baaeed38318f35d4bd4ce4269f71b6304b148f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360368"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>DataRecordset-Element (DataRecordSets_Type complexType) (' Visio XML ')

Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Enthält alle dataRecordset-Elemente im Dokument. ****  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[OData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Enthält XML, das dem klassischen ADO-XML-Schema für ein ADO-Recordset-Objekt entspricht und die Daten im Datenrecordset beschreibt.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Definiert eine Regel, mit der eine Spalte im über **** geordnetEn DataRecordset-Element mit einem Shape-Datenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion in der Benutzeroberfläche verglichen wird.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Definiert, wie eine Datenspalte im Fenster **externe Daten** auf der Visio-Benutzeroberfläche angezeigt wird, und qualifiziert die Daten in der Spalte durch Definieren des Datentyps und der Formatierung.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Enthält alle **DataColumn** -Elemente in einem Datenrecordset.  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifiziert eine oder mehrere Primärschlüsselspalten im Datenrecordset.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Gibt eine Zeile im Datenrecordset an, die mit einem Shape verknüpft ist, das nach der Aktualisierung des Datenrecordsets in Konflikt steht.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Ordnet eine Datensatzgruppe-Zeile einem Shape zu.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Prüfsumme  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Ein von Visio generierter Prüfsummenwert und basierend auf Datensatzgruppen Eigenschaften. Legen Sie diesen attirbute auf 0 fest. Visio berechnet diesen Wert zur Laufzeit neu.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Befehl  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Befehlszeichenfolge, die zum Abfragen von Daten aus der Datenquelle verwendet wird.  <br/> |Werte des XSD: String-Typs.  <br/> |
|ConnectionID  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die Verbindungs-ID für das **** zugeordnete DataConnection-Objekt. Ist für XML-Datenquellen nicht vorhanden.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die ID des Datenrecordsets, die innerhalb des Dokuments eindeutig ist.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Name  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Der Anzeigename (oder "Friendly") des Datenrecordsets.  <br/> |Werte des XSD: String-Typs.  <br/> |
|NextRowID  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die nächste verfügbare Visio-Zeilen-ID.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Optionen  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Optionen, die auf das Datenrecordset angewendet werden sollen. Mögliche Werte können eine beliebige Kombination aus einer oder mehreren der in der folgenden Tabelle dargestellten sein.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|RefreshInterval  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Wie oft (in Minuten) Visio das Datenrecordset automatisch aktualisiert. Dieser Wert muss 1 oder größer sein.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|RefreshNoReconciliationUI  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Benutzeroberfläche für die Datenabstimmung deaktiviert werden soll. True (1), um die Benutzeroberfläche zu deaktivieren. False (0), um die Benutzeroberfläche zu aktivieren.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|RefreshOverwriteAll  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Ob Benutzer Änderungen an Shape-Datenelemente in Shapes, die mit Daten verknüpft sind, beim Aktualisieren des Datenrecordsets überschrieben werden sollen.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|ReplaceLinks  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Definiert, wie Shape-Daten Links behandelt werden, wenn Shapes kopiert oder ausgeschnitten werden. 1, um vorhandene Links im Ziel-Shape zu ersetzen. 0, um vorhandene Verknüpfungen im Ziel-Shape zu verwalten.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|RowOrder  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Reihenfolge der Zeilen im Datenrecordset als Primärschlüssel verwendet werden soll. True (1), wenn Zeilen-IDs durch Zeilenreihenfolge bestimmt werden. False (0), wenn Zeilen-IDs durch Werte in der Primärschlüsselspalte (n) des Datenrecordsets bestimmt werden.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|TimeRefreshed  <br/> |XSD: dateTime  <br/> |Optional  <br/> |Datum und Uhrzeit der letzten Aktualisierung des Datenrecordset.  <br/> |Werte des XSD: dateTime-Typs.  <br/> |
   

