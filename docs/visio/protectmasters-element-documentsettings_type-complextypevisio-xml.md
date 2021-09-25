---
title: ProtectMasters-Element (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Gibt an, ob verhindert wird, dass der Benutzer Master-Shapes erstellt, bearbeitet oder löscht. Der Benutzer kann unabhängig von dieser Einstellung weiterhin neue Shapes aus einem Master-Shape erstellen.
ms.openlocfilehash: e0919e57bbdda5782548636793ba1ebb3744d788
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623173"
---
# <a name="protectmasters-element-documentsettings_type-complextype-visio-xml"></a>ProtectMasters-Element (DocumentSettings_Type complexType) (Visio XML)

Gibt an, ob verhindert wird, dass der Benutzer Master-Shapes erstellt, bearbeitet oder löscht. Der Benutzer kann unabhängig von dieser Einstellung weiterhin neue Shapes aus einem Master-Shape erstellen. 
  
Der Bereich der möglichen Werte für dieses Element ist entweder '0' oder '1'. Der Wert "0" gibt an, dass Benutzer Master-Shapes erstellen, bearbeiten oder löschen können. Der Wert "1" gibt an, dass Benutzer keine Master-Shapes erstellen, bearbeiten oder löschen können.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die Dokumenteinstellungen angeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

Keine.
  

