---
title: DataRecordSet-Element (DataRecordSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.
ms.openlocfilehash: 41390699788b9606bf72473c17683c32b5a3744e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608270"
---
# <a name="datarecordset-element-datarecordsets_type-complextype-visio-xml"></a>DataRecordSet-Element (DataRecordSets_Type complexType) (Visio XML)

Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Enthält alle **DataRecordset-Elemente** im Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Enthält XML, das dem klassischen ADO-XML-Schema für ein ADO-Recordset entspricht und die Daten im Datenrecordset beschreibt.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Definiert eine Regel, die eine Spalte im übergeordneten **DataRecordset-Element** mit einem Shape-Datenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion vergleicht, die auf der Benutzeroberfläche ausgeführt wurde.  <br/> |
|[Datacolumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Definiert, wie eine Datenspalte im Fenster **"Externe Daten"** auf der benutzeroberfläche Visio angezeigt wird, und qualifiziert die Daten in der Spalte durch Definieren des Datentyps und der Formatierung.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Enthält alle **DataColumn-Elemente** in einem Datenrecordset.  <br/> |
|[Primarykey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifiziert eine oder mehrere Primärschlüsselspalten im Datenrecordset.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Gibt eine Zeile im Datenrecordset an, die mit einem Shape verknüpft ist, das nach dem Aktualisieren des Datenrecordsets in Konflikt steht.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Karten einer Datensatzzeile zu einem Shape.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Prüfsumme  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Ein Prüfsummenwert, der von Visio generiert wird und auf Datenrecordseteigenschaften basiert. Legen Sie diese Einstellung auf 0 fest; Visio berechnet diesen Wert zur Laufzeit neu.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Befehl  <br/> |xsd:string  <br/> |Optional  <br/> |Die Befehlszeichenfolge, die zum Abfragen von Daten aus der Datenquelle verwendet wird.  <br/> |Werte des Typs "xsd:string".  <br/> |
|ConnectionID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die Verbindungs-ID für das zugeordnete **DataConnection-Objekt.** Ist für XML-Datenquellen nicht vorhanden.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die im Dokument eindeutige Datenrecordset-ID.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Anzeigename (oder "Anzeigename") des Datenrecordsets.  <br/> |Werte des Typs "xsd:string".  <br/> |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die nächste verfügbare Visio Zeilen-ID.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Optionen  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Optionen, die auf das Datenrecordset angewendet werden können. Mögliche Werte können eine beliebige Kombination aus einer oder mehreren der in der folgenden Tabelle dargestellten Werte sein.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|RefreshInterval  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Wie oft (in Minuten) Visio das Datenrecordset automatisch aktualisiert. Dieser Wert muss 1 oder größer sein.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|RefreshNoReconciliationUI  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Benutzeroberfläche für die Datenüberleitung deaktiviert werden soll. True (1), um die Benutzeroberfläche zu deaktivieren. False (0), um die Benutzeroberfläche zu aktivieren.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|RefreshOverwriteAll  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob Benutzeränderungen an Shape-Datenelementen in Shapes überschrieben werden sollen, die mit Daten verknüpft sind, wenn das Datenrecordset aktualisiert wird.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Definiert, wie Shape-Datenverknüpfungen behandelt werden, wenn Shapes kopiert oder ausgeschnitten werden. 1, um vorhandene Verknüpfungen im Ziel-Shape zu ersetzen. 0, um vorhandene Verknüpfungen im Ziel-Shape beizubehalten.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|RowOrder  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Reihenfolge der Zeilen im Datenrecordset als Primärschlüssel verwendet werden soll. True (1), wenn Zeilen-IDs durch die Zeilenreihenfolge bestimmt werden. False (0), wenn Zeilen-IDs durch Werte in den Primärschlüsselspalten des Datenrecordsets bestimmt werden.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|TimeRefreshed  <br/> |xsd:dateTime  <br/> |Optional  <br/> |Datum und Uhrzeit der letzten Aktualisierung des Datenrecordsets.  <br/> |Werte des Typs "xsd:dateTime".  <br/> |
   

