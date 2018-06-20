---
title: PageSheet-Element (Master_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Gibt die Eigenschaften des Zeichenblatts das Master-Shape zugeordnet.
ms.openlocfilehash: ab20cfe4561cd5fd0eeb6edad0b3a608428b0e8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797631"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a>PageSheet-Element (Master_Type ComplexType) ("Visio XML")

Gibt die Eigenschaften des Zeichenblatts das Master-Shape zugeordnet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Masters.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Gibt ein Master-Shape in einer Zeichnung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets von der Füllung Formatierung geerbt. Es muss der Wert des **ID** -Attributs einen **StyleSheet_Type** in der Zeichnung zugeordnet werden.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets von der linienformatierung geerbt. Es muss der Wert des **ID** -Attributs einen **StyleSheet_Type** in der Zeichnung zugeordnet werden.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets aus dem Text-Formatierung erben. Es muss der Wert des **ID** -Attributs einen **StyleSheet_Type** in der Zeichnung zugeordnet werden.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |XSD: String  <br/> |Optional  <br/> |Die eindeutige ID des Elements in seinem übergeordneten Element.  <br/> |Werte des Typs xsd: String.  <br/> |
   

