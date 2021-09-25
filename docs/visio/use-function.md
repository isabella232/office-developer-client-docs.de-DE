---
title: USE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
ms.localizationpriority: medium
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: Wendet das Linienmuster, das Füllmuster oder den Namen des linienenden Namens auf die Form an, wenn sie in der Zelle LinePattern, FillPattern, BeginArrow oder EndArrow platziert wird.
ms.openlocfilehash: 411193444316617e09ee947f34cc4f6a7c49d99e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622654"
---
# <a name="use-function"></a>USE Function

Wendet das Linienmuster, das Füllmuster oder den  _Namen_ des linienenden Namens auf die Form an, wenn sie in der Zelle LinePattern, FillPattern, BeginArrow oder EndArrow platziert wird. 
  
## <a name="syntax"></a>Syntax

USE(" ** *name* ** ") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die für einen gültigen Master-Shape-Namen steht.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Wenn ein benannter  _Mastername_ in der Dokumentschablone des Dokuments vorhanden ist, wird das Muster als Linienmuster, Füllmuster, Anfangspfeil oder Endpfeil angewendet. 
  
Diese Funktion gibt immer 254 zurück.
  
## <a name="example"></a>Beispiel

USE("Railroad Tracks") 
  
Formatiert das Shape, indem das Mastermuster namens Railroad Tracks auf das Shape, das die Formel enthält, angewendet wird. 
  

