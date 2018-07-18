---
title: TONE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Ändert die Farbe durch verringern die Sättigung entsprechend der Angabe in der Int-Parameter.
ms.openlocfilehash: be89764c849299288963c272f8ffb2d5d728f270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798298"
---
# <a name="tone-function"></a>TONE Function

Ändert die Farbe durch verringern die Sättigung entsprechend der Angabe in der _Int_ -Parameter. 
  
## <a name="syntax"></a>Syntax

TONE (** *Farbe* **, ** *Int* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Farbe_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.  <br/> |
| _int_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Wert, um den die Farbsättigung verringert werden soll. Kann positiv oder negativ sein.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

 **RGB**
  
## <a name="remarks"></a>Bemerkungen

Die unteren und oberen Grenzwerte der Sättigung sind 0 und 240. Es gibt keine Beschränkung der Größe von die ganze Zahl, die Sie für den Parameter _Int_ weitergeben können, aber Sättigung überschreitet nie diese Grenzwerte. 
  

