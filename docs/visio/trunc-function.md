---
title: TRUNC-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Gibt eine Zahl zurück, die auf die angegebene Anzahl von Ziffern gekürzt wurde.
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426499"
---
# <a name="trunc-function"></a>TRUNC Function

Gibt eine Zahl zurück, die auf die angegebene Anzahl von Ziffern gekürzt wurde.
  
## <a name="syntax"></a>Syntax

TRUNC(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die zu kürzende Zahl.  <br/> |
| _numberofdigits_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die Anzahl der Ziffern, auf die die Nummer abgeschnitten werden _soll._  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Numerisch.
  
## <a name="remarks"></a>Hinweise

Wenn  _numberofdigits_ größer als 0 ist, wird  _number_  _auf numberofdigits_ rechts neben dem Dezimalkomma abgeschnitten. Wenn  _numberofdigits_ 0 ist,  _wird zahl_ auf eine ganze Zahl abgeschnitten. Wenn  _numberofdigits_ kleiner als 0 ist, wird  _number_  _auf numberofdigits links_ vom Dezimaltrennzeichen abgeschnitten. 
  
## <a name="example-1"></a>Beispiel 1

TRUNC(123.654,2)
  
Gibt 123,65 zurück.
  
## <a name="example-2"></a>Beispiel 2

TRUNC(123.654,0)
  
Gibt 123 zurück.
  
## <a name="example-3"></a>Beispiel 3

TRUNC(123.654,-1)
  
Gibt 120 zurück.
  

