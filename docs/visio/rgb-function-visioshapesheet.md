---
title: RGB-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Gibt einen Wert zurück, der einen Index in der Farbpalette des Dokuments darstellt. Sie gibt eine Farbe anhand ihrer rot-, grün-und Blau-Komponenten an, wobei jedes eine Zahl im Bereich von 0 bis 255, einschließlich oder ein Ausdruck ist, der zu einer solchen Zahl ausgewertet wird.
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426303"
---
# <a name="rgb-function-visioshapesheet"></a>RGB-Funktion (VisioShapeSheet)

Gibt einen Wert zurück, der einen Index in der Farbpalette des Dokuments darstellt. Sie gibt eine Farbe anhand ihrer rot-, grün-und Blau-Komponenten an, wobei jedes eine Zahl im Bereich von 0 bis 255, einschließlich oder ein Ausdruck ist, der zu einer solchen Zahl ausgewertet wird. 
  
## <a name="syntax"></a>Syntax

RGB (* * *rot* * *, * * *grün* * *, * * *blau* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _rot_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Rotkomponente.  <br/> |
| _grün_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Grünkomponente.  <br/> |
| _blau_ <br/> |Erforderlich  <br/> |**Nmber** <br/> |Die Blaukomponente.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

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

RGB (0, 0255)
  
Gibt den Index für die Farbe Blau zurück.
  
## <a name="example-2"></a>Beispiel 2

RGB (rot (Blatt. 1! Zelle FillForegnd), 120, 0)
  
Gibt den Index für eine Farbe zurück, deren Rotkomponente der Vordergrundfüllfarbe von Sheet.1 entspricht.
  

