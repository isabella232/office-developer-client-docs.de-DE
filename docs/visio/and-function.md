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
description: Gibt TRUE (1) zurück, wenn alle angegebenen logischen Ausdrücke wahr sind. Wenn einer der logischen Ausdrücke FALSE oder 0 ist, gibt die Funktion und FALSE (0) zurück.
ms.openlocfilehash: 27b2ef97ef1d0afde37596b18674c6de26355a1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796409"
---
# <a name="and-function"></a>AND Function

Gibt TRUE (1) zurück, wenn alle angegebenen logischen Ausdrücke wahr sind. Wenn einer der logischen Ausdrücke FALSE oder 0 ist, gibt die Funktion und FALSE (0) zurück.
  
## <a name="syntax"></a>Syntax

UND (** *logische expression1* **, ** *logische expression2* **,..., ** *logische ExpressionN* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _logische Ausdruck_ <br/> |Erforderlich  <br/> |**String** <br/> | Eine Kombination aus Konstanten, Operatoren, Funktionen und Verweisen auf ShapeSheet-Zellen, die einen Wert ergeben. Ein mit einem Wert ungleich null ausgewerteter Ausdruck wird als TRUE angegeben.  <br/> |
   
## <a name="example"></a>Beispiel

UND (Höhe \> 1, DrehbezX \> 1)
  
Liefert TRUE, wenn beide Ausdrücke TRUE sind. Liefert FALSE, wenn einer der beiden Ausdrücke FALSE ist.
  

