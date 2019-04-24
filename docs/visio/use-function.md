---
title: USE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: Wendet das Linienmuster, das Füllmuster oder das Linienende namens auf die Form an, wenn es in die Zelle "LinePattern, FillPattern, beginArrow oder Zelle EndArrow gestellt wird.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337149"
---
# <a name="use-function"></a>USE Function

Wendet das Linienmuster, das Füllmuster oder das Linienende __ namens auf die Form an, wenn es in die Zelle "LinePattern, FillPattern, BeginArrow oder Zelle EndArrow gestellt wird. 
  
## <a name="syntax"></a>Syntax

USE ("* * *Name* * *") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die für einen gültigen Master-Shape-Namen steht.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Wenn ein Master- _Name_ in der Dokumentschablone des Dokuments vorhanden ist, wird das Muster als Linienmuster, Füllmuster, anfangs Pfeil oder Endpfeil angewendet. 
  
Diese Funktion gibt immer 254 zurück.
  
## <a name="example"></a>Beispiel

USE("Railroad Tracks") 
  
Formatiert das Shape, indem das Mastermuster namens Railroad Tracks auf das Shape, das die Formel enthält, angewendet wird. 
  

