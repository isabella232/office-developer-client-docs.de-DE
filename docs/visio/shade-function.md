---
title: SHADE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Ändert die Farbe durch Verringern der Helligkeit um den Betrag (positiven oder negativen) im Int-Parameter angegebene.
ms.openlocfilehash: 4a02aa41050c3cf36b567c238670b5f61074bd7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798002"
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
   
### <a name="return-value"></a>R�ckgabewert

 **RGB**
  
## <a name="remarks"></a>Bemerkungen

Die unteren und oberen Grenzwerte der Helligkeit sind 0 und 240. Es gibt keine Beschränkung der Größe von die ganze Zahl, die Sie für den Parameter _Int_ weitergeben können, aber Helligkeit überschreitet nie diese Grenzwerte. 
  
![](media/image199_ZA10173627.gif)
  

