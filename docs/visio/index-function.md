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
description: Gibt die Teilzeichenfolge am nullbasierten Standortindex in der Durch Trennzeichen getrennten Liste zurück. Wenn sich der Index nicht im Bereich befindet, wird auch eine leere Zeichenfolge oder das optionale Token zurückgegeben, das als Argument errorvalue angegeben wird.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431575"
---
# <a name="index-function"></a>INDEX Function

Gibt die Teilzeichenfolge am nullbasierten _Standortindex_ in der durch Trennzeichen getrennten Liste _zurück._  Wenn sich der Index nicht im Bereich befindet, wird auch eine leere Zeichenfolge oder das optionale Token zurückgegeben, das als  *Argument errorvalue angegeben*  wird. 
  
## <a name="syntax"></a>Syntax

INDEX(** *index* **," ** *list* ** "[,[ ** *delimiter* ** ][,[ ** *errorvalue* ** ]]]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Position, die gefunden werden soll.  <br/> |
| _list_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Liste, in der gesucht werden soll.  <br/> |
| _delimiter_ <br/> |Optional  <br/> |**String** <br/> | Die Zeichenfolge, die als Trennzeichen in der Liste verwendet _werden soll._ Eine  _Trennzeichenzeichenfolge_ kann mehr als ein Zeichen lang sein und Mehrbytezeichen enthalten. Das Standardtrennzeichen ist ein Semikolon.  <br/> |
| _errorvalue_ <br/> |Optional.  <br/> |**Number** <br/> | Ein benutzerdefinierter Wert, der zurückgegeben wird, wenn sich der Index außerhalb des gültigen Bereichs befindet. Der Standardwert ist eine leere Zeichenfolge.  <br/> |
   
## <a name="remarks"></a>Hinweise

Ist der Liste ein Trennzeichen voran- bzw. nachgestellt, wird eine leere Zeichenfolge vor bzw. hinter der Liste unterstellt. Aufeinander folgende Trennzeichen implizieren eine eingefügte leere Zeichenfolge. 
  
Liegt der Index nicht im Bereich, gibt Visio eine leere Zeichenfolge oder das optionale Token zurück, das als *Argument errorvalue bereitgestellt* wird. 
  
## <a name="example-1"></a>Beispiel 1

INDEX(3,"cat;rat;; Ziege")
  
Gibt "Ziege" zurück.
  
## <a name="example-2"></a>Beispiel 2

INDEX(54,";1;2;3;",,"ERROR")
  
Gibt "ERROR" zurück.
  

