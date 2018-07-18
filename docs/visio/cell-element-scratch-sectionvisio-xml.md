---
title: Zellenelement (Abschnitt "Scratch") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af17b1c5-51ee-f46f-79d0-4f33369b66f1
description: Gibt eine arbeitsumgebung für die Eingabe und Testen von Formeln, die auf die von anderen Zellen verwiesen werden können.
ms.openlocfilehash: c8917a8d4bcf26789f631238e6a9547e9ca2d59c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796609"
---
# <a name="cell-element-scratch-section-visio-xml"></a>Zellenelement (Abschnitt "Scratch") ("Visio XML")

Gibt eine arbeitsumgebung für die Eingabe und Testen von Formeln, die auf die von anderen Zellen verwiesen werden können.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.XML, masters.xml, Master-Shape # .xml, pages.xml, Seite # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Zeilenelement (Scratch-Abschnitt)](row-element-scratch-sectionvisio-xml.md) <br/> |[ScratchRow_Type](scratch_type-complextypevisio-xml.md) <br/> |Gibt eine arbeitsumgebung für die Eingabe und Testen von Formeln, die auf die von anderen Zellen verwiesen werden können.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf eine Seite.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt an, dass die Formel einen Fehler zurückgibt. Der Wert von **E** ist der aktuelle Wert (Zeichenfolge mit einer Fehlermeldung); der Wert des Attributs **V** ist der letzte gültige Wert.  <br/> |Zeichenfolge mit einer Fehlermeldung.  <br/> |
|F  <br/> |XSD: String  <br/> |Optional  <br/> | Formel für das Element darstellt. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  "(einige Formel)" Wenn die Formel lokal vorhanden ist.  <br/>  `No Formula`Wenn die Formel lokal gelöscht oder blockiert ist.  <br/>  `Inh`Wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |XSD: String  <br/> |erforderlich  <br/> |Der Name der ShapeSheet-Zelle darstellt.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Siehe Abschnitt "Hinweise".  <br/> |
|U  <br/> |XSD: String  <br/> |Optional  <br/> |Stellt eine Einheit der Messung der Standardwert ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |XSD: String  <br/> |Optional  <br/> |Den Wert der Zelle darstellt.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
### <a name="remarks"></a>Bemerkungen

Das **N** -Attribut dieses Elements **Zelle** muss eine der eine begrenzte Auswahl von Werten sein, die ShapeSheet-Zellen entsprechen. Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für diese **Zelle** Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|A  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|B  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|C  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|D  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|X  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|v  <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
   

