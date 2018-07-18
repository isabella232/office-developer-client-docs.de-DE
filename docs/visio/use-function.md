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
description: Wendet das Linienmuster, Füllmuster oder Linienende namens Name mit dem Shape in die Zelle LinePattern, FillPattern, BeginArrow oder EndArrow platziert.
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798355"
---
# <a name="use-function"></a>USE Function

Wendet das Linienmuster, Füllmuster oder Linienende namens _Name_ mit dem Shape in die Zelle LinePattern, FillPattern, BeginArrow oder EndArrow platziert. 
  
## <a name="syntax"></a>Syntax

VERWENDEN ("** *Namen* **") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Erforderlich  <br/> |**String** <br/> |Beliebige Zeichenfolge, die für einen gültigen Master-Shape-Namen steht.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Wenn ein Master-Shape mit dem Namen _Name_ in der Dokumentschablone des Dokuments vorhanden ist, wird das Muster als Linienmuster, Füllmuster, PfeilAnfang oder Pfeilende beginnen angewendet. 
  
Diese Funktion gibt immer 254 zurück.
  
## <a name="example"></a>Beispiel

USE("Railroad Tracks") 
  
Formatiert das Shape, indem das Mastermuster namens Railroad Tracks auf das Shape, das die Formel enthält, angewendet wird. 
  

