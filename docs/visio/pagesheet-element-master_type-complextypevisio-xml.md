---
title: PageSheet-Element (Master_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Gibt die Eigenschaften des Zeichenblatts an, das dem Master zugeordnet ist.
ms.openlocfilehash: 579b2b4f02c79a38842a150b8757329e19e7bb3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361124"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a>PageSheet-Element (Master_Type complexType) (' Visio XML ')

Gibt die Eigenschaften des Zeichenblatts an, das dem Master zugeordnet ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Masters. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Gibt einen Master in einer Zeichnung an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets an, von dem die Füllformatierung geerbt werden soll. Es muss der Wert des **ID-** Attributs sein, das einem **StyleSheet_Type** in der Zeichnung zugeordnet ist.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|LineStyle  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets an, von dem die Linienformatierung geerbt werden soll. Es muss der Wert des **ID-** Attributs sein, das einem **StyleSheet_Type** in der Zeichnung zugeordnet ist.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|TextStyle  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets an, von dem die Textformatierung geerbt werden soll. Es muss der Wert des **ID-** Attributs sein, das einem **StyleSheet_Type** in der Zeichnung zugeordnet ist.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|UniqueID  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des XSD: String-Typs.  <br/> |
   

