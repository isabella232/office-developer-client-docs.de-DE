---
title: TONE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Ändert die Farbe, indem die Sättigung um den im int-Parameter angegebenen Wert verringert wird.
ms.openlocfilehash: 2ea8e6af43fe199e9c7bff18d1120b1e24d08eca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627275"
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
  
## <a name="remarks"></a>Bemerkungen

Die unteren und oberen Grenzwerte der Sättigung liegen jeweils bei 0 und 240. Es gibt keine Beschränkung für die Größe der ganzen Zahl, die Sie für den  _int-Parameter_ übergeben können, aber die Sättigung überschreitet diese Grenzwerte niemals. 
  

