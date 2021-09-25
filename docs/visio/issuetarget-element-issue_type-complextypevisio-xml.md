---
title: IssueTarget-Element (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Gibt abhängig vom Ziel des übergeordneten Überprüfungsproblems entweder die Seite oder die Seite und das Shape an, die dem übergeordneten Überprüfungsproblem zugeordnet sind. Wenn das Ziel des übergeordneten Überprüfungsproblems ein Dokument ist, gibt IssueTarget weder eine Seite noch ein Shape an.
ms.openlocfilehash: dd85f62e35d4940da433f365e8c586689315fa9b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574069"
---
# <a name="issuetarget-element-issue_type-complextype-visio-xml"></a>IssueTarget-Element (Issue_Type complexType) (Visio XML)

Gibt abhängig vom Ziel des übergeordneten Überprüfungsproblems entweder die Seite oder die Seite und das Shape an, die dem übergeordneten Überprüfungsproblem zugeordnet sind. Wenn das Ziel des übergeordneten Überprüfungsproblems ein Dokument ist, gibt **IssueTarget** weder eine Seite noch ein Shape an. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Problem](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Stellt ein einzelnes Überprüfungsproblem im Dokument dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Gibt den eindeutigen Bezeichner der Seite an, die dem übergeordneten Überprüfungsproblem zugeordnet ist. Wenn das Ziel das Dokument ist, kann der PageID-Wert 0xFFFFFFFF werden.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Gibt den eindeutigen Bezeichner des Shapes an, das dem übergeordneten Überprüfungsproblem zugeordnet ist. Wenn das Ziel das Dokument oder eine Seite ist, kann der ShapeID-Wert 0xFFFFFFFF werden.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

