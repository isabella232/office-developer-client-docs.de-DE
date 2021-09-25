---
title: MODULUS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
ms.localizationpriority: medium
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Gibt den Rest (Modulus) zurück, der resultiert, wenn eine Zahl durch einen Teiler geteilt wird.
ms.openlocfilehash: 6d6d9893800aa8db0e882dd92d4adb0d05acb930
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623334"
---
# <a name="modulus-function"></a>MODULUS Function

Gibt den Rest (Modulus) zurück, der resultiert, wenn eine Zahl durch einen Teiler geteilt wird.
  
## <a name="syntax"></a>Syntax

MODULUS(** *number* **, ** *divisor* ** ) 
  
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
  

