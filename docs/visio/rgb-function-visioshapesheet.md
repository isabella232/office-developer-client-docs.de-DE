---
title: RGB Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Gibt einen Wert, der einen Index in der Farbpalette des Dokuments darstellt. Es gibt eine Farbe nach seiner Rot-, Grün- und blauen-Komponenten, wobei es sich um eine Zahl im Bereich von 0 bis einschließlich 255 oder ein Ausdruck, der als eine derartige Zahl ausgewertet wird.
ms.openlocfilehash: 7fa129d3ed28441f619660ed0db035cde85979bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797856"
---
# <a name="rgb-function-visioshapesheet"></a>RGB Function (VisioShapeSheet)

Gibt einen Wert, der einen Index in der Farbpalette des Dokuments darstellt. Es gibt eine Farbe nach seiner Rot-, Grün- und blauen-Komponenten, wobei es sich um eine Zahl im Bereich von 0 bis einschließlich 255 oder ein Ausdruck, der als eine derartige Zahl ausgewertet wird. 
  
## <a name="syntax"></a>Syntax

RGB (** *Rot* **, ** *grüne* **, ** *Blau* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Rot_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Rotkomponente.  <br/> |
| _Grün_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Grünkomponente.  <br/> |
| _Blau_ <br/> |Erforderlich  <br/> |**Nmber** <br/> |Die Blaukomponente.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Wenn die durch die Funktion zurückgegebene Farbe nicht bereits in der Farbpalette des aktuellen Dokuments vorhanden ist, wird sie in diese eingefügt.
  
Die folgende Tabelle listet einige Standardfarben mit ihren Rot-, Grün- und Blauwerten auf.
  
|**Color**|**Rotwert**|**Grünwert**|**Blauwert**|
|:-----|:-----|:-----|:-----|
|Schwarz  <br/> |0  <br/> |0  <br/> |0  <br/> |
|Blau  <br/> |0  <br/> |0  <br/> |255  <br/> |
|Grün  <br/> |0  <br/> |255  <br/> |0  <br/> |
|Cyan  <br/> |0  <br/> |255  <br/> |255  <br/> |
|Rot  <br/> |255  <br/> |0  <br/> |0  <br/> |
|Magenta  <br/> |255  <br/> |0  <br/> |255  <br/> |
|Gelb  <br/> |255  <br/> |255  <br/> |0  <br/> |
|Weiß  <br/> |255  <br/> |255  <br/> |255  <br/> |
   
## <a name="example-1"></a>Beispiel 1

RGB(0,0,255)
  
Gibt den Index für die Farbe Blau zurück.
  
## <a name="example-2"></a>Beispiel 2

RGB (Rot (Sheet.1! FillForegnd), 120, 0)
  
Gibt den Index für eine Farbe zurück, deren Rotkomponente der Vordergrundfüllfarbe von Sheet.1 entspricht.
  

