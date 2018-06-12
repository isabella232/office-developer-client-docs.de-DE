---
title: ISERRVALUE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Gibt True, wenn der Wert von Zellbezug Fehler ist geben #VALUE, wobei ein Argument in der Formel den falschen Typ besitzt. ISERRVALUE-Funktion wird in logischen Ausdrücken verwendet, die auf einer anderen Zelle verweisen.'
ms.openlocfilehash: 50c501cc404d9c5f80e0bd1261b3d3bcd7087de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797246"
---
# <a name="iserrvalue-function"></a>ISERRVALUE-Funktion

Gibt True, wenn der Wert von _Zellbezug_ Fehler ist geben #VALUE, wobei ein Argument in der Formel den falschen Typ besitzt. ISERRVALUE-Funktion wird in logischen Ausdrücken verwendet, die auf einer anderen Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

ISERRVALUE (** *Zellbezug* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zellbezug_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Entwurfzellen A bis D geben keinen Fehler vom Typ #WERT! zurück, da ihre Formeln in der gleichen Zeichenfolge Zahlen und Buchstaben enthalten können. Die Zellen X und Y dürfen nur Zahlen enthalten. 
  
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="Haus"  <br/> |#WERT!  <br/> |
|Scratch.A1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2  <br/> |
   
Gibt 2 zurück, da der zurückgegebene Wert den Fehlertyp #WERT! aufweist und der Ausdruck Microsoft Visio anweist, statt des Fehlers eine 2 zurückzugeben.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 7"  <br/> |5 + 7  <br/> |
|Scratch.B1  <br/> |= If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Gibt 12 zurück, da der zurückgegebene Wert nicht den Fehlertyp #WERT! aufweist und der Ausdruck Visio anweist, den Wert der ursprünglichen Zelle zurückzugeben.
  

