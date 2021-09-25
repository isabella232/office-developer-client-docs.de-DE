---
title: DEPENDSON-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
ms.localizationpriority: medium
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Erstellt eine Zellbezugsabhängigkeit.
ms.openlocfilehash: f97ba98cbc5e2a56578b5303583a1d2811242f67
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608235"
---
# <a name="dependson-function"></a>DEPENDSON Function

Erstellt eine Zellbezugsabhängigkeit.
  
## <a name="syntax"></a>Syntax

DEPENDSON(** *cellref* ** [, ** *cellref2* **,...]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Erforderlich  <br/> |**String** <br/> |Der erste Zellbezug.  <br/> |
| _cellref2_ <br/> |Optional  <br/> |**String** <br/> |Der zweite Zellbezug.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion gibt immer FALSE zurück. Sie hat keine Auswirkung, wenn Sie in einer Ereigniszeile oder in einer Aktionszelle verwendet wird. 
  
## <a name="example"></a>Beispiel

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
Öffnet den Textblock eines Shapes, sobald sich die Zellen PinX oder PinY des Shapes ändern. 
  

