---
title: THEMEVAL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: Ruft Werte aus dem aktiven Design ab.
ms.openlocfilehash: ba95b8a920174ee44c0349d7227258d3ee8a843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415754"
---
# <a name="themeval-function"></a>THEMEVAL-Funktion

Ruft Werte aus dem aktiven Design ab. 
  
## <a name="version-information"></a>Informationen zur Version

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **THEMEVAL**([ _"theme_value"_][, _Standard_]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _"theme_value"_ <br/> |Optional  <br/> |**String** <br/> |Der Name einer Zelle in der Designdefinition, aus der ein Wert erhalten werden soll.  <br/> |
| _default_ <br/> |Optional.  <br/> |Verschiedene  <br/> |Ein Standardwert, wenn das Dokument nicht designiert ist (es gibt keine Designdefinition).  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn die **THEMEVAL-Funktion** keine Argumente erhält, gibt sie den Designwert der Hostzelle zurück. Dies ist der Wert, der in der Definition des aktuellen Designs gespeichert ist. Die Hostzelle muss in der Lage sein, ein Bestimmtes zu erhalten, um einen Wert zurücksennen zu können. Wenn die Zelle nicht designfähig ist, gibt **THEMEVAL** einen Fehler zurück. 
  
Wenn die **THEMEVAL-Funktion** ein einzelnes Argument empfängt, ruft sie den Wert aus der designdefinition ab, die als Argument übergeben wurde. Das für den ersten Parameter übergebene Argument muss eine ganze Zahl oder eine der genauen Zeichenfolgen sein, die in der folgenden Tabelle aufgeführt sind. 
  
Die **THEMEVAL-Funktion** kann auch eine ganze Zahl für den ersten Parameter als Wert zwischen 1 und 8 akzeptieren. Mithilfe ganzzahliger Werte wird eine Farbe nach Index aus dem Farbschema des Designs abgerufen. Daher gibt der Wert "1" die Farbe "Dunkel" aus dem Design zurück, "2" gibt die Farbe "Light" zurück, "3" gibt die Farbe "Akzent 1" usw. zurück. 
  
Wenn die **THEMEVAL-Funktion** zwei Argumente empfängt, ruft sie den Wert aus der Designdefinition ab, die als erstes Argument übergeben wurde. Wenn dem Dokument jedoch kein Design angewendet wurde, verwendet die **THEMEVAL-Funktion** den als zweites Argument angegebenen Wert. 
  
**Mögliche Argumente für den Parameter "theme_value"**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|"Dunkel"  <br/> |Ruft dunkle RGB-Farbe aus der Designdefinition ab.  <br/> |
|"Light"  <br/> |Ruft light RGB-Farbe aus der Designdefinition ab.  <br/> |
|"BackgroundColor"  <br/> |Ruft Hintergrund-RGB-Farbe aus der Designdefinition ab.  <br/> |
|"AccentColor"  <br/> |Ruft Accent1 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"AccentColor2"  <br/> |Ruft Accent2 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"AccentColor3"  <br/> |Ruft Accent3 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"AccentColor4"  <br/> |Ruft Accent4 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"AccentColor5"  <br/> |Ruft Accent5 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"AccentColor6"  <br/> |Ruft Accent6 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"LinePattern"  <br/> |Ruft den LinePattern-Zellwert aus der Designdefinition ab.  <br/> |
|"LineWeight"  <br/> |Ruft den LineWeight-Zellwert aus der Designdefinition ab.  <br/> |
|"LineColor"  <br/> |Ruft den LineColor-Zellwert aus der Designdefinition ab.  <br/> |
|"LineCap"  <br/> |Ruft den LineCap-Zellwert aus der Designdefinition ab.  <br/> |
|"LineBegin"  <br/> |Ruft den BeginArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"LineEnd"  <br/> |Ruft den EndArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"LineColorTrans"  <br/> |Ruft den LineColorTrans-Zellwert aus der Designdefinition ab.  <br/> |
|"LineCompoundtype"  <br/> |Ruft den CompoundType-Zellwert aus der Designdefinition ab.  <br/> |
|"LineBegin"  <br/> |Ruft den BeginArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"LineEnd"  <br/> |Ruft den EndArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"LineBeginSize"  <br/> |Ruft den BeginArrowSize-Zellwert aus der Designdefinition ab.  <br/> |
|"LineEndSize"  <br/> |Ruft den EndArrowSize-Zellwert aus der Designdefinition ab.  <br/> |
|"LineRounding"  <br/> |Ruft den Wert der Rounding-Zelle aus der Designdefinition ab.  <br/> |
|"ConnectorColor"  <br/> |Ruft den LineColor-Zellwert aus der Designdefinition ab.  <br/> |
|"ConnectorPattern"  <br/> |Ruft den LinePattern-Zellwert aus der Designdefinition ab.  <br/> |
|"ConnectorWeight"  <br/> |Ruft den LineWeight-Zellwert aus der Designdefinition ab.  <br/> |
|"ConnectorTransparency"  <br/> |Ruft den LineColorTrans-Zellwert aus der Designdefinition ab.  <br/> |
|"ConnectorRounding"  <br/> |Ruft den Wert der Rounding-Zelle aus der Designdefinition ab.  <br/> |
|"ConnectorBegin"  <br/> |Ruft den BeginArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"ConnectorEnd"  <br/> |Ruft den EndArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"ConnectorBeginSize"  <br/> |Ruft den BeginArrowSize-Zellwert aus der Designdefinition ab.  <br/> |
|"ConnectorEndSize"  <br/> |Ruft den EndArrowSize-Zellwert aus der Designdefinition ab.  <br/> |
|"FillColor"  <br/> |Ruft den FillForegnd-Zellwert aus der Designdefinition ab.  <br/> |
|"FillColor2"  <br/> |Ruft den FillBkgnd-Zellwert aus der Designdefinition ab.  <br/> |
|"FillTransparency"  <br/> |Ruft den FillForegndTrans-Zellwert aus der Designdefinition ab.  <br/> |
|"FillPattern"  <br/> |Ruft den FillPattern-Zellwert aus der Designdefinition ab.  <br/> |
|"LineGradientEnabled"  <br/> |Ruft lineGradientEnabled-Zellwert aus der Designdefinition ab.  <br/> |
|"LineGradientDir"  <br/> |Ruft den LineGradientDir-Zellwert aus der Designdefinition ab.  <br/> |
|"LineGradientAngle"  <br/> |Ruft den LineGradientAngle-Zellwert aus der Designdefinition ab.  <br/> |
|"FillGradientEnabled"  <br/> |Ruft fillGradientEnabled-Zellwert aus der Designdefinition ab.  <br/> |
|"FillGradientDir"  <br/> |Ruft den FillGradientDir-Zellwert aus der Designdefinition ab.  <br/> |
|"FillGradientAngle"  <br/> |Ruft den FillGradientAngle-Zellwert aus der Designdefinition ab.  <br/> |
|"RotateGradientWithShape"  <br/> |Ruft den Zellenwert RotateGradientWithShape aus der Designdefinition ab.  <br/> |
|"UseGroupGradient"  <br/> |Ruft useGroupGradient-Zellwert aus der Designdefinition ab.  <br/> |
|"ShadowType"  <br/> |Ruft den ShapeShdwType-Zellwert aus der Designdefinition ab.  <br/> |
|"ShadowColor"  <br/> |Ruft den ShdwColor-Zellwert aus der Designdefinition ab.  <br/> |
|"ShadowTransparency"  <br/> |Ruft den ShdwColorTrans-Zellwert aus der Designdefinition ab.  <br/> |
|"ShadowMagnification"  <br/> |Ruft den ShapeShdwScaleFactor-Zellwert aus der Designdefinition ab.  <br/> |
|"ShadowBlur"  <br/> |Ruft den ShapeShdwBlur-Zellwert aus der Designdefinition ab.  <br/> |
|"ShadowXOffset"  <br/> |Ruft den ShapeShdwOffsetX-Zellwert aus der Designdefinition ab.  <br/> |
|"ShadowYOffset"  <br/> |Ruft den ShapeShdwOffsetY-Zellwert aus der Designdefinition ab.  <br/> |
|"ShadowDirection"  <br/> |Ruft den ShapeShdwObliqueAngle-Zellwert aus der Designdefinition ab.  <br/> |
|"ShadowPattern"  <br/> |Ruft den ShdwPattern-Zellwert aus der Designdefinition ab.  <br/> |
|"BevelTopType"  <br/> |Ruft den BevelTopType-Zellwert aus der Designdefinition ab.  <br/> |
|"BevelTopWidth"  <br/> |Ruft den BevelTopWidth-Zellwert aus der Designdefinition ab.  <br/> |
|"BevelTopHeight"  <br/> |Ruft den BevelTopHeight-Zellwert aus der Designdefinition ab.  <br/> |
|"BevelMaterial"  <br/> |Ruft den BevelMaterialType-Zellwert aus der Designdefinition ab.  <br/> |
|"BevelLighting"  <br/> |Ruft den BevelLightingType-Zellwert aus der Designdefinition ab.  <br/> |
|"BevelLightingAngle"  <br/> |Ruft den Zellwert "BevelLightingAngle" aus der Designdefinition ab.  <br/> |
|"BevelContourColor"  <br/> |Ruft den BevelContourColor-Zellwert aus der Designdefinition ab.  <br/> |
|"BevelContourSize"  <br/> |Ruft den BevelContourSize-Zellwert aus der Designdefinition ab.  <br/> |
|"ReflectionBlur"  <br/> |Ruft den ReflectionBlur-Zellwert aus der Designdefinition ab.  <br/> |
|"ReflectionDist"  <br/> |Ruft den ReflectionDist-Zellwert aus der Designdefinition ab.  <br/> |
|"ReflectionSize"  <br/> |Ruft den ReflectionSize-Zellwert aus der Designdefinition ab.  <br/> |
|"ReflectionTrans"  <br/> |Ruft den ReflectionTrans-Zellwert aus der Designdefinition ab.  <br/> |
|"SoftEdgesSize"  <br/> |Ruft den SoftEdgesSize-Zellwert aus der Designdefinition ab.  <br/> |
|"GlowSize"  <br/> |Ruft den GlowSize-Zellwert aus der Designdefinition ab.  <br/> |
|"GlowColor"  <br/> |Ruft den GlowColor-Zellwert aus der Designdefinition ab.  <br/> |
|"GlowTransparency"  <br/> |Ruft den GlowColorTrans-Zellwert aus der Designdefinition ab.  <br/> |
|"SketchAmount"  <br/> |Ruft den SketchAmount-Zellwert aus der Designdefinition ab.  <br/> |
|"SketchEnabled"  <br/> |Ruft den SketchEnabled-Zellwert aus der Designdefinition ab.  <br/> |
|"SketchFillChange"  <br/> |Ruft den SketchFillChange-Zellwert aus der Designdefinition ab.  <br/> |
|"SketchLineChange"  <br/> |Ruft den SketchLineChange-Zellwert aus der Designdefinition ab.  <br/> |
|"SketchLineWeight"  <br/> |Ruft den SketchLineWeight-Zellwert aus der Designdefinition ab.  <br/> |
|"LatinFont"  <br/> |Ruft den Font-Zellwert aus der Designdefinition ab.  <br/> |
|"TextColor"  <br/> |Ruft den Wert der Color-Zelle aus der Designdefinition ab.  <br/> |
|"TextStyle"  <br/> |Ruft den Character.Style-Zellwert aus der Designdefinition ab.  <br/> |
|"ComplexFont"  <br/> |Ruft den ComplexScriptFont-Zellwert aus der Designdefinition ab.  <br/> |
|"AsianFont"  <br/> |Ruft den Wert der AsianFont-Zelle aus der Designdefinition ab.  <br/> |
|"FillStop[x]Color"  <br/> |Ruft den Farbzellenwert in Zeile  *x*  aus der Designdefinition ab.  <br/> |
|"FillStop[x]Transparency"  <br/> |Ruft den ColorTrans-Zellwert in Zeile  *x*  aus der Designdefinition ab.  <br/> |
|"FillStop[x]Position"  <br/> |Ruft den Zellenwert Position in Zeile  *x*  aus der Designdefinition ab.  <br/> |
|"LineStop[x]Color"  <br/> |Ruft den Farbzellenwert in Zeile  *x*  aus der Designdefinition ab.  <br/> |
|"LineStop[x]Transparency"  <br/> |Ruft den ColorTrans-Zellwert in Zeile  *x*  aus der Designdefinition ab.  <br/> |
|"LineStop[x]Position"  <br/> |Ruft den Zellenwert Position in Zeile  *x*  aus der Designdefinition ab.  <br/> |
   
## <a name="example"></a>Beispiel

 `THEMEVAL("5")`
  
Gibt die Farbe "Akzent 3" aus der Designdefinition zurück.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Gibt den Wert der Zelle "LineWeight" aus der Designdefinition zurück. Wenn auf das Shape, das diese Funktion enthält, kein Design angewendet wurde, gibt die Funktion "0,7 Pt." zurück.
  

