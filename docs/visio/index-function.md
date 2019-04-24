---
title: INDEX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Gibt die Teilzeichenfolge am nullbasierten Speicherort Index in der durch Trennzeichen getrennten Liste zurück. Wenn sich der Index außerhalb des gültigen Gültigkeitsbereichs befindet, wird eine leere Zeichenfolge oder das optionale Token zurückgegeben, das als ERRORVALUE-Argument bereitgestellt wird.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344730"
---
# <a name="index-function"></a>INDEX Function

Gibt die Teilzeichenfolge am nullbasierten Speicherort _Index_ in der durch _Trenn_Zeichen getrennten _Liste_ zurück. Wenn sich der Index außerhalb des gültigen Gültigkeitsbereichs befindet, wird eine leere Zeichenfolge oder das optionale Token zurück ** gegeben, das als ERRORVALUE-Argument bereitgestellt wird. 
  
## <a name="syntax"></a>Syntax

Index (* * *Index* * *, * * * *Liste* * * [, [* * *Trennzeichen* * *] [, [* * ERRORVALUE ** * *]]]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Position, die gefunden werden soll.  <br/> |
| _list_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Liste, in der gesucht werden soll.  <br/> |
| _delimiter_ <br/> |Optional  <br/> |**String** <br/> | Die zu verwendende Zeichenfolge in _List_. Eine _Trenn_ Zeichen Zeichenfolge kann mehr als ein Zeichen lang sein und Multibyte-Zeichen enthalten. Das Standardtrennzeichen ist ein Semikolon.  <br/> |
| _ERRORVALUE_ <br/> |Optional  <br/> |**Number** <br/> | Ein benutzerdefinierter Wert, der zurückgegeben wird, wenn sich der Index außerhalb des gültigen Bereichs befindet. Der Standardwert ist eine leere Zeichenfolge.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ist der Liste ein Trennzeichen voran- bzw. nachgestellt, wird eine leere Zeichenfolge vor bzw. hinter der Liste unterstellt. Aufeinander folgende Trennzeichen implizieren eine eingefügte leere Zeichenfolge. 
  
Wenn sich der Index außerhalb des gültigen Gültigkeitszeitraums befindet, gibt Visio eine leere Zeichenfolge oder das optionale ** Token zurück, das als ERRORVALUE-Argument bereitgestellt wird. 
  
## <a name="example-1"></a>Beispiel 1

INDEX (3, "Cat; Rat;; Ziege ")
  
Gibt "Ziege" zurück.
  
## <a name="example-2"></a>Beispiel 2

INDEX (54, "; 1; 2; 3;",, "ERROR")
  
Gibt "ERROR" zurück.
  

