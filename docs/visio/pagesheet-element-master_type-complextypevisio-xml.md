---
title: PageSheet-Element (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Gibt die Eigenschaften des Zeichenblatts an, das dem Master zugeordnet ist.
ms.openlocfilehash: ed9bca13e8af1f37861892282596e7d5546c7c52
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608123"
---
# <a name="pagesheet-element-master_type-complextype-visio-xml"></a>PageSheet-Element (Master_Type complexType) (Visio XML)

Gibt die Eigenschaften des Zeichenblatts an, das dem Master zugeordnet ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |masters.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Gibt ein Master-Shape in einer Zeichnung an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |gibt die ID des Stylesheets an, von dem die Füllformatierung geerbt werden soll. Dies MUSS der Wert des **ID-Attributs** sein, das einem **StyleSheet_Type** in der Zeichnung zugeordnet ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets an, von dem die Zeilenformatierung geerbt werden soll. Dies MUSS der Wert des **ID-Attributs** sein, das einem **StyleSheet_Type** in der Zeichnung zugeordnet ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets an, von dem die Textformatierung geerbt werden soll. Dies MUSS der Wert des **ID-Attributs** sein, das einem **StyleSheet_Type** in der Zeichnung zugeordnet ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |Optional  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

