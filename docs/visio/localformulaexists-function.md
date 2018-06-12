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
ms.openlocfilehash: 1b749011de8554cb5b777fe92b20a6bcdb2fcb19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797368"
---
# <a name="localformulaexists-function"></a>LOCALFORMULAEXISTS Function

Gibt an, ob die referenzierte Zelle eine lokale Formel enthält. 
  
## <a name="syntax"></a>Syntax

LOCALFORMULAEXISTS (** *Cellref* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _CellRef_ <br/> |Erforderlich  <br/> |**String** <br/> | Die Zelle, die auf das Vorhandensein einer Formel überprüft werden soll.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Boolescher Wert
  
## <a name="remarks"></a>Bemerkungen

Die LOCALFORMULAEXISTS-Funktion gibt 1 zurück, wenn die Zelle eine Formel enthält; wenn keine Formel vorhanden ist oder wenn die Formel übernommen wurde, wird 0 (null) zurückgegeben. 
  

