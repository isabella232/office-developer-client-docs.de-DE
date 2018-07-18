---
title: TIME Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Gibt die Uhrzeit als Stunden, Minuten und Sekunden.
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798290"
---
# <a name="time-function-visioshapesheet"></a>TIME Function (VisioShapeSheet)

Gibt die Zeit, die durch _Stunde_, _Minute_und _Sekunde_dargestellt.
  
## <a name="syntax"></a>Syntax

Zeit (** *Stunde* **, ** *Minute* **, ** *zweiten* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die Stundenkomponente.  <br/> |
| _minute_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die Minutenkomponente.  <br/> |
| _second_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die Sekundenkomponente.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Numeric
  
## <a name="example-1"></a>Beispiel 1

TIME(15,30,30)
  
Gibt den Wert für 15:30:30 zurück.
  
## <a name="example-2"></a>Beispiel 2

FORMAT(ZEIT(15,30,30),"HH:mm")
  
Gibt den Wert für 15:30 zurück.
  
## <a name="example-3"></a>Beispiel 3

TIME(15,30,30) + 8 vs.
  
Gibt den Wert für 23:30:30 zurück.
  

