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
description: Erstellt eine Abhängigkeit von Zellverweisen.
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423468"
---
# <a name="dependson-function"></a>DEPENDSON Function

Erstellt eine Abhängigkeit von Zellverweisen.
  
## <a name="syntax"></a>Syntax

DEPENDSON(** *cellref* ** [, ** *cellref2* **,...]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Erforderlich  <br/> |**String** <br/> |Der erste Zellbezug.  <br/> |
| _cellref2_ <br/> |Optional  <br/> |**String** <br/> |Der zweite Zellbezug.  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Funktion gibt immer FALSE zurück. Sie hat keine Auswirkung, wenn Sie in einer Ereigniszeile oder in einer Aktionszelle verwendet wird. 
  
## <a name="example"></a>Beispiel

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
Öffnet den Textblock eines Shapes, sobald sich die Zellen PinX oder PinY des Shapes ändern. 
  

