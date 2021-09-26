---
title: NOW-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
ms.localizationpriority: medium
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Gibt den aktuellen Datums- und Uhrzeitwert zurück.
ms.openlocfilehash: 6ec4069334a4a11588d015b6b134926c75613188
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627863"
---
# <a name="now-function-visioshapesheet"></a>NOW-Funktion (VisioShapeSheet)

Gibt den aktuellen Datums- und Uhrzeitwert zurück.
  
## <a name="syntax"></a>Syntax

NOW ( )
  
### <a name="return-value"></a>Rückgabewert

Datetime
  
## <a name="remarks"></a>Bemerkungen

NOW wird in Abständen von einer Minute jeweils neu berechnet. 
  
## <a name="example-1"></a>Beispiel 1

NOW( )
  
Gibt das aktuelle Datum und die aktuelle Uhrzeit zurück, z. B. 27.9.2010 12:03:30.
  
## <a name="example-2"></a>Beispiel 2

FORMAT(JETZT(),"tt MMM. jjjj hh:mm")
  
Gibt das aktuelle Datum und die aktuelle Uhrzeit zurück, formatiert als 27 Sep. 2010 12:03.
  
## <a name="example-3"></a>Beispiel 3

NOW()+2EW.
  
Gibt das aktuelle Datum und die aktuelle Uhrzeit plus zwei vergangene Wochen zurück, z. B. 11.10.10 12:03:30.
  

