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
description: 'Gibt TRUE zurück, wenn der Wert von cellreference den Fehlertyp #VALUE, wobei ein Argument in der Formel den falschen Typ aufweist. Die ISERRVALUE-Funktion wird in logischen Ausdrücken verwendet, die auf eine andere Zelle verweisen.'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404428"
---
# <a name="iserrvalue-function"></a>ISERRVALUE Function

Gibt TRUE zurück, wenn der Wert von _cellreference_ den fehlertyp #VALUE, wobei ein Argument in der Formel den falschen Typ aufweist. Die ISERRVALUE-Funktion wird in logischen Ausdrücken verwendet, die auf eine andere Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

ISERRVALUE (* * *cellreference* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Entwurfzellen A bis D geben keinen Fehler vom Typ #WERT! zurück, da ihre Formeln in der gleichen Zeichenfolge Zahlen und Buchstaben enthalten können. Die Zellen X und Y dürfen nur Zahlen enthalten. 
  
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch. x1  <br/> |="Haus"  <br/> |#VALUE!  <br/> |
|Scratch. a1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2  <br/> |
   
Gibt 2 zurück, da der zurückgegebene Wert den Fehlertyp #WERT! aufweist und der Ausdruck Microsoft Visio anweist, statt des Fehlers eine 2 zurückzugeben.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |="5 + 7"  <br/> |5 + 7  <br/> |
|Scratch. B1  <br/> |= If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Gibt 12 zurück, da der zurückgegebene Wert nicht den Fehlertyp #WERT! aufweist und der Ausdruck Visio anweist, den Wert der ursprünglichen Zelle zurückzugeben.
  

