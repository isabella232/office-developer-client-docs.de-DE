---
title: PATHSEGMENT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Gibt die 1-basierte Segmentnummer an der angegebenen prozentualen Markierung entlang des angegebenen Pfads zurück.
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432485"
---
# <a name="pathsegment-function"></a>PATHSEGMENT Function

Gibt die 1-basierte Segmentnummer an der angegebenen prozentualen Markierung entlang des angegebenen Pfads zurück.
  
## <a name="syntax"></a>Syntax

PATHSEGMENT (* * *section* * *, * * *Reise* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _Reise_ <br/> |Erforderlich  <br/> |**Double** <br/> |Der Prozentsatz entlang des durchlaufenen Pfads vom Anfangs- zum Endpunkt. Muss zwischen 0 und 1 liegen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  

