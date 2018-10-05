---
title: Seitenelement (Pages_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Enthält Elemente, die eine Seite im Dokument zu definieren.
ms.openlocfilehash: 800e4ab2c6446ab298747f0492800000bb44cca3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398010"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>Seitenelement (Pages_Type ComplexType) ("Visio XML")

Enthält Elemente, die eine Seite im Dokument zu definieren.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Pages.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |**Elemente des für das Dokument** enthält.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die das Seitenblatt für **ein Seitenelement** definieren.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Hintergrund  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Ein Kennzeichen gibt an, ob die Seite ein Hintergrundblatt ist.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|BackPage  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die ID des Hintergrundblatt auf dieser Seite.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements in seinem übergeordneten Element.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der Name des Benutzers angepasst wurde.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|IsCustomNameU  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der universelle Name durch den Benutzer angepasst wurde.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|Name  <br/> |XSD: String  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des Typs xsd: String.  <br/> |
|ReviewerID  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die ID des Bearbeiters Markupüberlagerung zugeordnet.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |XSD: Double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite, die eine neue Ansicht (Fenster) geht davon aus, wenn es zunächst geöffnet wird.  <br/> |Werte des Typs xsd: Double.  <br/> |
|ViewCenterY  <br/> |XSD: Double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite, die eine neue Ansicht (Fenster) geht davon aus, wenn es zunächst geöffnet wird.  <br/> |Werte des Typs xsd: Double.  <br/> |
|ViewScale  <br/> |XSD: Double  <br/> |Optional  <br/> |Der Standardwert Vergrößerungsfaktor verwendet, wenn eine neue Ansicht (Fenster) auf der Seite geöffnet wird. Beispiel: 1 = 100 %; 1,5 = 150 % und So weiter.  <br/> |Werte des Typs xsd: Double.  <br/> |
   

