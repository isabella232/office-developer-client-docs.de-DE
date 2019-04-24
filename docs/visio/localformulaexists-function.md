---
title: LOCALFORMULAEXISTS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Gibt an, ob die referenzierte Zelle eine lokale Formel enthält.
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344464"
---
# <a name="localformulaexists-function"></a>LOCALFORMULAEXISTS Function

Gibt an, ob die referenzierte Zelle eine lokale Formel enthält. 
  
## <a name="syntax"></a>Syntax

LOCALFORMULAEXISTS (* * *CellRef* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _CellRef_ <br/> |Erforderlich  <br/> |**String** <br/> | Die Zelle, die auf das Vorhandensein einer Formel überprüft werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Boolesch
  
## <a name="remarks"></a>Bemerkungen

Die LOCALFORMULAEXISTS-Funktion gibt 1 zurück, wenn die Zelle eine Formel enthält; wenn keine Formel vorhanden ist oder wenn die Formel übernommen wurde, wird 0 (null) zurückgegeben. 
  

