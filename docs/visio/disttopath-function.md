---
title: DISTTOPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Gibt den kürzesten Abstand von dem von den angegebenen Koordinaten festgelegten Punkt zu einem Punkt im Pfad zurück.
ms.openlocfilehash: 227fe860de2e3683b5d7d3e5f9313d1e2e31b2d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796878"
---
# <a name="disttopath-function"></a>DISTTOPATH Function

Gibt den kürzesten Abstand von dem von den angegebenen Koordinaten festgelegten Punkt zu einem Punkt im Pfad zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

DISTTOPATH (** *Abschnitt* **, ** *X* **, ** *y* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _x_ <br/> |Erforderlich  <br/> |**Double** <br/> |Die _X_-Koordinate des Punkts.  <br/> |
| _y_ <br/> |Erforderlich  <br/> |**Double** <br/> |Die _y_-Koordinate des Punkts.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

 **Double**
  
## <a name="remarks"></a>Bemerkungen

Microsoft Visio gibt #REF! Wenn _Section_ nicht vorhanden ist. 
  
Der Rückgabewert ist positiv, wenn sich der Punkt links der Laufrichtung befindet; er ist positiv, wenn sich der Punkt rechts der Laufrichtung befindet.
  

