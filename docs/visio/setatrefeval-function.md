---
title: SETATREFEVAL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: In der Set_expression-Parameter der SETATREF-Funktion verwendet, um anzugeben, dass diese Set_expression berechnet werden soll, bevor Sie Reference-Parameter in SETATREF zuweisen.
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797989"
---
# <a name="setatrefeval-function"></a>SETATREFEVAL Function

In der _Set_expression_ -Parameter der SETATREF-Funktion verwendet, um anzugeben, dass _Set_expression_ vor dem Zuweisen zum _Reference_ -Parameter in SETATREF ausgewertet werden soll. 
  
## <a name="syntax"></a>Syntax

SETATREFEVAL (** *Ausdr* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Erforderlich  <br/> |**Variiert** <br/> | Ein Ausdruck, der ausgewertet wird, wenn die SETATREF-Funktion _Set_expression_ in eine andere Zelle umleitet.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Beim Zuweisen des *Set_expression* -Parameters der SETATREF-Funktion zu einer referenzierten Zelle wird *Set_expression* von Microsoft Visio eine Standard auf die Zelle geschrieben. Wenn ein Teil von *Set_expression* -Parameters durch die SETATREFEVAL-Funktion umbrochen wird, Visio wertet den Ausdruck und ersetzt die SETATREFEVAL-Funktion durch das Ergebnis vor dem Auflösen des SETATREF-Ausdrucks. 
  
## <a name="example"></a>Beispiel

Ein Beispiel finden Sie unter [SETATREF](setatref-function.md)-Funktion. 
  

