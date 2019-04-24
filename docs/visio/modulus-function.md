---
title: MODULUS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Gibt den Rest (Modulo) zurück, der ergibt, wenn eine Zahl durch einen Divisor geteilt wird.
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356994"
---
# <a name="modulus-function"></a>MODULUS Function

Gibt den Rest (Modulo) zurück, der ergibt, wenn eine Zahl durch einen Divisor geteilt wird.
  
## <a name="syntax"></a>Syntax

MODULo (* * *Number* * *, * * *Divisor* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Der Dividend.  <br/> |
| _Divisor_ <br/> |Erforderlich  <br/> |**Number** <br/> |Der Divisor.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Das Ergebnis hat das gleiche Vorzeichen wie der Divisor. Wenn der Divisor 0 ist, wird der Fehler #DIV/0! zurückgegeben. 
  
In fast allen Situationen sollte die MODULUS-Funktion gegenüber der MOD-Funktion verwendet werden. 
  
## <a name="example-1"></a>Beispiel 1

MODULUS(5, 1,4)
  
Gibt 0,8 zurück.
  
## <a name="example-2"></a>Beispiel 2

MODULUS(5, -1,4)
  
Gibt -0,6 zurück.
  
## <a name="example-3"></a>Beispiel 3

MODULUS(-5, 1,4)
  
Gibt 0,6 zurück.
  
## <a name="example-4"></a>Beispiel 4

MODULUS(-5, -1,4)
  
Gibt -0,8 zurück.
  

