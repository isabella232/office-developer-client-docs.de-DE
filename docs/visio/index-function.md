---
title: INDEX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
ms.localizationpriority: medium
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Gibt die Teilzeichenfolge am nullbasierten Positionsindex in der Liste zurück, die durch Trennzeichen getrennt ist. Wenn sich der Index außerhalb des Gültigen Bereichs befindet, wird auch eine leere Zeichenfolge oder das optionale Token zurückgegeben, das als Argument "errorvalue" bereitgestellt wird.
ms.openlocfilehash: 09559640a9d3b1d1da730a125024c9a8f4a11699
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628136"
---
# <a name="index-function"></a>INDEX Function

Gibt die Teilzeichenfolge am nullbasierten  _Positionsindex_ in der  _Liste_ zurück, die durch  _Trennzeichen_ getrennt ist. Wenn sich der Index außerhalb des Gültigen Bereichs befindet, wird auch eine leere Zeichenfolge oder das optionale Token zurückgegeben, das als  *Argument "errorvalue"*  bereitgestellt wird. 
  
## <a name="syntax"></a>Syntax

INDEX(** *index* **," ** *list* ** "[,[ ** *delimiter* ** ][,[ ** *errorvalue* ** ]]]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Position, die gefunden werden soll.  <br/> |
| _Liste_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Liste, in der gesucht werden soll.  <br/> |
| _delimiter_ <br/> |Optional  <br/> |**String** <br/> | Die Zeichenfolge, die als Trennzeichen in der  _Liste_ verwendet werden soll. Eine  _Trennzeichenfolge_ kann mehr als ein Zeichen lang sein und Multibyte-Zeichen enthalten. Das Standardtrennzeichen ist ein Semikolon.  <br/> |
| _errorvalue_ <br/> |Optional  <br/> |**Number** <br/> | Ein benutzerdefinierter Wert, der zurückgegeben wird, wenn sich der Index außerhalb des gültigen Bereichs befindet. Der Standardwert ist eine leere Zeichenfolge.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ist der Liste ein Trennzeichen voran- bzw. nachgestellt, wird eine leere Zeichenfolge vor bzw. hinter der Liste unterstellt. Aufeinander folgende Trennzeichen implizieren eine eingefügte leere Zeichenfolge. 
  
Wenn der Index außerhalb des Gültigen liegt, gibt Visio eine leere Zeichenfolge oder das optionale Token zurück, das als *Fehlerwertargument* bereitgestellt wird. 
  
## <a name="example-1"></a>Beispiel 1

INDEX(3,"cat;rat;; ist")
  
Gibt "Ziege" zurück.
  
## <a name="example-2"></a>Beispiel 2

INDEX(54,";1;2;3;","ERROR")
  
Gibt "ERROR" zurück.
  

