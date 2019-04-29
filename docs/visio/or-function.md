---
title: OR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Gibt TRUE (1) zurück, wenn einer der logischen Ausdrücke, die als Parameter übergeben werden, TRUE ist.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433507"
---
# <a name="or-function"></a>OR Function

Gibt TRUE (1) zurück, wenn einer der logischen Ausdrücke, die als Parameter übergeben werden, TRUE ist.
  
## <a name="syntax"></a>Syntax

oder (* * *logicalexpression1* * *, * * *logicalexpression2* * *,..., * * *logicalexpressionN* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |Erforderlich  <br/> |**String** <br/> |Der erste Ausdruck, dessen Wahrheit ausgewertet werden soll.  <br/> |
| _logicalexpression2_ <br/> |Erforderlich  <br/> |**String** <br/> |Der zweite Ausdruck, dessen Wahrheit ausgewertet werden soll.  <br/> |
| _logicalexpressionN_ <br/> |Erforderlich  <br/> |**String** <br/> |Der n-te Ausdruck, dessen Wahrheit ausgewertet werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Boolesch
  
## <a name="remarks"></a>Bemerkungen

Ein beliebiger Ausdruck, der einen Wert ungleich Null ergibt, wird als TRUE betrachtet. Wenn alle logischen Ausdrücke den Wert FALSE oder 0 aufweisen, gibt die Funktion FALSE zurück. 
  
## <a name="example"></a>Beispiel

OR (Höhe \> 1, PinX \> 1) 
  
Gibt TRUE (1) zurück, wenn mindestens einer der beiden Ausdrücke TRUE ist. Gibt FALSE (0) zurück, wenn beide Ausdrücke FALSE sind. 
  

