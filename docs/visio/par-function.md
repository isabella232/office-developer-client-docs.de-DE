---
title: PAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Gibt die XY-Koordinaten eines Punkts im Koordinatensystem des übergeordneten Shapes zurück.
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414508"
---
# <a name="par-function"></a>PAR Function

Gibt die  _XY-Koordinaten_ eines Punkts im Koordinatensystem des übergeordneten Shapes zurück. 
  
## <a name="syntax"></a>Syntax

PAR(** *point* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |Erforderlich  <br/> |**Number, Number** <br/> |Die Koordinaten des Punkts im Koordinatensystem des aktuellen Shapes.  <br/> |
   
## <a name="remarks"></a>Hinweise

In Microsoft Visio ist ein Punkt ein einzelner Wert, der ein Paar *x-* und *y-Koordinaten* verkörpert. Wenn sich das Shape in einer Gruppe befindet, ist das übergeordnete Element die Gruppe. Befindet sich das Shape nicht in einer Gruppe, ist das übergeordnete Element das Zeichenblatt. 
  
## <a name="example"></a>Beispiel

PAR(PNT(PinX,PinY)) 
  
In diesem Ausdruck konvertiert PKT ein Koordinatenpaar im aktuellen Shape in einen Punkt. PAR konvertiert den Punkt anschließend in ein Koordinatenpaar in Relation zu unteren linken Ecke des Zeichenblatts oder der Gruppe, in dem/der das aktuelle Shape enthalten ist. 
  

