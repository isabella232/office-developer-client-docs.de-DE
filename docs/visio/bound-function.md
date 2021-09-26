---
title: BOUND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
ms.localizationpriority: medium
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Schränkt den Wert einer Zelle auf einen oder mehrere Bereiche ein.
ms.openlocfilehash: 0190ae3b3066ffc15232574c83719b732bedc2a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613114"
---
# <a name="bound-function"></a>BOUND Function

Schränkt den Wert einer Zelle auf einen oder mehrere Bereiche ein.
  
## <a name="syntax"></a>Syntax

BOUND (** *wert* **, ** *type* **, ** *ignore* **, ** *value1* **, ** *value2* ** ** * [,ignore(n), value1(n), value2(n),...] * ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der aktuelle einzuschränkende Wert.  <br/> |
| _Typ_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Gibt an, ob die Einschränkung einschließend (0), ausschließend (1) oder deaktiviert (2) ist.  <br/> |
| _Ignorieren_ <br/> |Erforderlich  <br/> |**Boolean** <br/> | TRUE, um den Bereich zu ignorieren; FALSE, um den Wert der Zelle auf den Bereich zu beschränken.  <br/> |
| _Wert1_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Erster Wert in einem Bereich.  <br/> |
| _Wert2_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Zweiter Wert in einem Bereich.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die BOUND-Funktion, um den Wert einer Zelle auf eine obere und untere Grenze zu beschränken, z. B. um Objekte zu steuern, die nicht über oder unter einer minimalen oder maximalen Höhe gestreckt werden sollen. Die Einschränkung kann inklusiv oder exklusiv in Bezug auf den Bereich oder die Bereiche sein. Wenn der aktuelle Wert nicht eingeschränkt werden soll, legen Sie den  _Typparameter_ auf 2 (deaktiviert) fest. 
  
Sie können mehrere Bereiche definieren, indem Sie mehrere Vorkommen der Parameter  _ignore_,  _value1_ und  _value2_ angeben. Verwenden Sie den Parameter  _ignore,_ um Einschränkungen für einen bestimmten Bereich zu deaktivieren. 
  
Die Formel, die die BOUND-Funktion enthält, wird nicht überschrieben, wenn sich ihr Wert ändert. Stattdessen wird die Formel beibehalten, und der neue Wert wird in den  _Wertparameter_ eingefügt. 
  
## <a name="example-1"></a>Beispiel 1

In diesem Beispiel wird mit der BOUND-Funktion erzwungen, dass ein Steuerpunkt nicht die Grenzen eines Shape-Felds verlässt. 
  
Controls.X1 = BOUND(Width \* 0.5, 0, FALSE, Width \* 0, Width \* 1)
  
Controls.Y1 = BOUND(Height \* 0.5, 0, FALSE, Height \* 0, Height \* 1)
  
## <a name="example-2"></a>Beispiel 2

In diesem Beispiel wird mit der BOUND-Funktion die Breite eines Shapes auf 2 Zoll (inches), 4 Zoll oder 6 Zoll beschränkt. 
  
Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)
  

