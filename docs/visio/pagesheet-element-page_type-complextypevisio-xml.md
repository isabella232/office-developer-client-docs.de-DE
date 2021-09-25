---
title: PageSheet-Element (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Gibt die Eigenschaften des Zeichenblatts an, das dem Zeichenblatt zugeordnet ist.
ms.openlocfilehash: 26ab066a8539a1c464afb3eebedf59c2f1a54afa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554236"
---
# <a name="pagesheet-element-page_type-complextype-visio-xml"></a>PageSheet-Element (Page_Type complexType) (Visio XML)

Gibt die Eigenschaften des Zeichenblatts an, das dem Zeichenblatt zugeordnet ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |pages.xml  <br/> |
   
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
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die eine Seite im Dokument definieren.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets an, von dem die Füllformatierung geerbt werden soll. Dies MUSS der Wert des **ID-Attributs** sein, das einem **StyleSheet_Type** in der Zeichnung zugeordnet ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets an, von dem die Zeilenformatierung geerbt werden soll. Dies MUSS der Wert des **ID-Attributs** sein, das einem **StyleSheet_Type** in der Zeichnung zugeordnet ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets an, von dem die Textformatierung geerbt werden soll. Dies MUSS der Wert des **ID-Attributs** sein, das einem **StyleSheet_Type** in der Zeichnung zugeordnet ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |Optional  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

