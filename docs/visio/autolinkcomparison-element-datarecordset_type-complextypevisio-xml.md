---
title: AutoLinkComparison-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Definiert eine Regel, die eine Spalte im übergeordneten DataRecordset-Element mit einem Shape-Datenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion vergleicht, die auf der Benutzeroberfläche ausgeführt wurde.
ms.openlocfilehash: b8b2ea090946968de8fbc5a9e265a8e41a084e85
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598829"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a>AutoLinkComparison-Element (DataRecordSet_Type complexType) (Visio XML)

Definiert eine Regel, die eine Spalte im übergeordneten **DataRecordset-Element** mit einem Shape-Datenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion vergleicht, die auf der Benutzeroberfläche ausgeführt wurde. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Gibt ein Recordset und die Datenbindung zwischen diesem Recordset und Shapes in Zeichenblättern an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |xsd:string  <br/> |Erforderlich  <br/> |Entspricht einem Spaltennamen im ADO-Recordset.  <br/> |Werte des Typs "xsd:string".  <br/> |
|Contexttype  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Gibt die Eigenschaften der Gruppe oder Form an, die für den Vergleich verwendet werden soll. Mögliche Werte sind in der folgenden Tabelle dargestellt.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ContextTypeLabel  <br/> |xsd:string  <br/> |Optional  <br/> |Wenn der ContextType-Wert 2 oder 3 ist, ist dieses Attribut erforderlich, um einen Vergleich zu definieren. Für ContextType = 2 muss ContextTypeLabel die Shape-Datenelementbeschriftung sein, und wenn **ContextType** = 3 ist, muss ContextTypeLabel der lokale Zeilenname sein.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

