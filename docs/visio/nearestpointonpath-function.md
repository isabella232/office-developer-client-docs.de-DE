---
title: NEARESTPOINTONPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Gibt den Prozentsatz des Abstands entlang des Pfads des Punkts zurück, der den angegebenen Koordinaten am nächsten liegt, wie einen Wert zwischen 0 und 1.
ms.openlocfilehash: 29c5dac690913c1b3715f18c4a661991ea4c23aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608228"
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
| _x_ <br/> |Erforderlich  <br/> |**Double** <br/> |Die X-Koordinate des angegebenen Punkts.  <br/> |
| _y_ <br/> |Erforderlich  <br/> |**Double** <br/> |Die y-Koordinate des angegebenen Punkts.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Double**
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn _kein Abschnitt_ vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  

