---
title: SETATREFEVAL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
ms.localizationpriority: medium
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: Wird im set_expression Parameter der SETATREF-Funktion verwendet, um anzugeben, dass set_expression ausgewertet werden soll, bevor der Verweisparameter in SETATREF zugewiesen wird.
ms.openlocfilehash: 2ce7cd796e97a658911d01f667b538b9294ee4a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559586"
---
# <a name="setatrefeval-function"></a>SETATREFEVAL Function

Wird im  _set_expression_ Parameter der SETATREF-Funktion verwendet, um anzugeben, dass  _set_expression_ ausgewertet werden soll, bevor der  _Verweisparameter_ in SETATREF zugewiesen wird. 
  
## <a name="syntax"></a>Syntax

SETATREFEVAL(** *Expr* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Erforderlich  <br/> |**Variiert** <br/> | Ein Ausdruck, der ausgewertet wird, wenn die SETATREF-Funktion  _set_expression_ zu einer anderen Zelle umleitet.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Beim Zuweisen des *set_expression* Parameters der SETATREF-Funktion zu einer referenzierten Zelle schreibt Microsoft Visio *set_expression* standardmäßig als Ausdruck in die Zelle. Wenn jedoch ein Teil des *set_expression* Parameters von der SETATREFEVAL-Funktion umbrochen wird, wertet Visio den Ausdruck aus und ersetzt die SETATREFEVAL-Funktion durch das Ergebnis, bevor der SETATREF-Ausdruck aufgelöst wird. 
  
## <a name="example"></a>Beispiel

Ein Beispiel finden Sie unter [SETATREF](setatref-function.md)-Funktion. 
  

