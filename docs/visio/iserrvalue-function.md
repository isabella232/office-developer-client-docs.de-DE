---
title: ISERRVALUE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
ms.localizationpriority: medium
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Gibt TRUE zurück, wenn der Wert der Zellreferenz fehlertyp #VALUE ist, wobei ein Argument in der Formel den falschen Typ aufweist. Die ISERRVALUE-Funktion wird in logischen Ausdrücken verwendet, die auf eine andere Zelle verweisen.'
ms.openlocfilehash: 0186b0b51e89fad3106bb1df034615ce9e512060
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574097"
---
# <a name="iserrvalue-function"></a>ISERRVALUE Function

Gibt TRUE zurück, wenn der Wert der  _Zellreferenz_ fehlertyp #VALUE ist, wobei ein Argument in der Formel den falschen Typ aufweist. Die ISERRVALUE-Funktion wird in logischen Ausdrücken verwendet, die auf eine andere Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

ISERRVALUE(** *cellreference* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Entwurfzellen A bis D geben keinen Fehler vom Typ #WERT! zurück, da ihre Formeln in der gleichen Zeichenfolge Zahlen und Buchstaben enthalten können. Die Zellen X und Y dürfen nur Zahlen enthalten. 
  
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formel**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="Haus"  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2  <br/> |
   
Gibt 2 zurück, da der zurückgegebene Wert den Fehlertyp #WERT! aufweist und der Ausdruck Microsoft Visio anweist, statt des Fehlers eine 2 zurückzugeben.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formel**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 7"  <br/> |5 + 7  <br/> |
|Scratch.B1  <br/> |= If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Gibt 12 zurück, da der zurückgegebene Wert nicht den Fehlertyp #WERT! aufweist und der Ausdruck Visio anweist, den Wert der ursprünglichen Zelle zurückzugeben.
  

