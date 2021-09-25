---
title: THEMEVAL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: Ruft Werte aus dem aktiven Design ab.
ms.openlocfilehash: af46d000c8a7513cf961573d20d71e28c1c66915
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597849"
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
| _"theme_value"_ <br/> |Optional  <br/> |**String** <br/> |Der Name einer Zelle in der Designdefinition, aus der ein Wert abgerufen werden soll.  <br/> |
| _default_ <br/> |Optional  <br/> |Verschiedene  <br/> |Ein Standardwert, wenn das Dokument nicht mit Design versehen ist (es gibt keine Designdefinition).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die **THEMEVAL-Funktion** keine Argumente empfängt, gibt sie den Designwert der Hostzelle zurück. Dies ist der Wert, der in der Definition des aktuellen Designs gespeichert ist. Die Hostzelle muss in der Lage sein, ein Design zu erstellen, um einen Wert zurückzugeben. Wenn die Zelle nicht designfähig ist, gibt **THEMEVAL** einen Fehler zurück. 
  
Wenn die **THEMEVAL-Funktion** ein einzelnes Argument empfängt, ruft sie den Wert aus der Designdefinition ab, die als Argument übergeben wurde. Das Argument, das für den ersten Parameter übergeben wird, muss eine ganze Zahl oder eine der genauen Zeichenfolgen sein, die in der folgenden Tabelle aufgeführt sind. 
  
Die **THEMEVAL-Funktion** kann auch eine ganze Zahl für den ersten Parameter als Wert zwischen 1 und 8 akzeptieren. Die Verwendung ganzzahliger Werte ruft eine Farbe nach Index aus dem Farbschema des Designs ab. Daher gibt der Wert "1" die Farbe "Dunkel" aus dem Design zurück, "2" gibt die Farbe "Hell", "3" die Farbe "Akzent 1" usw. zurück. 
  
Wenn die **THEMEVAL-Funktion** zwei Argumente empfängt, ruft sie den Wert aus der Designdefinition ab, die als erstes Argument übergeben wird. Wenn auf das Dokument jedoch kein Design angewendet wird, verwendet die **THEMEVAL-Funktion** den als zweites Argument angegebenen Wert. 
  
**Mögliche Argumente für den Parameter "theme_value"**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|"Dunkel"  <br/> |Ruft dunkle RGB-Farbe aus der Designdefinition ab.  <br/> |
|"Light"  <br/> |Ruft die RGB-Farbe des Lichts aus der Designdefinition ab.  <br/> |
|"BackgroundColor"  <br/> |Ruft die RGB-Hintergrundfarbe aus der Designdefinition ab.  <br/> |
|"AccentColor"  <br/> |Ruft akzent1 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"AccentColor2"  <br/> |Ruft akzent2 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"AccentColor3"  <br/> |Ruft akzent3 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"AccentColor4"  <br/> |Ruft akzent4 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"AccentColor5"  <br/> |Ruft akzent5 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"AccentColor6"  <br/> |Ruft akzent6 RGB-Farbe aus der Designdefinition ab.  <br/> |
|"LinePattern"  <br/> |Ruft den Wert der Zelle LinePattern aus der Designdefinition ab.  <br/> |
|"LineWeight"  <br/> |Ruft den Wert der Zelle LineWeight aus der Designdefinition ab.  <br/> |
|"LineColor"  <br/> |Ruft den LineColor-Zellwert aus der Designdefinition ab.  <br/> |
|"LineCap"  <br/> |Ruft den LineCap-Zellwert aus der Designdefinition ab.  <br/> |
|"LineBegin"  <br/> |Ruft den BeginArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"LineEnd"  <br/> |Ruft den EndArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"LineColorTrans"  <br/> |Ruft den Zellenwert "LineColorTrans" aus der Designdefinition ab.  <br/> |
|"LineCompoundtype"  <br/> |Ruft den CompoundType-Zellwert aus der Designdefinition ab.  <br/> |
|"LineBegin"  <br/> |Ruft den BeginArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"LineEnd"  <br/> |Ruft den EndArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"LineBeginSize"  <br/> |Ruft den BeginArrowSize-Zellwert aus der Designdefinition ab.  <br/> |
|"LineEndSize"  <br/> |Ruft den EndArrowSize-Zellwert aus der Designdefinition ab.  <br/> |
|"LineRounding"  <br/> |Ruft den Wert der Rundungszelle aus der Designdefinition ab.  <br/> |
|"ConnectorColor"  <br/> |Ruft den LineColor-Zellwert aus der Designdefinition ab.  <br/> |
|"ConnectorPattern"  <br/> |Ruft den Wert der Zelle LinePattern aus der Designdefinition ab.  <br/> |
|"ConnectorWeight"  <br/> |Ruft den Wert der Zelle LineWeight aus der Designdefinition ab.  <br/> |
|"ConnectorTransparency"  <br/> |Ruft den Zellenwert "LineColorTrans" aus der Designdefinition ab.  <br/> |
|"ConnectorRounding"  <br/> |Ruft den Wert der Rundungszelle aus der Designdefinition ab.  <br/> |
|"ConnectorBegin"  <br/> |Ruft den BeginArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"ConnectorEnd"  <br/> |Ruft den EndArrow-Zellwert aus der Designdefinition ab.  <br/> |
|"ConnectorBeginSize"  <br/> |Ruft den BeginArrowSize-Zellwert aus der Designdefinition ab.  <br/> |
|"ConnectorEndSize"  <br/> |Ruft den EndArrowSize-Zellwert aus der Designdefinition ab.  <br/> |
|"FillColor"  <br/> |Ruft den FillForegnd-Zellwert aus der Designdefinition ab.  <br/> |
|"FillColor2"  <br/> |Ruft den FillBkgnd-Zellwert aus der Designdefinition ab.  <br/> |
|"FillTransparency"  <br/> |Ruft den FillForegndTrans-Zellwert aus der Designdefinition ab.  <br/> |
|"FillPattern"  <br/> |Ruft den FillPattern-Zellwert aus der Designdefinition ab.  <br/> |
|"LineGradientEnabled"  <br/> |Ruft den Wert der Zelle "LineGradientEnabled" aus der Designdefinition ab.  <br/> |
|"LineGradientDir"  <br/> |Ruft den Wert der Zelle "LineGradientDir" aus der Designdefinition ab.  <br/> |
|"LineGradientAngle"  <br/> |Ruft den Wert der Zelle "LineGradientAngle" aus der Designdefinition ab.  <br/> |
|"FillGradientEnabled"  <br/> |Ruft den FillGradientEnabled-Zellwert aus der Designdefinition ab.  <br/> |
|"FillGradientDir"  <br/> |Ruft den FillGradientDir-Zellwert aus der Designdefinition ab.  <br/> |
|"FillGradientAngle"  <br/> |Ruft den FillGradientAngle-Zellwert aus der Designdefinition ab.  <br/> |
|"RotateGradientWithShape"  <br/> |Ruft den Zellwert RotateGradientWithShape aus der Designdefinition ab.  <br/> |
|"UseGroupGradient"  <br/> |Ruft den UseGroupGradient-Zellwert aus der Designdefinition ab.  <br/> |
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
|"BevelTopWidth"  <br/> |Ruft den Wert der Zelle "BevelTopWidth" aus der Designdefinition ab.  <br/> |
|"BevelTopHeight"  <br/> |Ruft den BevelTopHeight-Zellwert aus der Designdefinition ab.  <br/> |
|"BevelMaterial"  <br/> |Ruft den BevelMaterialType-Zellwert aus der Designdefinition ab.  <br/> |
|"BevelLighting"  <br/> |Ruft den BevelLightingType-Zellwert aus der Designdefinition ab.  <br/> |
|"BevelLightingAngle"  <br/> |Ruft den BevelLightingAngle-Zellwert aus der Designdefinition ab.  <br/> |
|"BevelContourColor"  <br/> |Ruft den Wert der Zelle "BevelContourColor" aus der Designdefinition ab.  <br/> |
|"BevelContourSize"  <br/> |Ruft den BevelContourSize-Zellwert aus der Designdefinition ab.  <br/> |
|"ReflectionBlur"  <br/> |Ruft den Wert der ReflectionBlur-Zelle aus der Designdefinition ab.  <br/> |
|"ReflectionDist"  <br/> |Ruft den Wert der ReflectionDist-Zelle aus der Designdefinition ab.  <br/> |
|"ReflectionSize"  <br/> |Ruft den Wert der ReflectionSize-Zelle aus der Designdefinition ab.  <br/> |
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
|"LatinFont"  <br/> |Ruft den Zellenwert Font aus der Designdefinition ab.  <br/> |
|"TextColor"  <br/> |Ruft den Zellwert Color aus der Designdefinition ab.  <br/> |
|"TextStyle"  <br/> |Ruft den Wert der Zelle Character.Style aus der Designdefinition ab.  <br/> |
|"ComplexFont"  <br/> |Ruft den ComplexScriptFont-Zellwert aus der Designdefinition ab.  <br/> |
|"AsianFont"  <br/> |Ruft den AsianFont-Zellwert aus der Designdefinition ab.  <br/> |
|"FillStop[x]Color"  <br/> |Ruft den Zellwert "Color" in Zeile  *x*  aus der Designdefinition ab.  <br/> |
|"FillStop[x]Transparency"  <br/> |Ruft den ColorTrans-Zellwert in Zeile  *x*  aus der Designdefinition ab.  <br/> |
|"FillStop[x]Position"  <br/> |Ruft den Wert der Zelle Position in Zeile  *x*  aus der Designdefinition ab.  <br/> |
|"LineStop[x]Color"  <br/> |Ruft den Zellwert "Color" in Zeile  *x*  aus der Designdefinition ab.  <br/> |
|"LineStop[x]Transparency"  <br/> |Ruft den ColorTrans-Zellwert in Zeile  *x*  aus der Designdefinition ab.  <br/> |
|"LineStop[x]Position"  <br/> |Ruft den Wert der Zelle Position in Zeile  *x*  aus der Designdefinition ab.  <br/> |
   
## <a name="example"></a>Beispiel

 `THEMEVAL("5")`
  
Gibt die Farbe "Akzent 3" aus der Designdefinition zurück.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Gibt den Wert der Zelle "LineWeight" aus der Designdefinition zurück. Wenn auf die Form, die diese Funktion enthält, kein Design angewendet wurde, gibt die Funktion "0,7 pt." zurück.
  

