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

 **THEMEVAL** ([ _"theme_value"_] [, _default_]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _"theme_value"_ <br/> |Optional  <br/> |**String** <br/> |Der Name einer Zelle in der Design Definition, aus der ein Wert abgerufen werden soll.  <br/> |
| _default_ <br/> |Optional  <br/> |Verschiedene  <br/> |Ein Standardwert, wenn das Dokument nicht thematisch ist (es gibt keine Design Definition).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die **THEMEVAL** -Funktion keine Argumente empfängt, wird der Wert der Host Zelle zurückgegeben. Dies ist der Wert, der in der Definition des aktuellen Designs gespeichert ist. Die Host Zelle muss in der Lage sein, einen Wert zurückzugeben; Wenn die Zelle nicht in der Lage ist, themaisch zu sein, gibt **THEMEVAL** einen Fehler zurück. 
  
Wenn die **THEMEVAL** -Funktion ein einzelnes Argument empfängt, ruft Sie den Wert aus der Design Definition ab, die als Argument übergeben wurde. Das Argument, das für den ersten Parameter übergeben wird, muss eine ganze Zahl oder eine der genauen Zeichenfolgen in der folgenden Tabelle sein. 
  
Die **THEMEVAL** -Funktion kann auch eine ganze Zahl für den ersten Parameter als Wert zwischen 1 und 8 annehmen. Bei Verwendung von ganzzahligen Werten wird eine Farbe nach Index aus dem Farbschema des Designs abgerufen. Daher gibt der Wert "1" die dunkle Farbe aus dem Design zurück, "2" gibt die Farbe "Light" zurück, ' 3 ' gibt die Farbe "Akzent 1" zurück usw. 
  
Wenn die **THEMEVAL** -Funktion zwei Argumente empfängt, ruft Sie den Wert aus der Design Definition ab, die als erstes Argument übergeben wurde. Wenn jedoch auf das Dokument kein Design angewendet wird, verwendet die **THEMEVAL** -Funktion den Wert, der als zweites Argument angegeben wird. 
  
**Mögliche Argumente für den Parameter "theme_value"**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Dunkel  <br/> |Ruft dunkle RGB-Farbe aus der Design Definition ab.  <br/> |
|Licht  <br/> |Ruft die helle RGB-Farbe aus der Design Definition ab.  <br/> |
|Background Color  <br/> |Ruft Hintergrund-RGB-Farbe aus der Design Definition ab.  <br/> |
|"AccentColor"  <br/> |Ruft Accent1 RGB-Farbe aus der Design Definition ab.  <br/> |
|"AccentColor2"  <br/> |Ruft Accent2 RGB-Farbe aus der Design Definition ab.  <br/> |
|"AccentColor3"  <br/> |Ruft Accent3 RGB-Farbe aus der Design Definition ab.  <br/> |
|"AccentColor4"  <br/> |Ruft Accent4 RGB-Farbe aus der Design Definition ab.  <br/> |
|"AccentColor5"  <br/> |Ruft Accent5 RGB-Farbe aus der Design Definition ab.  <br/> |
|"AccentColor6"  <br/> |Ruft Accent6 RGB-Farbe aus der Design Definition ab.  <br/> |
|"LinePattern  <br/> |Ruft den "LinePattern-Zellenwert aus der Design Definition ab.  <br/> |
|LineWeight  <br/> |Ruft den LineWeight-Zellenwert aus der Design Definition ab.  <br/> |
|Zelle LineColor  <br/> |Ruft den Zelle LineColor-Zellenwert aus der Design Definition ab.  <br/> |
|"LineCap  <br/> |Ruft den "LineCap-Zellenwert aus der Design Definition ab.  <br/> |
|"LineBegin"  <br/> |Ruft den Zellenwert beginArrow aus der Design Definition ab.  <br/> |
|"LineEnd"  <br/> |Ruft den Zelle EndArrow-Zellenwert aus der Design Definition ab.  <br/> |
|Zelle linecolortrans  <br/> |Ruft den Zelle linecolortrans-Zellenwert aus der Design Definition ab.  <br/> |
|"LineCompoundtype"  <br/> |Ruft den Zellwert Compoundtype aus der Design Definition ab.  <br/> |
|"LineBegin"  <br/> |Ruft den Zellenwert beginArrow aus der Design Definition ab.  <br/> |
|"LineEnd"  <br/> |Ruft den Zelle EndArrow-Zellenwert aus der Design Definition ab.  <br/> |
|"LineBeginSize"  <br/> |Ruft den Zellenwert beginArrowS aus der Design Definition ab.  <br/> |
|"LineEndSize"  <br/> |Ruft den Zelle EndArrowSize-Zellenwert aus der Design Definition ab.  <br/> |
|"LineRounding"  <br/> |Ruft den Rundungs Zellenwert aus der Design Definition ab.  <br/> |
|"ConnectorColor"  <br/> |Ruft den Zelle LineColor-Zellenwert aus der Design Definition ab.  <br/> |
|"ConnectorPattern"  <br/> |Ruft den "LinePattern-Zellenwert aus der Design Definition ab.  <br/> |
|"ConnectorWeight"  <br/> |Ruft den LineWeight-Zellenwert aus der Design Definition ab.  <br/> |
|"ConnectorTransparency"  <br/> |Ruft den Zelle linecolortrans-Zellenwert aus der Design Definition ab.  <br/> |
|"ConnectorRounding"  <br/> |Ruft den Rundungs Zellenwert aus der Design Definition ab.  <br/> |
|"ConnectorBegin"  <br/> |Ruft den Zellenwert beginArrow aus der Design Definition ab.  <br/> |
|"ConnectorEnd"  <br/> |Ruft den Zelle EndArrow-Zellenwert aus der Design Definition ab.  <br/> |
|"ConnectorBeginSize"  <br/> |Ruft den Zellenwert beginArrowS aus der Design Definition ab.  <br/> |
|"ConnectorEndSize"  <br/> |Ruft den Zelle EndArrowSize-Zellenwert aus der Design Definition ab.  <br/> |
|FillColor  <br/> |Ruft den Zelle FillForegnd-Zellenwert aus der Design Definition ab.  <br/> |
|"FillColor2"  <br/> |Ruft den Zelle FillBkgnd-Zellenwert aus der Design Definition ab.  <br/> |
|"FillTransparency"  <br/> |Ruft den Zelle FillForegndTrans-Zellenwert aus der Design Definition ab.  <br/> |
|FillPattern  <br/> |Ruft den FillPattern-Zellenwert aus der Design Definition ab.  <br/> |
|"LineGradientEnabled"  <br/> |Ruft den LineGradientEnabled-Zellenwert aus der Design Definition ab.  <br/> |
|"LineGradientDir"  <br/> |Ruft den LineGradientDir-Zellenwert aus der Design Definition ab.  <br/> |
|"LineGradientAngle"  <br/> |Ruft den LineGradientAngle-Zellenwert aus der Design Definition ab.  <br/> |
|"FillGradientEnabled"  <br/> |Ruft den FillGradientEnabled-Zellenwert aus der Design Definition ab.  <br/> |
|"FillGradientDir"  <br/> |Ruft den FillGradientDir-Zellenwert aus der Design Definition ab.  <br/> |
|"FillGradientAngle"  <br/> |Ruft den FillGradientAngle-Zellenwert aus der Design Definition ab.  <br/> |
|"RotateGradientWithShape"  <br/> |Ruft den RotateGradientWithShape-Zellenwert aus der Design Definition ab.  <br/> |
|"UseGroupGradient"  <br/> |Ruft den UseGroupGradient-Zellenwert aus der Design Definition ab.  <br/> |
|"Shadowtype"  <br/> |Ruft den Zelle-Zellenwert aus der Design Definition ab.  <br/> |
|ShadowColor  <br/> |Ruft den ShdwColor-Zellenwert aus der Design Definition ab.  <br/> |
|"ShadowTransparency"  <br/> |Ruft den ShdwColorTrans-Zellenwert aus der Design Definition ab.  <br/> |
|"ShadowMagnification"  <br/> |Ruft den Zelle ShapeShdwScaleFactor-Zellenwert aus der Design Definition ab.  <br/> |
|"ShadowBlur"  <br/> |Ruft den ShapeShdwBlur-Zellenwert aus der Design Definition ab.  <br/> |
|"ShadowXOffset"  <br/> |Ruft den Zelle ShapeShdwOffsetX-Zellenwert aus der Design Definition ab.  <br/> |
|"ShadowYOffset"  <br/> |Ruft den Zelle ShapeShdwOffsetY-Zellenwert aus der Design Definition ab.  <br/> |
|"ShadowDirection"  <br/> |Ruft den Zelle ShapeShdwObliqueAngle-Zellenwert aus der Design Definition ab.  <br/> |
|"ShadowPattern"  <br/> |Ruft den Zelle ShdwPattern-Zellenwert aus der Design Definition ab.  <br/> |
|BevelTopType  <br/> |Ruft den BevelTopType-Zellenwert aus der Design Definition ab.  <br/> |
|"BevelTopWidth"  <br/> |Ruft den BevelTopWidth-Zellenwert aus der Design Definition ab.  <br/> |
|"BevelTopHeight"  <br/> |Ruft den BevelTopHeight-Zellenwert aus der Design Definition ab.  <br/> |
|"BevelMaterial"  <br/> |Ruft den BevelMaterialType-Zellenwert aus der Design Definition ab.  <br/> |
|"BevelLighting"  <br/> |Ruft den BevelLightingType-Zellenwert aus der Design Definition ab.  <br/> |
|"BevelLightingAngle"  <br/> |Ruft den BevelLightingAngle-Zellenwert aus der Design Definition ab.  <br/> |
|"BevelContourColor"  <br/> |Ruft den BevelContourColor-Zellenwert aus der Design Definition ab.  <br/> |
|"BevelContourSize"  <br/> |Ruft den BevelContourSize-Zellenwert aus der Design Definition ab.  <br/> |
|"ReflectionBlur"  <br/> |Ruft den ReflectionBlur-Zellenwert aus der Design Definition ab.  <br/> |
|"ReflectionDist"  <br/> |Ruft den ReflectionDist-Zellenwert aus der Design Definition ab.  <br/> |
|"Reflexion"  <br/> |Ruft den reFlexe-Zellenwert aus der Design Definition ab.  <br/> |
|"ReflectionTrans"  <br/> |Ruft den ReflectionTrans-Zellenwert aus der Design Definition ab.  <br/> |
|"SoftEdgesSize"  <br/> |Ruft den SoftEdgesSize-Zellenwert aus der Design Definition ab.  <br/> |
|GlowSize  <br/> |Ruft den GlowSize-Zellenwert aus der Design Definition ab.  <br/> |
|GlowColor  <br/> |Ruft den GlowColor-Zellenwert aus der Design Definition ab.  <br/> |
|"GlowTransparency"  <br/> |Ruft den GlowColorTrans-Zellenwert aus der Design Definition ab.  <br/> |
|"SketchAmount"  <br/> |Ruft den SketchAmount-Zellenwert aus der Design Definition ab.  <br/> |
|"SketchEnabled"  <br/> |Ruft den SketchEnabled-Zellenwert aus der Design Definition ab.  <br/> |
|"SketchFillChange"  <br/> |Ruft den SketchFillChange-Zellenwert aus der Design Definition ab.  <br/> |
|"SketchLineChange"  <br/> |Ruft den SketchLineChange-Zellenwert aus der Design Definition ab.  <br/> |
|"SketchLineWeight"  <br/> |Ruft den SketchLineWeight-Zellenwert aus der Design Definition ab.  <br/> |
|"LatinFont"  <br/> |Ruft den Schriftart Zellenwert aus der Design Definition ab.  <br/> |
|TextColor  <br/> |Ruft den Farbzellen Wert aus der Design Definition ab.  <br/> |
|TextStyle  <br/> |Ruft den Zellenwert Character. Style aus der Design Definition ab.  <br/> |
|"ComplexFont"  <br/> |Ruft den "ComplexScriptFont-Zellenwert aus der Design Definition ab.  <br/> |
|"AsianFont  <br/> |Ruft den "AsianFont-Zellenwert aus der Design Definition ab.  <br/> |
|"FillStop [x] Color"  <br/> |Ruft den Farbzellen Wert in Zeile *x* aus der Design Definition ab.  <br/> |
|"FillStop [x] Transparenz"  <br/> |Ruft ColorTrans Zellenwert in Zeile *x* aus der Design Definition ab.  <br/> |
|"FillStop [x] Position"  <br/> |Ruft den Zellenwert Position in Zeile *x* aus der Design Definition ab.  <br/> |
|"LineStop [x] Color"  <br/> |Ruft den Farbzellen Wert in Zeile *x* aus der Design Definition ab.  <br/> |
|"LineStop [x] Transparenz"  <br/> |Ruft ColorTrans Zellenwert in Zeile *x* aus der Design Definition ab.  <br/> |
|"LineStop [x] Position"  <br/> |Ruft den Zellenwert Position in Zeile *x* aus der Design Definition ab.  <br/> |
   
## <a name="example"></a>Beispiel

 `THEMEVAL("5")`
  
Gibt die Farbe "Akzent 3" aus der Design Definition zurück.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Gibt den Wert der Zelle LineWeight aus der Design Definition zurück. Wenn auf das Shape mit dieser Funktion kein Design angewendet wurde, gibt die Funktion ' 0,7 pt. ' zurück.
  

