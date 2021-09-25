---
title: Verbinden-Element (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
ms.openlocfilehash: 933a58a4afece3798e419f1a483b00f0d823961a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560011"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a>Verbinden-Element (Connects_Type complexType) (Visio XML)

Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Enthält ein **Verbinden-Element** für jede Verbindung zwischen zwei Formen in einer Zeichnung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd:string  <br/> |Optional  <br/> |Die Zelle, aus der eine Verbindung stammt.  <br/> |Werte des Typs "xsd:string".  <br/> |
|FromPart  <br/> |xsd:int  <br/> |Optional  <br/> |Der Teil eines Shapes, aus dem eine Verbindung stammt.  <br/> |Werte des Typs "xsd:int".  <br/> |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Die ID des Shapes, aus dem eine Verbindung oder Verbindungen stammen.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ToCell  <br/> |xsd:string  <br/> |Optional  <br/> |Die Zelle, mit der eine Verbindung hergestellt wird.  <br/> |Werte des Typs "xsd:string".  <br/> |
|ToPart  <br/> |xsd:int  <br/> |Optional  <br/> |Der Teil eines Shapes, mit dem eine Verbindung hergestellt wird.  <br/> |Werte des Typs "xsd:Int".  <br/> |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die ID des Shapes, mit dem eine oder mehrere Verbindungen hergestellt werden.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

