---
title: CHAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Gibt das ANSI-Zeichen für eine Zahl zurück.
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418190"
---
# <a name="char-function"></a>CHAR Function

Gibt das ANSI-Zeichen für eine Zahl zurück.
  
## <a name="syntax"></a>Syntax

CHAR(** *number* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Zahl, deren ANSI-Zeichen Sie erhalten möchten.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die resultierende Zeichenfolge ist ein Zeichen lang. Der  _Parameter number_ muss eine ganze Zahl zwischen 1 und 255 (einschließlich) sein, oder die Funktion gibt einen Fehler zurück. 
  
## <a name="example"></a>Beispiel

CHAR(9) 
  
Gibt das Tabulatorzeichen zurück. 
  

