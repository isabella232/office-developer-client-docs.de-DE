---
title: FLOOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Rundet eine Zahl in Richtung 0 (Null), zur nächsten ganzen Zahl oder zur nächsten Instanz von mehreren.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439898"
---
# <a name="floor-function"></a>FLOOR Function

Rundet eine Zahl in Richtung 0 (Null), zur nächsten ganzen Zahl oder zur nächsten Instanz von _mehreren ._
  
## <a name="syntax"></a>Syntax

FLOOR(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die zu rundende Zahl.  <br/> |
| _multiple_ <br/> |Erforderlich  <br/> |**Number** <br/> |Das Vielfache, auf das gerundet werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Nummer
  
## <a name="remarks"></a>Hinweise

Wenn  _nicht multiple_ angegeben ist, wird die Zahl in Richtung 0 zur nächsten ganzen Zahl gerundet. 
  
 _Zahl_ und  _Vielfaches_ müssen die gleichen Zeichen haben, oder ein #NUM! zurückgegeben. Wenn eine  _Zahl oder_  _ein Vielfaches_ nicht in einen Wert konvertiert werden kann, wird #VALUE! zurückgegeben. Wenn zahl  _oder_  _mehrfach_ 0 ist, ist das Ergebnis 0. 
  
## <a name="example-1"></a>Beispiel 1

FLOOR(3.7)
  
Gibt 3 zurück.
  
## <a name="example-2"></a>Beispiel 2

FLOOR(-3.7)
  
Gibt -3 zurück.
  
## <a name="example-3"></a>Beispiel 3

FLOOR(3.7, 0.5)
  
Gibt 3,5 zurück.
  

