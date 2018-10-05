---
title: PageSheet-Element (Page_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Gibt die Eigenschaften des Zeichnungsfensters Zeichenblatt zugeordnet.
ms.openlocfilehash: 8b60795c02717e4b752c09af19fa932f87924d1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395133"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a>PageSheet-Element (Page_Type ComplexType) ("Visio XML")

Gibt die Eigenschaften des Zeichnungsfensters Zeichenblatt zugeordnet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Pages.Xml  <br/> |
   
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
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die eine Seite im Dokument zu definieren.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets von der Füllung Formatierung geerbt. Es muss der Wert des **ID** -Attributs einen **StyleSheet_Type** in der Zeichnung zugeordnet werden.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets von der linienformatierung geerbt. Es muss der Wert des **ID** -Attributs einen **StyleSheet_Type** in der Zeichnung zugeordnet werden.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets aus dem Text-Formatierung erben. Es muss der Wert des **ID** -Attributs einen **StyleSheet_Type** in der Zeichnung zugeordnet werden.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |XSD: String  <br/> |Optional  <br/> |Die eindeutige ID des Elements in seinem übergeordneten Element.  <br/> |Werte des Typs xsd: String.  <br/> |
   

