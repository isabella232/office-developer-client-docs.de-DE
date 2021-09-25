---
title: DataColumn-Element (DataColumns_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Definiert, wie eine Datenspalte im Fenster "Externe Daten" auf der benutzeroberfläche Visio angezeigt wird, und qualifiziert die Daten in der Spalte durch Definieren des Datentyps und der Formatierung.
ms.openlocfilehash: d218762be73b4bebcfbb500d2c1cb9519179b394
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582862"
---
# <a name="datacolumn-element-datacolumns_type-complextype-visio-xml"></a>DataColumn-Element (DataColumns_Type complexType) (Visio XML)

Definiert, wie eine Datenspalte im Fenster **"Externe Daten"** auf der benutzeroberfläche Visio angezeigt wird, und qualifiziert die Daten in der Spalte durch Definieren des Datentyps und der Formatierung. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Enthält alle **DataColumn-Elemente** in einem Datenrecordset.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Kalender  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Kalender-ID der Datenspalte.  <br/> |Werte des Typs "xsd:unsignedShort".  <br/> |
|ColumnNameID  <br/> |xsd:string  <br/> |erforderlich  <br/> |Externer Name der Datenspalte. Wird in den Überschriften im Fenster **"Externe Daten"** und in Beschriftungen in Datengrafiken angezeigt.  <br/> |Werte des Typs "xsd:string".  <br/> |
|Währung  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Währungs-ID der Datenspalte.  <br/> |Werte des Typs "xsd:unsignedShort".  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Typ der Daten in der Datenspalte.  <br/> |Werte des Typs "xsd:unsignedShort".  <br/> |
|Degree  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt den Grad (Potenz) der Einheiten an, z. B. quadratisch oder würfelt. Der Standardwert (Attribut ist nicht vorhanden) ist 1.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Definiert die Anzeigeposition der Datenspalte im Fenster **"Externe Daten",** von der linken Spalte (0) bis zur rechten Spalte (größter Wert).  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Breite der Datenspalte im Fenster **"Externe Daten".**  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Hyperlink  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Datenspalte einen Hyperlink in einem Shape erstellt, wenn das Shape mit Daten verknüpft ist.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|Beschriftung  <br/> |xsd:string  <br/> |erforderlich  <br/> |Beschriftung der Datenspalte.  <br/> |Werte des Typs "xsd:string".  <br/> |
|Langid  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die Sprach-ID der Datenspalte.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Zugeordnet  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Spalte im Fenster **"Externe Daten"** angezeigt wird. True (1), damit die Spalte sichtbar ist; False (0), damit die Spalte nicht sichtbar ist. Der Standardwert (Attribut fehlt) ist, dass die Spalte sichtbar ist.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|Name  <br/> |xsd:string  <br/> |Erforderlich  <br/> |Interner Name der Datenspalte. Wird als Zeilenname für das Shape-Datenelement (benutzerdefinierte Eigenschaft) verwendet, das einem Shape hinzugefügt wird, wenn das Shape mit einer Datenzeile verknüpft ist.  <br/> |Werte des Typs "xsd:string".  <br/> |
|OrigLabel  <br/> |xsd:string  <br/> |Optional  <br/> |Spaltenbeschriftung, die von der zugrunde liegenden ADO-Schnittstelle an Visio zurückgegeben wird.  <br/> |Werte des Typs "xsd:string".  <br/> |
|Unittype  <br/> |xsd:string  <br/> |Optional  <br/> |Einheitentyp der Daten in der Datenspalte.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

