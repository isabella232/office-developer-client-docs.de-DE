---
title: Connect-Element (Connects_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346508"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>Connect-Element (Connects_Type complexType) (' Visio XML ')

Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Page #. XML, Master #. XML  <br/> |
   
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
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Zelle, von der eine Verbindung stammt.  <br/> |Werte des XSD: String-Typs.  <br/> |
|FromPart  <br/> |XSD: int  <br/> |Optional  <br/> |Der Teil eines Shapes, von dem eine Verbindung stammt.  <br/> |Werte des XSD: int-Typs.  <br/> |
|FromSheet  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die ID der Form, aus der eine Verbindung oder Verbindungen entstehen.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ToCell  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Zelle, in der eine Verbindung hergestellt wird.  <br/> |Werte des XSD: String-Typs.  <br/> |
|ToPart  <br/> |XSD: int  <br/> |Optional  <br/> |Der Teil eines Shapes, mit dem eine Verbindung hergestellt wird.  <br/> |Werte des XSD: int-Typs.  <br/> |
|ToSheet  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die ID der Form, zu der eine oder mehrere Verbindungen hergestellt werden.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

