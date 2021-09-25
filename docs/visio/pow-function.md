---
title: POW-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
ms.localizationpriority: medium
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Gibt eine Zahl zurück, die mit der Potenz eines Exponenten ausgelöst wurde.
ms.openlocfilehash: 5c829bb4ec236b251cc258fed6d2c862ede54980
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570330"
---
# <a name="pow-function"></a>POW Function

Gibt eine Zahl zurück, die mit der Potenz eines Exponenten ausgelöst wurde.
  
## <a name="syntax"></a>Syntax

POW(** *number* **, ** *exponent* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Zahl, die mit einem Exponenten potenziert werden soll.  <br/> |
| _exponent_ <br/> |Erforderlich  <br/> |**Number** <br/> |Der Exponent.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

_Zahl_ und _Exponent_ können nicht ganze Zahlen sein, und sie können negativ sein. Wenn _Zahl_ nicht 0 und Exponent 0 ist, gibt diese Funktion 1 zurück.  Wenn _Zahl_ 0 ist und Exponent negativ ist, gibt diese Funktion 0,0 zurück.  Wenn  _Zahl_ und  _Exponent_ 0 sind oder wenn  _Zahl_ negativ und  _exponent_ keine ganze Zahl ist, gibt diese Funktion 0,0 zurück. Wenn  _Zahl_ und  _Exponent_ negativ sind, gibt diese Funktion -1,#IND zurück. 
  
## <a name="example"></a>Beispiel

POW(5,2) 
  
Gibt 25 zurück. 
  

