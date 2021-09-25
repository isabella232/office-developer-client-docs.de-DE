---
title: NOT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
ms.localizationpriority: medium
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Gibt TRUE (1) zurück, wenn Logicalexpression FALSE ist. Andernfalls wird FALSE (0) zurückgegeben.
ms.openlocfilehash: 54e4f85845546c2a6a511d8831a834c2cc9a0fd7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608214"
---
# <a name="not-function"></a>NOT Function

Gibt TRUE (1) zurück, wenn  _Logicalexpression_ FALSE ist. Andernfalls wird FALSE (0) zurückgegeben. 
  
## <a name="syntax"></a>Syntax

NOT(** *logicalexpression* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Erforderlich  <br/> |**String** <br/> |Der logische Ausdruck, der ausgewertet werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Boolesch
  
## <a name="example"></a>Beispiel

NOT(Höhe \> 0,75 zoll) 
  
Gibt 1 zurück, wenn Höhe kleiner als oder gleich 2 cm ist. Gibt 0 zurück, wenn Höhe größer als 2 cm ist. 
  

