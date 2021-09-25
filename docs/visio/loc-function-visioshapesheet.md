---
title: LOC-Funktion(VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
ms.localizationpriority: medium
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Nimmt einen in den lokalen Koordinaten eines Shapes definierten Punkt an und gibt den entsprechenden Punkt zurück, der in den lokalen Koordinaten des der Formel zugeordneten Shapes ausgedrückt wird.
ms.openlocfilehash: 82a399a3e50aa94a9d158260bd9292a026af4017
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565975"
---
# <a name="loc-function-visioshapesheet"></a>LOC-Funktion(VisioShapeSheet)

Nimmt einen in den lokalen Koordinaten eines Shapes definierten Punkt an und gibt den entsprechenden Punkt zurück, der in den lokalen Koordinaten des der Formel zugeordneten Shapes ausgedrückt wird. 
  
## <a name="syntax"></a>Syntax

LOC(** *point* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Punkt_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Punkt, der in den lokalen Koordinaten eines Shapes definiert ist.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>HinwBemerkungeneise

Lokale Koordinaten werden von der unteren linken Ecke des Auswahlrechtecks eines Shapes gemessen. Beide Shapes müssen sich auf demselben Zeichenblatt befinden.
  
## <a name="example"></a>Beispiel

LOC(PNT(Sheet.5! LocPinX, Sheet.5! LocPinY)) 
  
In diesem Ausdruck konvertiert PKT ein Paar lokaler Koordinaten in Sheet.5 in einen Punkt. (Bei Sheet.5 handelt es sich um ein weiteres Shape auf demselben Zeichenblatt.) LOC konvertiert diesen Punkt dann in einen äquivalenten Punkt in dem lokalen Koordinatensystem des aktuellen Shapes - relativ zur unteren linken Ecke des Auswahlrechtecks des aktuellen Shapes. 
  
Die 5 in Sheet.5 ist die ID für das Shape, das im Dialogfeld **Shape-Name** (Registerkarte **Entwickler**) angezeigt wird. 
  

