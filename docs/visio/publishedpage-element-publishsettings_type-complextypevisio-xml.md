---
title: PublishedPage-Element (PublishSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Gibt an, ob ein Zeichenblatt im Browser mit Visio Diensten in Microsoft SharePoint Server 2013 angezeigt werden kann.
ms.openlocfilehash: df1beb45c6709cac8aa96525b7e068b337d8c791
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565933"
---
# <a name="publishedpage-element-publishsettings_type-complextype-visio-xml"></a>PublishedPage-Element (PublishSettings_Type complexType) (Visio XML)

Gibt an, ob ein Zeichenblatt im Browser mit Visio Diensten in Microsoft SharePoint Server 2013 angezeigt werden kann.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[PublishedPage_Type](publishedpage_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[PublishSettings](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |Gibt die Einstellungen an, die verwendet werden, wenn das Diagramm mit Visio Services geöffnet wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Der Bezeichner eines Zeichenblatts.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

