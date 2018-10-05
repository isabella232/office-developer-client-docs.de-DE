---
title: ProtectMasters-Element (DocumentSettings_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Gibt an, ob der Benutzer erstellen, bearbeiten oder Löschen von master-Shapes verhindert wird. Der Benutzer kann neue Shapes aus einem master-Shape, unabhängig von dieser Einstellung weiterhin erstellen.
ms.openlocfilehash: 2730fa3aa3f9f4f7529d6b939e48d3533e31e1f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386446"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a>ProtectMasters-Element (DocumentSettings_Type ComplexType) ("Visio XML")

Gibt an, ob der Benutzer erstellen, bearbeiten oder Löschen von master-Shapes verhindert wird. Der Benutzer kann neue Shapes aus einem master-Shape, unabhängig von dieser Einstellung weiterhin erstellen. 
  
Der Bereich der möglichen Werte für dieses Element ist "0" oder "1". Der Wert "0" gibt an, dass Benutzer erstellen, bearbeiten oder Löschen von master-Shapes können. Der Wert "1" gibt an, dass Benutzer erstellen, bearbeiten oder Löschen von master-Shapes ist nicht möglich.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die dokumenteinstellungen angeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

Keine.
  

