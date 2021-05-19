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
description: Wird im set_expression der SETATREF-Funktion verwendet, um anzugeben, dass set_expression ausgewertet werden soll, bevor sie dem Referenzparameter in SETATREF zugewiesen werden.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432982"
---
# <a name="setatrefeval-function"></a>SETATREFEVAL Function

Wird im _set_expression_ der SETATREF-Funktion verwendet,  um anzugeben, dass set_expression ausgewertet werden  soll, bevor dem Referenzparameter in SETATREF zugewiesen wird. 
  
## <a name="syntax"></a>Syntax

SETATREFEVAL(** *expr* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Erforderlich  <br/> |**Variiert** <br/> | Ein Ausdruck, der ausgewertet wird, wenn die SETATREF-Funktion  _set_expression_ zu einer anderen Zelle umleite.  <br/> |
   
## <a name="remarks"></a>Hinweise

Beim Zuweisen des *set_expression-Parameters* der SETATREF-Funktion zu einer zelle, auf  die verwiesen wird, schreibt Microsoft Visio standardmäßig set_expression in die Zelle als Ausdruck. Wenn jedoch ein Teil des *set_expression-Parameters* von der SETATREFEVAL-Funktion umschlossen wird, wertet Visio den Ausdruck aus und ersetzt die SETATREFEVAL-Funktion durch ihr Ergebnis, bevor der SETATREF-Ausdruck aufgelöst wird. 
  
## <a name="example"></a>Beispiel

Ein Beispiel finden Sie unter [SETATREF](setatref-function.md)-Funktion. 
  

