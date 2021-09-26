---
title: IF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
ms.localizationpriority: medium
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Gibt valueiftrue zurück, wenn logicalexpression true ist. Andernfalls wird valueiffalse zurückgegeben.
ms.openlocfilehash: 8364db9622d4e0432544d83c1265e2af0c4b33f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612645"
---
# <a name="if-function"></a>IF Function

Gibt  _valueiftrue_ zurück, wenn  _logicalexpression_ true ist. Andernfalls wird _valueiffalse zurückgegeben._
  
## <a name="syntax"></a>Syntax

IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Erforderlich  <br/> |**String** <br/> |Der auszuwertende Ausdruck.  <br/> |
| _valueiftrue_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Wert, der zurückgegeben werden soll, wenn  _"logicalexpression"_ auf "true" festgelegt ist.  <br/> |
| _valueiffalse_ <br/> |Erforderlich  <br/> |**Variiert** <br/> | Wert, der zurückgegeben werden soll, wenn  _logicalexpression_ auf "false" festgelegt ist.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Variiert
  
## <a name="example"></a>Beispiel

IF(Height \> 1,25 in,5,7)
  
Gibt 5 zurück, wenn die Höhe des Shapes größer als 3 cm ist. Gibt 7 zurück, wenn die Höhe des Shapes kleiner als oder gleich 3 cm ist.
  

