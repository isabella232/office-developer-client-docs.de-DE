---
title: BOUND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Schränkt den Wert einer Zelle auf einen oder mehrere Bereiche ein.
ms.openlocfilehash: 2f6228828fee8fa1831bb0d3a714fca068808652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796572"
---
# <a name="bound-function"></a>BOUND Function

Schränkt den Wert einer Zelle auf einen oder mehrere Bereiche ein.
  
## <a name="syntax"></a>Syntax

GEBUNDEN (** *Wert* **, ** *Typ* **, ** *ignorieren* **, ** *Wert1* **, ** *value2* ** ** * [, ignore(n), value1(n), value2(n),...] * **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Value_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Der aktuelle einzuschränkende Wert.  <br/> |
| _Typ_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Gibt an, ob die Einschränkung einschließend (0) ist ausschließend (1) oder deaktiviert (2).  <br/> |
| _ignorieren_ <br/> |Erforderlich  <br/> |**Boolean** <br/> | True, um den Bereich zu ignorieren. Legen Sie false fest, um den Wert der Zelle auf den Bereich einzuschränken.  <br/> |
| _Wert1_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Erster Wert in einem Bereich.  <br/> |
| _Wert2_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Zweiter Wert in einem Bereich.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden der BOUND-Funktion zum Einschränken der Wert auf eine obere und die untere Grenze, beispielsweise einer Zelle, um Objekte zu steuern, die nicht über oder unter eine minimale oder maximale Höhe gedehnt werden sollten. Die Einschränkung kann inklusive oder exklusive in Bezug auf den Bereich oder die Bereiche. Wenn der aktuelle Wert nicht eingeschränkt werden soll, legen Sie den Parameter _Type_ auf 2 (deaktiviert). 
  
Sie können mehrere Bereiche definieren, indem der Parameter _ignore_, _value1_und _value2_ mehrere Vorkommen. Verwenden Sie den Parameter _ignorieren_ , um Einschränkungen durch einen bestimmten Bereich deaktivieren. 
  
Die Formel, die mit der BOUND-Funktion ist nicht überschrieben, wenn der Wert geändert wird; stattdessen die Formel wird beibehalten, und der neue Wert wird in der _Value_ -Parameter eingefügt. 
  
## <a name="example-1"></a>Beispiel 1

In diesem Beispiel wird mit der BOUND-Funktion erzwungen, dass ein Steuerpunkt nicht die Grenzen eines Shape-Felds verlässt. 
  
Controls.X1 = Grenze (Breite\*0,5, 0, FALSE, Breite\*0, Breite\*1)
  
Controls.Y1 = Grenze (Höhe\*0,5, 0, FALSE, Height\*0, Höhe\*1)
  
## <a name="example-2"></a>Beispiel 2

In diesem Beispiel wird mit der BOUND-Funktion die Breite eines Shapes auf 2 Zoll (inches), 4 Zoll oder 6 Zoll beschränkt. 
  
Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)
  

