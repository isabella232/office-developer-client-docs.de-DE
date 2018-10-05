---
title: Verbinden-Element (Connects_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: "\n			Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.\n"
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399319"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>Verbinden-Element (Connects_Type ComplexType) ("Visio XML")


			Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.

  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Seite # .xml, Gestaltungsvorlagen # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |XSD: String  <br/> |Optional  <br/> |Die Zelle, von der eine Verbindung stammt.  <br/> |Werte des Typs xsd: String.  <br/> |
|FromPart  <br/> |XSD: int  <br/> |Optional  <br/> |Der Teil eines Shapes, von dem eine Verbindung stammt.  <br/> |Werte des Typs xsd: int.  <br/> |
|FromSheet  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die ID des Shapes, aus denen eine Verbindung oder Verbindungen stammen.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ToCell  <br/> |XSD: String  <br/> |Optional  <br/> |Die Zelle mit der eine Verbindung hergestellt wird.  <br/> |Werte des Typs xsd: String.  <br/> |
|ToPart  <br/> |XSD: int  <br/> |Optional  <br/> |Der Teil eines Shapes, mit dem eine Verbindung hergestellt wird.  <br/> |Werte des Typs xsd: int.  <br/> |
|ToSheet  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die ID des das Shape, mit dem eine oder mehrere Verbindungen hergestellt werden.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
   

