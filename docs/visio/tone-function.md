---
title: TONE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Ändert die Farbe, indem die Sättigung um den im int-Parameter angegebenen Wert verringert wird.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434375"
---
# <a name="tone-function"></a>TONE Function

Ändert die Farbe, indem die Sättigung um den im  _int-Parameter_ angegebenen Wert verringert wird. 
  
## <a name="syntax"></a>Syntax

TONE(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.  <br/> |
| _int_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Wert, um den die Farbsättigung verringert werden soll. Kann positiv oder negativ sein.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **RGB**
  
## <a name="remarks"></a>Hinweise

Die unteren und oberen Grenzwerte der Sättigung liegen jeweils bei 0 und 240. Es gibt keine Beschränkung für die Größe der ganzen Zahl, die Sie für den  _int-Parameter_ übergeben können, aber die Sättigung überschreitet diese Grenzwerte nie. 
  

