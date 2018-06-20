---
title: DataRecordSet-Element (DataRecordSets_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.
ms.openlocfilehash: 157213476214c736367b724dd6ca944060c53467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796793"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>DataRecordSet-Element (DataRecordSets_Type ComplexType) ("Visio XML")

Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Recordsets.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Enthält alle **DataRecordset** -Elemente im Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Enthält XML, die dem klassischen ADO XML-Schema für ein ADO-Recordset entspricht und die die Daten im Datenrecordset beschreibt.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Definiert eine Regel, die eine Spalte in der übergeordneten **DataRecordset** -Element mit eines Shape-Datenelements aus der letzten erfolgreichen automatische Verknüpfen Aktion auf der Benutzeroberfläche vergleicht.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Definiert, wie eine Datenspalte im Fenster **Externe Daten** in der Visio-Benutzeroberfläche angezeigt und berechtigt ist die Daten in der Spalte Datentyp zu definieren und die Formatierung.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Enthält alle **DataColumn** -Elemente in einem Datenrecordset.  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Eine oder mehrere Primärschlüsselspalten im Datenrecordset identifiziert.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Gibt eine Zeile im Datenrecordset verknüpft ein Shape, das nach der Datenrecordsets ein Konflikt vorliegt.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Ordnet eine Datenrecordset Zeile eines Shapes.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Prüfsumme  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Ein Prüfsummenwert von Visio erstellt werden, und basierend auf Datenrecordset Eigenschaften. Diese Attirbute auf 0 festgelegt; Visio wird dieser Wert zur Laufzeit neu berechnet.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Befehl  <br/> |XSD: String  <br/> |Optional  <br/> |Die Befehlszeichenfolge zum Abfragen von Daten aus der Datenquelle.  <br/> |Werte des Typs xsd: String.  <br/> |
|ConnectionID  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die Verbindungs-ID für das zugeordnete **DataConnection** -Objekt. Ist für XML-Datenquellen nicht vorhanden.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die ID des Datenrecordsets, innerhalb des Dokuments eindeutig.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Name  <br/> |XSD: String  <br/> |Optional  <br/> |Die Anzeige (oder "benutzerfreundlichen") Name des Datenrecordsets.  <br/> |Werte des Typs xsd: String.  <br/> |
|NextRowID  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die nächsten verfügbaren Visio Zeilen-ID.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Options  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Optionen für das Datenrecordset gilt. Mögliche Werte können eine beliebige Kombination von eines oder mehrere der in der folgenden Tabelle dargestellt werden.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|RefreshInterval  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Visio aktualisiert das Datenrecordset wie häufig (in Minuten) automatisch aus. Dieser Wert muss 1 oder größer sein.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|RefreshNoReconciliationUI  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Daten Abstimmung-Benutzeroberfläche deaktiviert werden soll. "True" (1), um die Benutzeroberfläche (UI) zu deaktivieren. False (0), um die Benutzeroberfläche zu aktivieren.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|RefreshOverwriteAll  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Ob benutzeränderungen an Shape-Datenelemente im Shapes überschrieben verknüpften Daten, wenn das Datenrecordset aktualisiert wird.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|ReplaceLinks  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Definiert, wie Shapes und Daten Links behandelt werden, wenn Shapes kopiert oder ausgeschnitten werden. 1 Ersetzen der vorhandenen Hyperlinks im Ziel-Shape. 0 zum Aufrechterhalten der vorhandenen Hyperlinks im Ziel-Shape.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|RowOrder  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Die Reihenfolge der Zeilen im Datenrecordset als Primärschlüssel verwenden sollen. "True" (1), wenn Zeilen-IDs durch Zeilenreihenfolge bestimmt werden. False (0), wenn Zeilen-IDs durch die Werte in die Primärschlüsselspalten des Datenrecordsets bestimmt werden.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|TimeRefreshed  <br/> |XSD: DateTime  <br/> |Optional  <br/> |Das Datum und die Zeit, die das Datenrecordset zuletzt aktualisiert wurde.  <br/> |Werte des Typs xsd: DateTime.  <br/> |
   

