---
title: DISTTOPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Gibt den kürzesten Abstand von dem von den angegebenen Koordinaten festgelegten Punkt zu einem Punkt im Pfad zurück.
ms.openlocfilehash: f6e0bae491b148c16ae4e0f87edd02cc9d4b9f9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586544"
---
# <a name="disttopath-function"></a>DISTTOPATH Function

Gibt den kürzesten Abstand von dem von den angegebenen Koordinaten festgelegten Punkt zu einem Punkt im Pfad zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

DISTTOPATH(** *section* **, ** *x* **, ** *y* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _x_ <br/> |Erforderlich  <br/> |**Double** <br/> |Die X-Koordinate des Punkts.  <br/> |
| _y_ <br/> |Erforderlich  <br/> |**Double** <br/> |Die y-Koordinate des Punkts.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Double**
  
## <a name="remarks"></a>HinwBemerkungeneise

Microsoft Visio gibt #REF! wenn  _kein Abschnitt_ vorhanden ist. 
  
Der Rückgabewert ist positiv, wenn sich der Punkt links der Laufrichtung befindet; er ist positiv, wenn sich der Punkt rechts der Laufrichtung befindet.
  

