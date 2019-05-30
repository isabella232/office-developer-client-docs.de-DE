---
title: DataRecordset-Element (DataRecordSets_Type complexType) (Visio XML)
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
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>DataRecordset-Element (DataRecordSets_Type complexType) (Visio XML)

Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Enthält alle DataRecordset-Elemente im Dokument. ****  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Odata](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Enthält XML, das dem klassischen ADO-XML-Schema für ein ADO-Recordset-Objekt entspricht und die Daten im Datenrecordset beschreibt.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Definiert eine Regel, die eine Spalte im übergeordneten DataRecordset-Element mit einem Shape-Datenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion vergleicht, die auf der Benutzeroberfläche ausgeführt wurde. ****  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Definiert, wie eine Datenspalte im Fenster **externe Daten** auf der Visio-Benutzeroberfläche angezeigt wird, und qualifiziert die Daten in der Spalte, indem Sie den Datentyp und die Formatierung definiert.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Enthält alle **DataColumn** -Elemente in einem Datenrecordset.  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Gibt eine oder mehrere Primärschlüsselspalten im Datenrecordset an.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Gibt eine Zeile im Datenrecordset an, die mit einem Shape verknüpft ist, das nach dem Aktualisieren des Daten-Recordsets in Konflikt steht.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Ordnet einer Form eine Data-Recordset-Zeile zu.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Prüfsumme  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Ein von Visio generierter Prüfsummenwert und basierend auf Data-Recordset-Eigenschaften. Legen Sie diese attirbute auf 0 fest; Visio berechnet diesen Wert zur Laufzeit neu.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Befehl  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Befehlszeichenfolge, die zum Abfragen von Daten aus der Datenquelle verwendet wird.  <br/> |Werte des Typs XSD: String.  <br/> |
|ConnectionID  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die Verbindungs-ID für das **** zugeordnete DataConnection-Objekt. Ist für XML-Datenquellen nicht vorhanden.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die Daten-Recordset-ID, die innerhalb des Dokuments eindeutig ist.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Name  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Der Anzeigename (oder "Friendly") des Datenrecordset.  <br/> |Werte des Typs XSD: String.  <br/> |
|NextRowID  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die nächste verfügbare Visio-Zeilen-ID.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Optionen  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Optionen, die auf das Datenrecordset angewendet werden sollen. Mögliche Werte können eine beliebige Kombination aus einer oder mehreren der in der folgenden Tabelle dargestellten sein.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|RefreshInterval  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Wie oft (in Minuten) wird das Datenrecordset von Visio automatisch aktualisiert. Dieser Wert muss 1 oder größer sein.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|RefreshNoReconciliationUI  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Benutzeroberfläche für die Datenabstimmung deaktiviert werden soll. True (1), um die Benutzeroberfläche (UI) zu deaktivieren. False (0), um die Benutzeroberfläche zu aktivieren.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|RefreshOverwriteAll  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob Benutzer Änderungen an Shape-Datenelementen in Shapes überschrieben werden, die mit Daten verknüpft sind, wenn das Datenrecordset aktualisiert wird.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|ReplaceLinks  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Definiert, wie Shape-Data-Verknüpfungen behandelt werden, wenn Shapes kopiert oder ausgeschnitten werden. 1, um vorhandene Verknüpfungen im Ziel-Shape zu ersetzen. 0, um vorhandene Verknüpfungen im Ziel-Shape beizubehalten.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|RowOrder  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Reihenfolge der Zeilen im Datenrecordset als Primärschlüssel verwendet werden soll. True (1), wenn Zeilen-IDs durch Zeilenreihenfolge bestimmt werden. False (0), wenn Zeilen-IDs durch Werte in der Primärschlüsselspalte (n) des Datenrecordset bestimmt werden.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|TimeRefreshed  <br/> |XSD: DateTime  <br/> |Optional  <br/> |Datum und Uhrzeit der letzten Aktualisierung des Daten-Recordset-Objekts.  <br/> |Werte des Typs XSD: DateTime.  <br/> |
   

