---
title: CHAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
ms.localizationpriority: medium
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Gibt das ANSI-Zeichen für eine Zahl zurück.
ms.openlocfilehash: 9e29a518f81a59fcf63313ef06391a4984944d81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603753"
---
# <a name="char-function"></a>CHAR Function

Gibt das ANSI-Zeichen für eine Zahl zurück.
  
## <a name="syntax"></a>Syntax

CHAR(** *number* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Zahl, deren ANSI-Zeichen Sie abrufen möchten.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die resultierende Zeichenfolge ist ein Zeichen lang. Der  _Zahlenparameter_ muss eine ganze Zahl zwischen 1 und 255 (einschließlich) sein, andernfalls gibt die Funktion einen Fehler zurück. 
  
## <a name="example"></a>Beispiel

CHAR(9) 
  
Gibt das Tabulatorzeichen zurück. 
  

