---
title: THEMEVAL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: Ruft die Werte aus dem aktiven Design ab.
ms.openlocfilehash: 7bbd017c859a0a167bbd279d60af029e98421375
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798277"
---
# <a name="themeval-function"></a>THEMEVAL-Funktion

Ruft die Werte aus dem aktiven Design ab. 
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **THEMEVAL** ([ _"Theme_value"_] [, _Standard_]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _"Theme_value"_ <br/> |Optional  <br/> |**String** <br/> |Der Name einer Zelle in der Designdefinition, einen Wert abgerufen werden soll.  <br/> |
| _default_ <br/> |Optional  <br/> |Sonstige  <br/> |Ein Standardwert, wenn das Dokument nicht entsprechendes mit Design versehenes ist (es ist keine Designdefinition).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die **THEMEVAL** -Funktion keine Argumente erhält, wird den entsprechendes mit Design versehenes Wert der Zelle Host zurückgegeben. Dies ist der Wert in der Definition des aktuellen Designs gespeichert. Die Zelle Host muss mit Designs einen Wert zurückgegeben werden können; Wenn die Zelle nicht mit Designs Lage ist, gibt **THEMEVAL** einen Fehler zurück. 
  
Wenn die **THEMEVAL** -Funktion als einziges Argument empfängt, wird der Wert aus der Designdefinition als Argument übergebene abgerufen. Das Argument für den ersten Parameter übergebenen muss eine ganze Zahl oder eine der in der folgenden Tabelle aufgeführten genauen Zeichenfolgen sein. 
  
Die **THEMEVAL** -Funktion kann eine Ganzzahl für den ersten Parameter, auch als Wert zwischen 1 und 8 akzeptieren. Werte für ganze Zahl mit eine Farbe anhand des Index des Farbschemas des Designs abgerufen. Folglich wird "Dunkles" den Wert "1" aus dem Design zurück, "2" gibt die Farbe "Light", "3" gibt die Farbe "Akzent 1" usw.. 
  
Wenn die Funktion **THEMEVAL** zwei Argumente empfängt, wird der Wert abgerufen, aus der Designdefinition als erstes Argument übergeben. Allerdings weist das Dokument kein Design angewendet wird, verwendet die **THEMEVAL** -Funktion den Wert als zweites Argument angegeben. 
  
**Möglichen Argumente für den Parameter "Theme_value"**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|"Dunkel"  <br/> |Dunkles RGB-Farbe aus der Designdefinition abgerufen.  <br/> |
|"Light"  <br/> |Hell RGB-Farbe aus der Designdefinition abgerufen.  <br/> |
|"BackgroundColor"  <br/> |Hintergrund RGB-Farbe aus der Designdefinition abgerufen.  <br/> |
|"AccentColor"  <br/> |Ruft Akzent1 RGB-Farbe aus der Designdefinition.  <br/> |
|"AccentColor2"  <br/> |Ruft Accent2 RGB-Farbe aus der Designdefinition.  <br/> |
|"AccentColor3"  <br/> |Ruft Accent3 RGB-Farbe aus der Designdefinition.  <br/> |
|"AccentColor4"  <br/> |Ruft Accent4 RGB-Farbe aus der Designdefinition.  <br/> |
|"AccentColor5"  <br/> |Ruft Accent5 RGB-Farbe aus der Designdefinition.  <br/> |
|"AccentColor6"  <br/> |Ruft Accent6 RGB-Farbe aus der Designdefinition.  <br/> |
|"LinePattern"  <br/> |Zellwert LinePattern aus der Designdefinition abgerufen.  <br/> |
|"LineWeight"  <br/> |Zellwert LineWeight aus der Designdefinition abgerufen.  <br/> |
|"LineColor"  <br/> |Zellwert LineColor aus der Designdefinition abgerufen.  <br/> |
|"LineCap"  <br/> |Zellwert LineCap aus der Designdefinition abgerufen.  <br/> |
|"LineBegin"  <br/> |Zellwert BeginArrow aus der Designdefinition abgerufen.  <br/> |
|"LineEnd"  <br/> |Zellwert EndArrow aus der Designdefinition abgerufen.  <br/> |
|"LineColorTrans"  <br/> |Der Wert Zelle LineColorTrans aus der Designdefinition abgerufen.  <br/> |
|"LineCompoundtype"  <br/> |Zellwert CompoundType aus der Designdefinition abgerufen.  <br/> |
|"LineBegin"  <br/> |Zellwert BeginArrow aus der Designdefinition abgerufen.  <br/> |
|"LineEnd"  <br/> |Zellwert EndArrow aus der Designdefinition abgerufen.  <br/> |
|"LineBeginSize"  <br/> |Zellwert BeginArrowSize aus der Designdefinition abgerufen.  <br/> |
|"LineEndSize"  <br/> |Zellwert EndArrowSize aus der Designdefinition abgerufen.  <br/> |
|"LineRounding"  <br/> |Zellwert Rounding aus der Designdefinition abgerufen.  <br/> |
|"ConnectorColor"  <br/> |Zellwert LineColor aus der Designdefinition abgerufen.  <br/> |
|"ConnectorPattern"  <br/> |Zellwert LinePattern aus der Designdefinition abgerufen.  <br/> |
|"ConnectorWeight"  <br/> |Zellwert LineWeight aus der Designdefinition abgerufen.  <br/> |
|"ConnectorTransparency"  <br/> |Der Wert Zelle LineColorTrans aus der Designdefinition abgerufen.  <br/> |
|"ConnectorRounding"  <br/> |Zellwert Rounding aus der Designdefinition abgerufen.  <br/> |
|"ConnectorBegin"  <br/> |Zellwert BeginArrow aus der Designdefinition abgerufen.  <br/> |
|"ConnectorEnd"  <br/> |Zellwert EndArrow aus der Designdefinition abgerufen.  <br/> |
|"ConnectorBeginSize"  <br/> |Zellwert BeginArrowSize aus der Designdefinition abgerufen.  <br/> |
|"ConnectorEndSize"  <br/> |Zellwert EndArrowSize aus der Designdefinition abgerufen.  <br/> |
|"FillColor"  <br/> |Zellwert FillForegnd aus der Designdefinition abgerufen.  <br/> |
|"FillColor2"  <br/> |Zellwert FillBkgnd aus der Designdefinition abgerufen.  <br/> |
|"FillTransparency"  <br/> |Zellwert FillForegndTrans aus der Designdefinition abgerufen.  <br/> |
|"FillPattern"  <br/> |Zellwert FillPattern aus der Designdefinition abgerufen.  <br/> |
|"LineGradientEnabled"  <br/> |Zellwert LineGradientEnabled aus der Designdefinition abgerufen.  <br/> |
|"LineGradientDir"  <br/> |Zellwert LineGradientDir aus der Designdefinition abgerufen.  <br/> |
|"LineGradientAngle"  <br/> |Zellwert LineGradientAngle aus der Designdefinition abgerufen.  <br/> |
|"FillGradientEnabled"  <br/> |Zellwert FillGradientEnabled aus der Designdefinition abgerufen.  <br/> |
|"FillGradientDir"  <br/> |Zellwert FillGradientDir aus der Designdefinition abgerufen.  <br/> |
|"FillGradientAngle"  <br/> |Zellwert FillGradientAngle aus der Designdefinition abgerufen.  <br/> |
|"RotateGradientWithShape"  <br/> |Zellwert RotateGradientWithShape aus der Designdefinition abgerufen.  <br/> |
|"UseGroupGradient"  <br/> |Zellwert UseGroupGradient aus der Designdefinition abgerufen.  <br/> |
|"ShadowType"  <br/> |Der Wert Zelle ShapeShdwType aus der Designdefinition abgerufen.  <br/> |
|"ShadowColor"  <br/> |Zellwert ShdwColor aus der Designdefinition abgerufen.  <br/> |
|"ShadowTransparency"  <br/> |Zellwert ShdwColorTrans aus der Designdefinition abgerufen.  <br/> |
|"ShadowMagnification"  <br/> |Zellwert ShapeShdwScaleFactor aus der Designdefinition abgerufen.  <br/> |
|"ShadowBlur"  <br/> |Zellwert ShapeShdwBlur aus der Designdefinition abgerufen.  <br/> |
|"ShadowXOffset"  <br/> |Zellwert ShapeShdwOffsetX aus der Designdefinition abgerufen.  <br/> |
|"ShadowYOffset"  <br/> |Zellwert ShapeShdwOffsetY aus der Designdefinition abgerufen.  <br/> |
|"ShadowDirection"  <br/> |Zellwert ShapeShdwObliqueAngle aus der Designdefinition abgerufen.  <br/> |
|"ShadowPattern"  <br/> |Zellwert ShdwPattern aus der Designdefinition abgerufen.  <br/> |
|"BevelTopType"  <br/> |Wert der BevelTopType-Zelle aus der Designdefinition abgerufen.  <br/> |
|"BevelTopWidth"  <br/> |Zellwert BevelTopWidth aus der Designdefinition abgerufen.  <br/> |
|"BevelTopHeight"  <br/> |Zellwert BevelTopHeight aus der Designdefinition abgerufen.  <br/> |
|"BevelMaterial"  <br/> |Zellwert BevelMaterialType aus der Designdefinition abgerufen.  <br/> |
|"BevelLighting"  <br/> |Zellwert BevelLightingType aus der Designdefinition abgerufen.  <br/> |
|"BevelLightingAngle"  <br/> |Zellwert BevelLightingAngle aus der Designdefinition abgerufen.  <br/> |
|"BevelContourColor"  <br/> |Zellwert BevelContourColor aus der Designdefinition abgerufen.  <br/> |
|"BevelContourSize"  <br/> |Zellwert BevelContourSize aus der Designdefinition abgerufen.  <br/> |
|"ReflectionBlur"  <br/> |Zellwert ReflectionBlur aus der Designdefinition abgerufen.  <br/> |
|"ReflectionDist"  <br/> |Zellwert ReflectionDist aus der Designdefinition abgerufen.  <br/> |
|"ReflectionSize"  <br/> |Zellwert ReflectionSize aus der Designdefinition abgerufen.  <br/> |
|"ReflectionTrans"  <br/> |Zellwert ReflectionTrans aus der Designdefinition abgerufen.  <br/> |
|"SoftEdgesSize"  <br/> |Zellwert SoftEdgesSize aus der Designdefinition abgerufen.  <br/> |
|"GlowSize"  <br/> |Zellwert GlowSize aus der Designdefinition abgerufen.  <br/> |
|"GlowColor"  <br/> |Zellwert GlowColor aus der Designdefinition abgerufen.  <br/> |
|"GlowTransparency"  <br/> |Zellwert GlowColorTrans aus der Designdefinition abgerufen.  <br/> |
|"SketchAmount"  <br/> |Zellwert SketchAmount aus der Designdefinition abgerufen.  <br/> |
|"SketchEnabled"  <br/> |Zellwert SketchEnabled aus der Designdefinition abgerufen.  <br/> |
|"SketchFillChange"  <br/> |Zellwert SketchFillChange aus der Designdefinition abgerufen.  <br/> |
|"SketchLineChange"  <br/> |Zellwert SketchLineChange aus der Designdefinition abgerufen.  <br/> |
|"SketchLineWeight"  <br/> |Zellwert SketchLineWeight aus der Designdefinition abgerufen.  <br/> |
|"LatinFont"  <br/> |Zellwert Schriftart aus der Designdefinition abgerufen.  <br/> |
|"TextColor"  <br/> |Zellwert Farbe aus der Designdefinition abgerufen.  <br/> |
|"TextStyle"  <br/> |Ruft den Zellwert Character.Style aus der Designdefinition.  <br/> |
|"ComplexFont"  <br/> |Zellwert ComplexScriptFont aus der Designdefinition abgerufen.  <br/> |
|"AsianFont"  <br/> |Zellwert AsianFont aus der Designdefinition abgerufen.  <br/> |
|"Farbe FillStop [X]"  <br/> |Ruft Farbwert der Zelle in Zeile *X* aus der Designdefinition.  <br/> |
|"Transparenz FillStop [X]"  <br/> |Zellwert in Zeile *X* ColorTrans aus der Designdefinition abgerufen.  <br/> |
|"Position FillStop [X]"  <br/> |Zellwert in Zeile *X* Position aus der Designdefinition abgerufen.  <br/> |
|"Farbe LineStop [X]"  <br/> |Ruft Farbwert der Zelle in Zeile *X* aus der Designdefinition.  <br/> |
|"Transparenz LineStop [X]"  <br/> |Zellwert in Zeile *X* ColorTrans aus der Designdefinition abgerufen.  <br/> |
|"Position LineStop [X]"  <br/> |Zellwert in Zeile *X* Position aus der Designdefinition abgerufen.  <br/> |
   
## <a name="example"></a>Beispiel

 `THEMEVAL("5")`
  
Gibt die Farbe "Akzent 3" von der Designdefinition zurück.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Gibt den Wert der Zelle "LineWeight" von der Designdefinition zurück. Wenn die Form, die diese Funktion enthält kein Design angewendet hat, gibt die Funktion "0,7 pt".
  

