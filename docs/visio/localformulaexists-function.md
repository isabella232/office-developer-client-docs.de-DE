---
title: LOCALFORMULAEXISTS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
ms.localizationpriority: medium
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Gibt an, ob die zelle, auf die verwiesen wird, eine lokale Formel enthält.
ms.openlocfilehash: 2fdd6e547f1f86491fc84d316237d472e767536b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603655"
---
# <a name="localformulaexists-function"></a>LOCALFORMULAEXISTS Function

Gibt an, ob die zelle, auf die verwiesen wird, eine lokale Formel enthält. 
  
## <a name="syntax"></a>Syntax

LOCALFORMULAEXISTS (** *cellref* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Erforderlich  <br/> |**String** <br/> | Die Zelle, die auf das Vorhandensein einer Formel überprüft werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Boolesch
  
## <a name="remarks"></a>Bemerkungen

Die LOCALFORMULAEXISTS-Funktion gibt 1 zurück, wenn die Zelle eine Formel enthält; wenn keine Formel vorhanden ist oder wenn die Formel übernommen wurde, wird 0 (null) zurückgegeben. 
  

