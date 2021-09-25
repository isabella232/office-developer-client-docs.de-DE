---
title: MAGNITUDE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
ms.localizationpriority: medium
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Gibt die Größe des Vektors zurück, dessen Anstieg A und dessen Lauf B ist, multipliziert mit den entsprechenden Konstanten KonstanteA und KonstanteB.
ms.openlocfilehash: ac3eb76ad2ad5c20e76f391c6ceedea50d1c3d8d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582505"
---
# <a name="magnitude-function"></a>MAGNITUDE Function

Gibt die Größe des Vektors zurück, dessen Anstieg _A_ und dessen Lauf _B_ ist, multipliziert mit den entsprechenden Konstanten _KonstanteA_ und _KonstanteB._ 
  
## <a name="syntax"></a>Syntax

MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Constanta_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Konstante, mit der die Steigung multipliziert werden soll.  <br/> |
| _A_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Steigung.  <br/> |
| _constantB_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Konstante, mit der die Länge multipliziert werden soll.  <br/> |
| _B_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Länge.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

MAGNITUDE wird nach folgender Formel berechnet:
  
SQRT((constantA \* A)^2 + (constantB \* B)^2)
  
## <a name="example"></a>Beispiel

MAGNITUDE(1, 3, 1, 4) 
  
Gibt 5 zurück. 
  

