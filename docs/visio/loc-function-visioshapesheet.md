---
title: LOC-Funktion(VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Akzeptiert einen Punkt, der in den lokalen Koordinaten eines Shapes definiert ist, und gibt den entsprechenden Punkt in den lokalen Koordinaten der Form zurück, die der Formel zugeordnet ist.
ms.openlocfilehash: 4728e5f8301c6ef10ddb0c14b6c0868a7a48b2a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344429"
---
# <a name="loc-function-visioshapesheet"></a>LOC-Funktion(VisioShapeSheet)

Akzeptiert einen Punkt, der in den lokalen Koordinaten eines Shapes definiert ist, und gibt den entsprechenden Punkt in den lokalen Koordinaten der Form zurück, die der Formel zugeordnet ist. 
  
## <a name="syntax"></a>Syntax

LOC (* * *Point* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Punkt_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Punkt, der in den lokalen Koordinaten eines Shapes definiert ist.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Lokale Koordinaten werden von der unteren linken Ecke des Auswahlrechtecks eines Shapes gemessen. Beide Shapes müssen sich auf demselben Zeichenblatt befinden.
  
## <a name="example"></a>Beispiel

LOC (PNT (Blatt. 5! Zelle LocPinX, Sheet. 5! Zelle LocPinY)) 
  
In diesem Ausdruck konvertiert PKT ein Paar lokaler Koordinaten in Sheet.5 in einen Punkt. (Bei Sheet.5 handelt es sich um ein weiteres Shape auf demselben Zeichenblatt.) LOC konvertiert diesen Punkt dann in einen äquivalenten Punkt in dem lokalen Koordinatensystem des aktuellen Shapes - relativ zur unteren linken Ecke des Auswahlrechtecks des aktuellen Shapes. 
  
Die 5 in Sheet.5 ist die ID für das Shape, das im Dialogfeld **Shape-Name** (Registerkarte **Entwickler**) angezeigt wird. 
  

