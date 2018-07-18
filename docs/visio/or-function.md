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
description: Gibt TRUE (1) zurück, wenn einer der logischen Ausdrücke als Parameter übergebene wahr sind.
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797571"
---
# <a name="or-function"></a>OR Function

Gibt TRUE (1) zurück, wenn einer der logischen Ausdrücke als Parameter übergebene wahr sind.
  
## <a name="syntax"></a>Syntax

ODER (** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *LogicalexpressionN* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |Erforderlich  <br/> |**String** <br/> |Der erste Ausdruck, dessen Wahrheit ausgewertet werden soll.  <br/> |
| _logicalexpression2_ <br/> |Erforderlich  <br/> |**String** <br/> |Der zweite Ausdruck, dessen Wahrheit ausgewertet werden soll.  <br/> |
| _logicalexpressionN_ <br/> |Erforderlich  <br/> |**String** <br/> |Der n-te Ausdruck, dessen Wahrheit ausgewertet werden soll.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Boolean
  
## <a name="remarks"></a>Bemerkungen

Ein beliebiger Ausdruck, der einen Wert ungleich Null ergibt, wird als TRUE betrachtet. Wenn alle logischen Ausdrücke den Wert FALSE oder 0 aufweisen, gibt die Funktion FALSE zurück. 
  
## <a name="example"></a>Beispiel

ODER (Höhe \> 1, DrehbezX \> 1) 
  
Gibt TRUE (1) zurück, wenn mindestens einer der beiden Ausdrücke TRUE ist. Gibt FALSE (0) zurück, wenn beide Ausdrücke FALSE sind. 
  

