---
title: PageSheet-Element (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Gibt die Eigenschaften des Zeichenblatts an, das dem Zeichenblatt zugeordnet ist.
ms.openlocfilehash: 2f49d152a0fcb30e3f5aea98cdc251d3b65b8f69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540623"
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die eine Seite im Dokument definieren.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets an, von dem die Füllformatierung erben werden soll. Dies muss der  Wert des ID-Attributs sein, das einem StyleSheet_Type **in** der Zeichnung zugeordnet ist.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets an, von dem zeilenformatiert werden soll. Dies muss der  Wert des ID-Attributs sein, das einem StyleSheet_Type **in** der Zeichnung zugeordnet ist.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt die ID des Stylesheets an, von dem die Textformatierung erben werden soll. Dies muss der  Wert des ID-Attributs sein, das einem StyleSheet_Type **in** der Zeichnung zugeordnet ist.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |Optional  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

