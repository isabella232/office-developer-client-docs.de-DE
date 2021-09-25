---
title: AND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
ms.localizationpriority: medium
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Gibt TRUE (1) zurück, wenn alle angegebenen logischen Ausdrücke TRUE sind. Wenn einer der logischen Ausdrücke FALSE oder 0 ist, gibt die AND-Funktion FALSE (0) zurück.
ms.openlocfilehash: 82ce384641c400764356d3288ae7d903ee901292
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628878"
---
# <a name="and-function"></a>AND Function

Gibt TRUE (1) zurück, wenn alle angegebenen logischen Ausdrücke TRUE sind. Wenn einer der logischen Ausdrücke FALSE oder 0 ist, gibt die AND-Funktion FALSE (0) zurück.
  
## <a name="syntax"></a>Syntax

AND(** *logical expression1* **, ** *logical expression2* **,..., ** *logical expressionN* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Logischer Ausdruck_ <br/> |Erforderlich  <br/> |**String** <br/> | Eine Kombination aus Konstanten, Operatoren, Funktionen und Verweisen auf ShapeSheet-Zellen, die einen Wert ergeben. Ein mit einem Wert ungleich null ausgewerteter Ausdruck wird als TRUE angegeben.  <br/> |
   
## <a name="example"></a>Beispiel

AND(Height \> 1, PinX \> 1)
  
Liefert TRUE, wenn beide Ausdrücke TRUE sind. Liefert FALSE, wenn einer der beiden Ausdrücke FALSE ist.
  

