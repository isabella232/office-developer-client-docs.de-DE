---
title: AND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Gibt TRUE (1) zurück, wenn alle angegebenen logischen Ausdrücke TRUE sind. Wenn einer der logischen Ausdrücke FALSE oder 0 ist, gibt die-und-Funktion FALSE (0) zurück.
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341559"
---
# <a name="and-function"></a>AND Function

Gibt TRUE (1) zurück, wenn alle angegebenen logischen Ausdrücke TRUE sind. Wenn einer der logischen Ausdrücke FALSE oder 0 ist, gibt die-und-Funktion FALSE (0) zurück.
  
## <a name="syntax"></a>Syntax

und (* * *logisches expression1* * *, * * logisches *expression2* * *,..., * * *logische ausdrücke* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _logischer Ausdruck_ <br/> |Erforderlich  <br/> |**String** <br/> | Eine Kombination aus Konstanten, Operatoren, Funktionen und Verweisen auf ShapeSheet-Zellen, die einen Wert ergeben. Ein mit einem Wert ungleich null ausgewerteter Ausdruck wird als TRUE angegeben.  <br/> |
   
## <a name="example"></a>Beispiel

UND (Höhe \> 1, PinX \> 1)
  
Liefert TRUE, wenn beide Ausdrücke TRUE sind. Liefert FALSE, wenn einer der beiden Ausdrücke FALSE ist.
  

