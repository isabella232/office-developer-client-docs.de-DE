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
description: Wird im set_expression-Parameter der SETATREF-Funktion verwendet, um anzugeben, dass set_expression vor dem Zuweisen zum Verweisparameter in SETATREF ausgewertet werden soll.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432982"
---
# <a name="setatrefeval-function"></a>SETATREFEVAL Function

Wird im _set_expression_ -Parameter der SETATREF-Funktion verwendet, um anzugeben, dass _set_expression_ vor dem Zuweisen zum _Verweis_ Parameter in SETATREF ausgewertet werden soll. 
  
## <a name="syntax"></a>Syntax

SETATREFEVAL (* * *expr* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Erforderlich  <br/> |**Variiert** <br/> | Ein Ausdruck, der ausgewertet wird, wenn die SETATREF-Funktion _set_expression_ in eine andere Zelle umleitet.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie den *set_expression* -Parameter der SETATREF-Funktion einer referenzierten Zelle zuweisen, schreibt Microsoft Visio *set_expression* standardmäßig als Ausdruck in die Zelle. Wenn jedoch ein Teil des *set_expression* -Parameters von der SETATREFEVAL-Funktion umschlossen wird, wertet Visio den Ausdruck aus und ersetzt die SETATREFEVAL-Funktion durch das Ergebnis vor dem Auflösen des SETATREF-Ausdrucks. 
  
## <a name="example"></a>Beispiel

Ein Beispiel finden Sie unter [SETATREF](setatref-function.md)-Funktion. 
  

