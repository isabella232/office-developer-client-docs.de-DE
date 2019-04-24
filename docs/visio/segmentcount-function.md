---
title: SEGMENTCOUNT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Gibt die Anzahl der Liniensegmente zurück, aus denen der Pfad besteht.
ms.openlocfilehash: 947e37c13de638e4f281bc17376a253a8ca07e04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326040"
---
# <a name="segmentcount-function"></a>SEGMENTCOUNT Function

Gibt die Anzahl der Liniensegmente zurück, aus denen der Pfad besteht.
  
## <a name="syntax"></a>Syntax

Segment count (* * *pathRef* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _pathRef_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf die Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Liniensprünge sind in der Gesamtzahl der zurückgegebenen Segmente nicht eingeschlossen.
  

