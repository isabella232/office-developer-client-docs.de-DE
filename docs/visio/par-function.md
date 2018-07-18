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
description: Gibt die X, y-Koordinaten eines Punkts im Koordinatensystem des übergeordneten Shapes zurück.
ms.openlocfilehash: a3f7afd3f9bc988a20526451a6d7d7081d27a2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797598"
---
# <a name="par-function"></a>PAR Function

Gibt die _X, y_ -Koordinaten eines Punkts im Koordinatensystem des übergeordneten Shapes zurück. 
  
## <a name="syntax"></a>Syntax

PAR (** *zeigen* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Punkt_ <br/> |Erforderlich  <br/> |**Number, Number** <br/> |Die Koordinaten des Punkts im Koordinatensystem des aktuellen Shapes.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

In Microsoft Visio ist ein Punkt einen single-Wert, der verkörpert ein Paar von *X* - und *y* -Koordinaten. Wenn das Shape in einer Gruppe ist, ist die übergeordnete Gruppe. Wenn das Shape nicht in einer Gruppe ist, ist die übergeordnete der Seite. 
  
## <a name="example"></a>Beispiel

PAR(PNT(PinX,PinY)) 
  
In diesem Ausdruck konvertiert PKT ein Koordinatenpaar im aktuellen Shape in einen Punkt. PAR konvertiert den Punkt anschließend in ein Koordinatenpaar in Relation zu unteren linken Ecke des Zeichenblatts oder der Gruppe, in dem/der das aktuelle Shape enthalten ist. 
  

