---
title: TINT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Ändert die Farbe, indem deren Helligkeit um den Wert (positiven oder negativen) im Int-Parameter angegeben.
ms.openlocfilehash: a4b15596a4742edb4f9e4746929f19d2eafe94d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798288"
---
# <a name="tint-function"></a>TINT-Funktion

Ändert die Farbe, indem deren Helligkeit um den Wert (positiven oder negativen) im _Int_ -Parameter angegeben. 
  
## <a name="syntax"></a>Syntax

FARBTON (** *Farbe* **, ** *Int* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Farbe_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.  <br/> |
| _int_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Wert, um den die Leuchtdichte der Farbe erhöht werden soll. Kann positiv oder negativ sein.
  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

 **RGB**
  
## <a name="remarks"></a>Bemerkungen

Die unteren und oberen Grenzwerte der Helligkeit sind 0 und 240. Es gibt keine Beschränkung der Größe von die ganze Zahl, die Sie für den Parameter _Int_ weitergeben können, aber Helligkeit überschreitet nie diese Grenzwerte. 
  

