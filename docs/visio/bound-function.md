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
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425960"
---
# <a name="bound-function"></a>BOUND Function

Schränkt den Wert einer Zelle auf einen oder mehrere Bereiche ein.
  
## <a name="syntax"></a>Syntax

BOUND (** *value* **, ** *type* **, ** *ignore* **, ** *value1* **, ** *value2* ** ** [,ignore(n), value1(n), value2(n),...] * ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der aktuelle einzuschränkende Wert.  <br/> |
| _Typ_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Gibt an, ob die Einschränkung einschließend (0), ausschließend (1) oder deaktiviert (2) ist.  <br/> |
| _ignore_ <br/> |Erforderlich  <br/> |**Boolean** <br/> | TRUE, um den Bereich zu ignorieren; FALSE, um den Wert der Zelle auf den Bereich zu beschränken.  <br/> |
| _value1_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Erster Wert in einem Bereich.  <br/> |
| _value2_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Zweiter Wert in einem Bereich.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie die BOUND-Funktion, um den Wert einer Zelle auf eine obere und untere Grenze zu beschränken, z. B. um Objekte zu steuern, die nicht über oder unter einer minimalen oder maximalen Höhe gestreckt werden sollten. Die Einschränkung kann in Bezug auf den Bereich oder die Bereiche einschließlich oder exklusiv sein. Wenn der aktuelle Wert nicht eingeschränkt werden soll, legen Sie den  _Type-Parameter_ auf 2 (deaktiviert) festgelegt. 
  
Sie können mehrere Bereiche definieren, indem Sie mehrere Vorkommen der  _Parameter ignore_,  _value1_ und  _value2_ angeben. Verwenden Sie den  _Ignore-Parameter,_ um Einschränkungen durch einen bestimmten Bereich zu deaktivieren. 
  
Die Formel, die die BOUND-Funktion enthält, wird nicht überschrieben, wenn sich ihr Wert ändert. stattdessen wird die Formel beibehalten, und der neue Wert wird in den  _Value-Parameter_ platziert. 
  
## <a name="example-1"></a>Beispiel 1

In diesem Beispiel wird mit der BOUND-Funktion erzwungen, dass ein Steuerpunkt nicht die Grenzen eines Shape-Felds verlässt. 
  
Controls.X1 = BOUND(Width \* 0.5, 0, FALSE, Width \* 0, Width \* 1)
  
Controls.Y1 = BOUND(Height \* 0.5, 0, FALSE, Height \* 0, Height \* 1)
  
## <a name="example-2"></a>Beispiel 2

In diesem Beispiel wird mit der BOUND-Funktion die Breite eines Shapes auf 2 Zoll (inches), 4 Zoll oder 6 Zoll beschränkt. 
  
Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)
  

