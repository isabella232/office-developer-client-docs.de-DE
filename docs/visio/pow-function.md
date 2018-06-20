---
title: POW-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Gibt eine Zahl, die potenziert mit einem Exponenten zurück.
ms.openlocfilehash: 48870c679251a666a5756b2b684d262fe059eee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797724"
---
# <a name="pow-function"></a>POW-Funktion

Gibt eine Zahl, die potenziert mit einem Exponenten zurück.
  
## <a name="syntax"></a>Syntax

POW (** *Anzahl* **, ** *Exponent* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Zahl, die mit einem Exponenten potenziert werden soll.  <br/> |
| _Exponent_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Der Exponent.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

_Zahl_ und _Exponent_ können keine ganzen Zahlen sein und kann einen negativen Wert haben. Wenn _Zahl_ nicht gleich 0 und _Exponent_ ist 0, diese Funktion gibt 1 zurück. Wenn _Zahl_ 0 gleich und _Exponent_ negativ ist, gibt diese Funktion 0,0 zurück. Wenn _Zahl_ und _Exponent_ 0 sind oder _Zahl_ negativ und _Exponent_ ist keine Ganzzahl ist, gibt diese Funktion 0,0 zurück. Wenn _Zahl_ und _Exponent_ negativ sind, gibt diese Funktion-1 zurück. #IND. 
  
## <a name="example"></a>Beispiel

POW(5,2) 
  
Gibt 25 zurück. 
  

