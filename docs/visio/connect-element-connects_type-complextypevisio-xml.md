---
title: Connect-Element (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541995"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>Connect-Element (Connects_Type complexType) (Visio XML)

Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Seite #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Formen in einer Zeichnung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Zelle, aus der eine Verbindung stammt.  <br/> |Werte des Typs XSD: String.  <br/> |
|FromPart  <br/> |XSD: int  <br/> |Optional  <br/> |Der Teil eines Shapes, von dem eine Verbindung stammt.  <br/> |Werte des Typs XSD: int.  <br/> |
|FromSheet  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die ID der Form, aus der eine Verbindung oder Verbindungen stammen.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ToCell  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Zelle, in der eine Verbindung hergestellt wird.  <br/> |Werte des Typs XSD: String.  <br/> |
|ToPart  <br/> |XSD: int  <br/> |Optional  <br/> |Der Teil eines Shapes, mit dem eine Verbindung hergestellt wird.  <br/> |Werte des Typs XSD: int.  <br/> |
|ToSheet  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die ID der Form, in die mindestens eine Verbindung hergestellt wird.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

