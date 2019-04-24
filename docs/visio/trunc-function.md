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
description: Gibt eine Zahl zurück, die auf die angegebene Anzahl von Ziffern abgeschnitten wurde.
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335175"
---
# <a name="trunc-function"></a>TRUNC Function

Gibt eine Zahl zurück, die auf die angegebene Anzahl von Ziffern abgeschnitten wurde.
  
## <a name="syntax"></a>Syntax

KÜRZEN (* * *Number* * *, * * *Wert von AnzahlVonStellen* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Die zu kürzende Zahl.  <br/> |
| _Wert von AnzahlVonStellen_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Die Anzahl der Ziffern, auf die die _Zahl_gekürzt werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Numerischen.
  
## <a name="remarks"></a>Bemerkungen

Wenn _Wert von AnzahlVonStellen_ größer als 0 ist, wird die _Zahl_ auf _Wert von AnzahlVonStellen_ rechts vom Dezimaltrennzeichen abgeschnitten. Wenn _Wert von AnzahlVonStellen_ 0 ist, wird _Number_ auf eine ganze Zahl gekürzt. Wenn _Wert von AnzahlVonStellen_ kleiner als 0 ist, wird die _Zahl_ auf _Wert von AnzahlVonStellen_ Links vom Dezimaltrennzeichen abgeschnitten. 
  
## <a name="example-1"></a>Beispiel 1

KÜRZEN (123.654, 2)
  
Gibt 123,65 zurück.
  
## <a name="example-2"></a>Beispiel 2

KÜRZEN (123.654, 0)
  
Gibt 123 zurück.
  
## <a name="example-3"></a>Beispiel 3

KÜRZEN (123.654,-1)
  
Gibt 120 zurück.
  

