---
title: CEILING-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
ms.localizationpriority: medium
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Rundet eine Zahl von 0 (null) auf die nächste Instanz von mehreren ab. Wenn Multiple nicht angegeben ist, wird die Zahl von 0 auf die nächste ganze Zahl gerundet.
ms.openlocfilehash: e544be99fe035e1394d55acb0af5a8ee78e7a06f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578116"
---
# <a name="ceiling-function"></a>CEILING Function

Rundet eine Zahl von 0 (null) auf die nächste Instanz  _mehrerer_. Wenn  Multiple nicht angegeben ist, wird die Zahl von 0 auf die nächste ganze Zahl gerundet. 
  
## <a name="syntax"></a>Syntax

CEILING(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die zu rundende Zahl.  <br/> |
| _Mehrere_ <br/> |Erforderlich  <br/> |**Number** <br/> |Das Vielfache, auf das gerundet werden soll.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 _Zahl_ und Mehrere müssen dieselben Vorzeichen oder ein #NUM aufweisen!  zurückgegeben. Wenn  _eine Zahl_ oder  _ein Vielfaches_ nicht in einen Wert konvertiert werden kann, #VALUE! zurückgegeben. Wenn  _Zahl_ oder  _Vielfache_ 0 ist, ist das Ergebnis 0. 
  
## <a name="example-1"></a>Beispiel 1

CEILING(3.7)
  
Gibt 4 zurück.
  
## <a name="example-2"></a>Beispiel 2

CEILING(-3.7)
  
Gibt -4 zurück.
  
## <a name="example-3"></a>Beispiel 3

CEILING(3.7, 0.25)
  
Gibt 3,75 zurück.
  

