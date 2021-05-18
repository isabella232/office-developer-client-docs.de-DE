---
title: NEARESTPOINTONPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Gibt den Prozentsatz des Abstands entlang des Pfads des Punkts zurück, der den angegebenen Koordinaten am nächsten liegt, wie einen Wert zwischen 0 und 1.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407333"
---
# <a name="nearestpointonpath-function"></a>NEARESTPOINTONPATH Function

Gibt den Prozentsatz des Abstands entlang des Pfads des Punkts zurück, der den angegebenen Koordinaten am nächsten liegt, wie einen Wert zwischen 0 und 1.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

NEARESTPOINTONPATH(** *section* **, ** *x* **, ** *y* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _x_ <br/> |Erforderlich  <br/> |**Double** <br/> |Die x-Koordinate des angegebenen Punkts.  <br/> |
| _y_ <br/> |Erforderlich  <br/> |**Double** <br/> |Die y-Koordinate des angegebenen Punkts.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Double**
  
## <a name="remarks"></a>Hinweise

Wenn _der_ Abschnitt nicht vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  

