---
title: AutoLinkComparison-Element (DataRecordSet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Definiert eine Regel, die eine Spalte in der übergeordneten DataRecordset-Element mit eines Shape-Datenelements aus der letzten erfolgreichen automatische Verknüpfen Aktion auf der Benutzeroberfläche vergleicht.
ms.openlocfilehash: 38970a84676f769c36c9bdc3f8334652f7d9ec21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796423"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a>AutoLinkComparison-Element (DataRecordSet_Type ComplexType) ("Visio XML")

Definiert eine Regel, die eine Spalte in der übergeordneten **DataRecordset** -Element mit eines Shape-Datenelements aus der letzten erfolgreichen automatische Verknüpfen Aktion auf der Benutzeroberfläche vergleicht. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Recordsets.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Gibt ein Recordset-Objekt und die Datenbindung zwischen, Recordset und Shapes in Zeichnungseinheiten Seiten.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Spaltenname  <br/> |XSD: String  <br/> |erforderlich  <br/> |Ein Spaltenname in das ADO-Recordset-Objekt entspricht.  <br/> |Werte des Typs xsd: String.  <br/> |
|ContextType  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Gibt die Eigenschaften der Gruppe oder ein Shape, die für den Vergleich verwendet. Mögliche Werte sind in der folgenden Tabelle aufgeführt.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ContextTypeLabel  <br/> |XSD: String  <br/> |Optional  <br/> |Ist der Wert ContextType 2 oder 3, ist dieses Attribut erforderlich, um einen Vergleich zu definieren. ContextType = 2, ContextTypeLabel muss, werden die Form Element Beschriftung, und wenn **ContextType** = 3, ContextTypeLabel muss der lokale Zeilenname.  <br/> |Werte des Typs xsd: String.  <br/> |
   

