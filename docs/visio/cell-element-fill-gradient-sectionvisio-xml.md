---
title: Cell-Element (Abschnitt "Fill Gradient") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d085f83a-f77b-9bf9-07dc-4561b83e288c
description: Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füllgradienten.
ms.openlocfilehash: 998c63d5273c39601e5b7293ae03eebbc3b467b2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539551"
---
# <a name="cell-element-fill-gradient-section-visio-xml"></a>Cell-Element (Abschnitt "Fill Gradient") (Visio XML)

Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füllgradienten.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml, Master#.xml, Seite#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Row-Element (FillGradient Section)](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[FillGradientRow_Type](fillgradientrow_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füllgradienten.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehlermeldungszeichenfolge); Der Wert  des V-Attributs ist der letzte gültige Wert.  <br/> |Eine Fehlermeldungszeichenfolge.  <br/> |
|F  <br/> |xsd:string  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  '(einige Formel)' wenn die Formel lokal vorhanden ist  <br/>  `No Formula` wenn die Formel lokal gelöscht oder blockiert wird  <br/>  `Inh` wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |xsd:string  <br/> |erforderlich  <br/> |Stellt den Namen der Zelle ShapeSheet dar.  <br/> |Der Name der Zelle ShapeSheet.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise".  <br/> |
|U  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar Die Standardeinstellung ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der Zelle ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **N-Attribut** dieses **Cell-Elements** muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen. In der folgenden Tabelle finden Sie  Informationen zu den Werten des N-Attributs, die für dieses **Cell-Element zulässig** sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|GradientStopColor  <br/> |Der Farbwert des Farbverlaufsstopps. Dieser Wert kann als Indexnummer einer Farbe in der Dokumentpalette oder mithilfe der **RGB-,** **THEMEVAL-** oder **HSL-Funktionen ausgedrückt** werden.  <br/> |[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md) <br/> |
|GradientStopColorTrans  <br/> |Die Transparenz des Farbverlaufsstopps als Prozentsatz.  <br/> |[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md) <br/> |
|GradientStopPosition  <br/> |Die Position des Gradientenstopps entlang der Richtung des Linienverlaufs, als Prozentsatz vom Ursprung des Farbverlaufs bis zum äußeren Rand des Farbverlaufs.  <br/> |[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md) <br/> |
   

