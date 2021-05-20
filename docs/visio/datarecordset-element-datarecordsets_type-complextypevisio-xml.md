---
title: DataRecordSet-Element (DataRecordSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.
ms.openlocfilehash: e478593f370968db5fe9a65329cb1928c0f7c6ea
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539677"
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Enthält alle **DataRecordset-Elemente** im Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Enthält XML, das dem klassischen ADO-XML-Schema für ein ADO-Recordset entspricht und die Daten im Daten recordset beschreibt.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Definiert eine Regel, die eine Spalte im übergeordneten **DataRecordset-Element** mit einem Shapedatenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion auf der Benutzeroberfläche vergleicht.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Definiert, wie eine Datenspalte im Fenster Externe Daten auf der benutzeroberfläche Visio angezeigt wird, und qualifiziert die Daten in der Spalte durch Definieren des Datentyps und der Formatierung.   <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Enthält alle **DataColumn-Elemente** in einem Daten recordset.  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifiziert eine oder mehrere Primärschlüsselspalten im Datendatensatz.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Gibt eine Zeile im Daten recordset an, die mit einem Shape verknüpft ist, das nach der Aktualisierung des Daten recordset in Konflikt steht.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Karten einer Daten-Recordset-Zeile zu einer Form.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Prüfsumme  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Ein Prüfsummenwert, der von Visio generiert wird und auf Datendatensatzeigenschaften basiert. Legen Sie diese attirbute auf 0; Visio berechnet diesen Wert zur Laufzeit neu.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Get-Help  <br/> |xsd:string  <br/> |Optional  <br/> |Die Befehlszeichenfolge, die zum Abfragen von Daten aus der Datenquelle verwendet wird.  <br/> |Werte des xsd:string-Typs.  <br/> |
|ConnectionID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die Verbindungs-ID für das zugeordnete **DataConnection-Objekt.** Ist für XML-Datenquellen nicht vorhanden.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die daten recordset-ID, die innerhalb des Dokuments eindeutig ist.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Anzeigename (oder der Anzeigename) des Datendatensatz.  <br/> |Werte des xsd:string-Typs.  <br/> |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die nächste verfügbare Visio Zeilen-ID.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Optionen  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Optionen, die auf das Daten recordset angewendet werden. Mögliche Werte können eine beliebige Kombination aus einer oder mehreren der in der folgenden Tabelle angezeigten Werte sein.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|RefreshInterval  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Wie oft (in Minuten) Visio das Daten recordset automatisch aktualisiert. Dieser Wert muss 1 oder größer sein.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|RefreshNoReconciliationUI  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Benutzeroberfläche für die Datenabgleich deaktiviert werden soll. True (1), um die Benutzeroberfläche zu deaktivieren. False (0), um die Benutzeroberfläche zu aktivieren.  <br/> |Werte des typs xsd:boolean.  <br/> |
|RefreshOverwriteAll  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob Benutzeränderungen an Shapedatenelementen in Shapes überschrieben werden, die mit Daten verknüpft sind, wenn das Daten recordset aktualisiert wird.  <br/> |Werte des typs xsd:boolean.  <br/> |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Definiert, wie Shape-Daten-Verknüpfungen behandelt werden, wenn Shapes kopiert oder ausgeschnitten werden. 1, um vorhandene Links in der Zielform zu ersetzen. 0, um vorhandene Links in der Zielform zu verwalten.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|RowOrder  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Reihenfolge der Zeilen im Datendatensatz als Primärschlüssel verwendet werden soll. True (1), wenn Zeilen-IDs durch die Zeilenreihenfolge bestimmt werden. False (0), wenn Zeilen-IDs durch Werte in den Primärschlüsselspalten des Daten recordset bestimmt werden.  <br/> |Werte des typs xsd:boolean.  <br/> |
|TimeRefreshed  <br/> |xsd:dateTime  <br/> |Optional  <br/> |Datum und Uhrzeit, zu der das Daten recordset zuletzt aktualisiert wurde.  <br/> |Werte des xsd:dateTime-Typs.  <br/> |
   

