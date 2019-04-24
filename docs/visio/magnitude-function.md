---
title: MAGNITUDE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Gibt die Größe des Vektors zurück, dessen Anstieg A ist und dessen Ausführung B ist, multipliziert mit den entsprechenden Konstanten constantA und Konstanteb.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317815"
---
# <a name="magnitude-function"></a>MAGNITUDE Function

Gibt die Größe des Vektors zurück, dessen Anstieg _A_ ist und dessen Ausführung _B_ist, multipliziert mit den entsprechenden Konstanten _constantA_ und _konstanteb_. 
  
## <a name="syntax"></a>Syntax

MAGNITUDE (* * *constantA* * *, * * *a* * *, * * *konstanteb* * *, * * *B* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _constantA_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Konstante, mit der die Steigung multipliziert werden soll.  <br/> |
| _A_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Steigung.  <br/> |
| _Konstanteb_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Konstante, mit der die Länge multipliziert werden soll.  <br/> |
| _B_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Länge.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

MAGNITUDE wird nach folgender Formel berechnet:
  
SQRT ((constantA \* A) ^ 2 + (konstanteb \* B) ^ 2)
  
## <a name="example"></a>Beispiel

MAGNITUDE(1, 3, 1, 4) 
  
Gibt 5 zurück. 
  

