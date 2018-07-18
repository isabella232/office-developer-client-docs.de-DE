---
title: NOW Function (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Gibt den aktuellen Wert für Datum und Uhrzeit zurück.
ms.openlocfilehash: 387425369b1f1d6313502b3679a72cfd23038834
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797577"
---
# <a name="now-function-visioshapesheet"></a>NOW Function (VisioShapeSheet)

Gibt den aktuellen Wert für Datum und Uhrzeit zurück.
  
## <a name="syntax"></a>Syntax

NOW ( )
  
### <a name="return-value"></a>R�ckgabewert

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
  

