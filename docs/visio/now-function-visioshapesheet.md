---
title: NOW-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Gibt den aktuellen Datums- und Uhrzeitwert zurück.
ms.openlocfilehash: 9e28f51b0e1d1c09a70e54e432a865968c721940
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414081"
---
# <a name="now-function-visioshapesheet"></a>NOW-Funktion (VisioShapeSheet)

Gibt den aktuellen Datums- und Uhrzeitwert zurück.
  
## <a name="syntax"></a>Syntax

NOW ( )
  
### <a name="return-value"></a>Rückgabewert

Datetime
  
## <a name="remarks"></a>Hinweise

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
  

