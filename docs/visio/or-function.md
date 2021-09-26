---
title: OR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
ms.localizationpriority: medium
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Gibt TRUE (1) zurück, wenn einer der logischen Ausdrücke, die als Parameter übergeben werden, TRUE ist.
ms.openlocfilehash: 3d625417b52f970cb529b300e8506835ba1b8990
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627807"
---
# <a name="or-function"></a>OR Function

Gibt TRUE (1) zurück, wenn einer der logischen Ausdrücke, die als Parameter übergeben werden, TRUE ist.
  
## <a name="syntax"></a>Syntax

OR(** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* ** ) 
  
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

OR(Height \> 1,PinX \> 1) 
  
Gibt TRUE (1) zurück, wenn mindestens einer der beiden Ausdrücke TRUE ist. Gibt FALSE (0) zurück, wenn beide Ausdrücke FALSE sind. 
  

