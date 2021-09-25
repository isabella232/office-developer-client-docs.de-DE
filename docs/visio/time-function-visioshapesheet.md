---
title: TIME-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
ms.localizationpriority: medium
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Gibt die Uhrzeit zurück, die durch Stunde, Minute und Sekunde dargestellt wird.
ms.openlocfilehash: 4df859721e4947ba625a473f391d9e81f5606b2e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622746"
---
# <a name="time-function-visioshapesheet"></a>TIME-Funktion (VisioShapeSheet)

Gibt die Uhrzeit zurück, die durch  _Stunde,_  _Minute_ und  _Sekunde_ dargestellt wird.
  
## <a name="syntax"></a>Syntax

TIME(** *hour* **, ** *minute* **, ** *second* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die Stundenkomponente.  <br/> |
| _minute_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die Minutenkomponente.  <br/> |
| _second_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die Sekundenkomponente.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Numeric
  
## <a name="example-1"></a>Beispiel 1

TIME(15,30,30)
  
Gibt den Wert für 15:30:30 zurück.
  
## <a name="example-2"></a>Beispiel 2

FORMAT(TIME(15,30,30),"HH:mm")
  
Gibt den Wert für 15:30 zurück.
  
## <a name="example-3"></a>Beispiel 3

TIME(15,30,30) + 8 vs.
  
Gibt den Wert für 23:30:30 zurück.
  

