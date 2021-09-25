---
title: ROUND-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
ms.localizationpriority: medium
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Rundet eine Zahl auf die Genauigkeit, die durch numberofdigits dargestellt wird.
ms.openlocfilehash: e004542ba0cd8b804893698045d3f9d67737b520
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554075"
---
# <a name="round-function-visioshapesheet"></a>ROUND-Funktion (VisioShapeSheet)

Rundet eine Zahl auf die Genauigkeit, die durch  *numberofdigits*  dargestellt wird. 
  
## <a name="syntax"></a>Syntax

ROUND(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die zu rundende Zahl.  <br/> |
| _numberofdigits_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Anzahl der Dezimalstellen für den Grad der Genauigkeit.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn  _Numberofdigits_ größer als 0 ist, wird die  _Zahl_ um  _numberofdigits_ rechts neben dem Dezimaltrennzeichen gerundet. Wenn  _Numberofdigits_ 0 ist, wird  _Zahl_ auf eine ganze Zahl gerundet. Wenn  _Numberofdigits_ kleiner als 0 ist, wird die  _Zahl_ um  _numberofdigits_ links neben dem Dezimaltrennzeichen gerundet. 
  
## <a name="example-1"></a>Beispiel 1

ROUND(123.654,2)
  
Gibt 123,65 zurück.
  
## <a name="example-2"></a>Beispiel 2

ROUND(123.654,0)
  
Gibt 124 zurück.
  
## <a name="example-3"></a>Beispiel 3

ROUND(123.654,-1)
  
Gibt 120 zurück.
  

