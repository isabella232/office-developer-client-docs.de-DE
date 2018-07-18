---
title: DEPENDSON-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Erstellt eine Zelle Verweis Abhängigkeit.
ms.openlocfilehash: 07c0d79668230cbf2b1e8d51b50e67835c87e2f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796835"
---
# <a name="dependson-function"></a>DEPENDSON Function

Erstellt eine Zelle Verweis Abhängigkeit.
  
## <a name="syntax"></a>Syntax

DEPENDSON (** *Cellref* ** [, ** *cellref2* **,...]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _CellRef_ <br/> |Erforderlich  <br/> |**String** <br/> |Der erste Zellbezug.  <br/> |
| _cellref2_ <br/> |Optional  <br/> |**String** <br/> |Der zweite Zellbezug.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Funktion gibt immer FALSE zurück. Sie hat keine Auswirkung, wenn Sie in einer Ereigniszeile oder in einer Aktionszelle verwendet wird. 
  
## <a name="example"></a>Beispiel

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
Öffnet den Textblock eines Shapes, sobald sich die Zellen PinX oder PinY des Shapes ändern. 
  

