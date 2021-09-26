---
title: FLOOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
ms.localizationpriority: medium
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Rundet eine Zahl in Richtung 0 (Null), auf die nächste ganze Zahl oder auf die nächste Instanz von mehreren.
ms.openlocfilehash: 280697a8c8f38d122cd4cd1a1e7802e55b100107
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598689"
---
# <a name="floor-function"></a>FLOOR Function

Rundet eine Zahl in Richtung 0 (Null), auf die nächste ganze Zahl oder auf die nächste Instanz  _mehrerer_.
  
## <a name="syntax"></a>Syntax

FLOOR(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die zu rundende Zahl.  <br/> |
| _Mehrere_ <br/> |Erforderlich  <br/> |**Number** <br/> |Das Vielfache, auf das gerundet werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn  Multiple nicht angegeben ist, wird die Zahl in Richtung 0 auf die nächste ganze Zahl gerundet. 
  
 _Zahl_ und Mehrere müssen dieselben Vorzeichen oder ein #NUM aufweisen!  zurückgegeben. Wenn  _eine Zahl_ oder  _ein Vielfaches_ nicht in einen Wert konvertiert werden kann, #VALUE! zurückgegeben. Wenn  _Zahl_ oder  _Vielfache_ 0 ist, ist das Ergebnis 0. 
  
## <a name="example-1"></a>Beispiel 1

FLOOR(3.7)
  
Gibt 3 zurück.
  
## <a name="example-2"></a>Beispiel 2

FLOOR(-3.7)
  
Gibt -3 zurück.
  
## <a name="example-3"></a>Beispiel 3

FLOOR(3.7, 0.5)
  
Gibt 3,5 zurück.
  

