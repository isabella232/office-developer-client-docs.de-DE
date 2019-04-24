---
title: Cell-Element (Abschnitt "Scratch") (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af17b1c5-51ee-f46f-79d0-4f33369b66f1
description: Gibt einen Arbeitsbereich zum eingeben und Testen von Formeln an, auf die von anderen Zellen verwiesen werden kann.
ms.openlocfilehash: 147cc152ec20e3e2b032b91f6387ec06a3cb1d6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339529"
---
# <a name="cell-element-scratch-section-visio-xml"></a>Cell-Element (Abschnitt "Scratch") (' Visio XML ')

Gibt einen Arbeitsbereich zum eingeben und Testen von Formeln an, auf die von anderen Zellen verwiesen werden kann.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |"Document. xml", "Masters. xml", "#. xml", "pages. xml", "page #. xml"  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Row-Element (Abschnitt "Scratch")](row-element-scratch-sectionvisio-xml.md) <br/> |[ScratchRow_Type](scratch_type-complextypevisio-xml.md) <br/> |Gibt einen Arbeitsbereich zum eingeben und Testen von Formeln an, auf die von anderen Zellen verwiesen werden kann.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf eine Seite an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehler Meldungszeichenfolge); der Wert des **V** -Attributs ist der letzte gültige Wert.  <br/> |Eine Fehlermeldungs-Zeichenfolge.  <br/> |
|F  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  ' (eine Formel) ', wenn die Formel lokal vorhanden ist  <br/>  `No Formula`Wenn die Formel lokal gelöscht oder gesperrt ist  <br/>  `Inh`Wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Stellt den Namen der ShapeSheet-Zelle dar.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise" unten.  <br/> |
|U  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar der Standardwert ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
### <a name="remarks"></a>Bemerkungen

Das **N** -Attribut dieses **Cell** -Elements muss einer einer begrenzten Menge von Werten sein, die ShapeSheet-Zellen entsprechen. In der nachstehenden Tabelle finden Sie die Werte des **N** -Attributs, die für dieses **Cell** -Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|A  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|B  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|C  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|D  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|X  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|v  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
   

