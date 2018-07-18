---
title: LOCTOPAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: Gibt einen transformierten Punkt in übergeordneten Koordinaten im Zielkoordinatensystem zurück.
ms.openlocfilehash: 7d882ec34de93db2828fc751f99d87fc3e961d64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797436"
---
# <a name="loctopar-function"></a>LOCTOPAR Function

Gibt einen transformierten Punkt in übergeordneten Koordinaten im Zielkoordinatensystem zurück.
  
## <a name="syntax"></a>Syntax

LOCTOPAR (** *Quellpunkt* **, ** *SrcRef* **, ** *Zielbezug* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Quellpunkt_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Punkt in den lokalen Koordinaten des Quellkoordinatensystems.  <br/> |
| _srcRef_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Bezug auf eine Zelle im Quellobjekt.  <br/> |
| _Zielbezug_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Bezug auf eine Zelle im Zielobjekt.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Die Funktion konvertiert einen Punkt aus lokalen Koordinaten in einem Quell-Shape in die übergeordneten Koordinaten eines Ziel-Shapes. Sie können die Funktion LOCTOPAR verwenden, um übergeordnete Koordinaten in Zellen eines Shapes, wie z.B. PinX, PinY, BeginX und BeginY festzulegen und dabei einen anderen Punkt von einem anderen Koordinatensystem zu verwenden. 
  
Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst. 
  
Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt liegen. 
  
Wenn das Ziel ein Zeichenblatt ohne übergeordnetes Objekt ist, wird das Ergebnis in den lokalen Koordinaten des Zeichenblatts ausgedrückt. 
  
## <a name="example"></a>Beispiel

LOCTOPAR(PKT(LokDrehbezX, LokDrehbezY), Breite, Sheet.4!Breite) 
  
Konvertiert den lokalen Drehpunkt des Shapes, die mit der Formel verknüpft ist, in die übergeordneten Koordinaten von Sheet.4. 
  

