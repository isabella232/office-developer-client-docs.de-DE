---
title: TRUNC-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
ms.localizationpriority: medium
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Gibt eine Zahl zurück, die auf die angegebene Anzahl von Ziffern abgeschnitten ist.
ms.openlocfilehash: d7a682fe413248af6da0eac6895f4e0a0a6de800
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603249"
---
# <a name="trunc-function"></a>TRUNC Function

Gibt eine Zahl zurück, die auf die angegebene Anzahl von Ziffern abgeschnitten ist.
  
## <a name="syntax"></a>Syntax

TRUNC(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die zu kürzende Zahl.  <br/> |
| _numberofdigits_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die Anzahl der Stellen, auf die die  _Zahl_ abgeschnitten werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Numerischen.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn  _Numberofdigits_ größer als 0 ist, wird die  _Zahl_ auf  _numberofdigits_ rechts neben dem Dezimaltrennzeichen abgeschnitten. Wenn  _Numberofdigits_ 0 ist, wird  _Zahl_ auf eine ganze Zahl gekürzt. Wenn  _Numberofdigits_ kleiner als 0 ist, wird die  _Zahl_ auf  _numberofdigits_ links neben dem Dezimaltrennzeichen abgeschnitten. 
  
## <a name="example-1"></a>Beispiel 1

TRUNC(123.654,2)
  
Gibt 123,65 zurück.
  
## <a name="example-2"></a>Beispiel 2

TRUNC(123.654,0)
  
Gibt 123 zurück.
  
## <a name="example-3"></a>Beispiel 3

TRUNC(123.654,-1)
  
Gibt 120 zurück.
  

