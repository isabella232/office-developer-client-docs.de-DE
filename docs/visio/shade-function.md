---
title: SHADE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Ändert die Farbe durch Verringern der Helligkeit um den Betrag (positiven oder negativen) im Int-Parameter angegebene.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382981"
---
# <a name="shade-function"></a>SHADE Function

Ändert die Farbe durch Verringern der Helligkeit um den Betrag (positiven oder negativen) im _Int_ -Parameter angegebene. 
  
## <a name="syntax"></a>Syntax

SCHATTEN (** *Farbe* **, ** *Int* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Farbe_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.  <br/> |
| _int_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Wert, um den die Leuchtdichte der Farbe verringert werden soll. Kann positiv oder negativ sein.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **RGB**
  
## <a name="remarks"></a>Hinweise

Die unteren und oberen Grenzwerte der Helligkeit sind 0 und 240. Es gibt keine Beschränkung der Größe von die ganze Zahl, die Sie für den Parameter _Int_ weitergeben können, aber Helligkeit überschreitet nie diese Grenzwerte. 
  
![Unteren und oberen Grenzwerte der Helligkeit](media/image199_ZA10173627.gif)
  

