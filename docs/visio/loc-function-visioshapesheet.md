---
title: LOC Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Nimmt einen Punkt in lokalen Koordinaten eine Form definiert und gibt den entsprechenden Punkt, der in den lokalen Koordinaten des mit der Formel verknüpften Shapes ausgedrückt.
ms.openlocfilehash: 196e2c92ea6ab410b6ecca9767b68605e4eb4d30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797361"
---
# <a name="loc-function-visioshapesheet"></a>LOC Function (VisioShapeSheet)

Nimmt einen Punkt in lokalen Koordinaten eine Form definiert und gibt den entsprechenden Punkt, der in den lokalen Koordinaten des mit der Formel verknüpften Shapes ausgedrückt. 
  
## <a name="syntax"></a>Syntax

LOC (** *zeigen* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zeigen Sie_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Punkt, der in den lokalen Koordinaten eines Shapes definiert ist.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

String
  
## <a name="remarks"></a>Bemerkungen

Lokale Koordinaten werden von der unteren linken Ecke des Auswahlrechtecks eines Shapes gemessen. Beide Shapes müssen sich auf demselben Zeichenblatt befinden.
  
## <a name="example"></a>Beispiel

LOC (Pkt (Sheet.5! LocPinX, Sheet.5! LocPinY)) 
  
In diesem Ausdruck konvertiert PKT ein Paar lokaler Koordinaten in Sheet.5 in einen Punkt. (Bei Sheet.5 handelt es sich um ein weiteres Shape auf demselben Zeichenblatt.) LOC konvertiert diesen Punkt dann in einen äquivalenten Punkt in dem lokalen Koordinatensystem des aktuellen Shapes - relativ zur unteren linken Ecke des Auswahlrechtecks des aktuellen Shapes. 
  
Die 5 in Sheet.5 ist die ID-Nummer für die Form, die im Dialogfeld **Shape-Name** (Registerkarte**Entwickler** ) angezeigt wird. 
  

