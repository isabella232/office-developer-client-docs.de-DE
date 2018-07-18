---
title: NOT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Gibt TRUE (1) zurück, wenn Logicalexpression auf false festgelegt ist. Andernfalls wird FALSE (0) zurückgegeben.
ms.openlocfilehash: e2359aaab18469cd4f272f71aca8d899a12b2120
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797550"
---
# <a name="not-function"></a>NOT Function

Gibt TRUE (1) zurück, wenn _Logicalexpression_ auf false festgelegt ist. Andernfalls wird FALSE (0) zurückgegeben. 
  
## <a name="syntax"></a>Syntax

KEINE (** *Logicalexpression* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Erforderlich  <br/> |**String** <br/> |Der logische Ausdruck, der ausgewertet werden soll.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Boolean
  
## <a name="example"></a>Beispiel

KEINE (Höhe \> 0,75 Zoll) 
  
Gibt 1 zurück, wenn Höhe kleiner als oder gleich 2 cm ist. Gibt 0 zurück, wenn Höhe größer als 2 cm ist. 
  

