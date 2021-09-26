---
title: PAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
ms.localizationpriority: medium
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Gibt die X,Y-Koordinaten eines Punkts im Koordinatensystem des übergeordneten Shapes zurück.
ms.openlocfilehash: b3ac20694b7ee2c4031c86a52f7c631685fb8b70
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627744"
---
# <a name="par-function"></a>PAR Function

Gibt die  _X,Y-Koordinaten_ eines Punkts im Koordinatensystem des übergeordneten Shapes zurück. 
  
## <a name="syntax"></a>Syntax

PAR(** *Punkt* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Punkt_ <br/> |Erforderlich  <br/> |**Number, Number** <br/> |Die Koordinaten des Punkts im Koordinatensystem des aktuellen Shapes.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

In Microsoft Visio ist ein Punkt ein einzelner Wert, *der* ein Paar x- und *y-Koordinaten* darstellt. Wenn sich das Shape in einer Gruppe befindet, ist das übergeordnete Element die Gruppe. Befindet sich das Shape nicht in einer Gruppe, ist das übergeordnete Element das Zeichenblatt. 
  
## <a name="example"></a>Beispiel

PAR(PNT(PinX,PinY)) 
  
In diesem Ausdruck konvertiert PKT ein Koordinatenpaar im aktuellen Shape in einen Punkt. PAR konvertiert den Punkt anschließend in ein Koordinatenpaar in Relation zu unteren linken Ecke des Zeichenblatts oder der Gruppe, in dem/der das aktuelle Shape enthalten ist. 
  

