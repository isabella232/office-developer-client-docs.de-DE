---
title: Cell-Element (Abschnitt "Fill Gradient") (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d085f83a-f77b-9bf9-07dc-4561b83e288c
description: Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füll Verlauf.
ms.openlocfilehash: 3c4cdf1f60f68748fd2500b2dec0b5a5ad553ff5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356098"
---
# <a name="cell-element-fill-gradient-section-visio-xml"></a>Cell-Element (Abschnitt "Fill Gradient") (' Visio XML ')

Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füll Verlauf.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML, Master #. XML, Page #. XML  <br/> |
   
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
|[Row-Element (FillGradient-Abschnitt)](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[FillGradientRow_Type](fillgradientrow_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füll Verlauf.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehler Meldungszeichenfolge); der Wert des **V** -Attributs ist der letzte gültige Wert.  <br/> |Eine Fehlermeldungs-Zeichenfolge.  <br/> |
|F  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  ' (eine Formel) ', wenn die Formel lokal vorhanden ist  <br/>  `No Formula`Wenn die Formel lokal gelöscht oder gesperrt ist  <br/>  `Inh`Wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Stellt den Namen der ShapeSheet-Zelle dar.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise" unten.  <br/> |
|U  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar der Standardwert ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **N** -Attribut dieses **Cell** -Elements muss einer einer begrenzten Menge von Werten sein, die ShapeSheet-Zellen entsprechen. In der nachstehenden Tabelle finden Sie die Werte des **N** -Attributs, die für dieses **Cell** -Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|GradientStopColor  <br/> |Der Farbwert des Farbverlaufsstopps. Dieser Wert kann als Indexzahl einer Farbe in der dokumentpalette oder unter Verwendung der **RGB**-, **THEMEVAL**-oder **gsl** -Funktionen ausgedrückt werden.  <br/> |[Verlaufs Unterbrechungs Zeile (Abschnitt "Füll Verlauf")](gradient-stop-row-fill-gradient-section.md) <br/> |
|GradientStopColorTrans  <br/> |Der Transparenzgrad der Farbverlaufs Unterbrechung als Prozentsatz.  <br/> |[Verlaufs Unterbrechungs Zeile (Abschnitt "Füll Verlauf")](gradient-stop-row-fill-gradient-section.md) <br/> |
|GradientStopPosition  <br/> |Die Position des Farbverlaufsstopps entlang der Richtung des Linien Verlaufs, als Prozentsatz vom Ursprungspunkt des Farbverlaufs bis zur äußeren Kante des Farbverlaufs.  <br/> |[Verlaufs Unterbrechungs Zeile (Abschnitt "Füll Verlauf")](gradient-stop-row-fill-gradient-section.md) <br/> |
   

