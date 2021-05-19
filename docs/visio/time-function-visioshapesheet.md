---
title: TIME-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Gibt die Durch Stunde, Minute und Sekunde dargestellte Zeit zurück.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414473"
---
# <a name="time-function-visioshapesheet"></a>TIME-Funktion (VisioShapeSheet)

Gibt die Durch _Stunde,_ Minute und Sekunde dargestellte Zeit _zurück._ 
  
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
  

