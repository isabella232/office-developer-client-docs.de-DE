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
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796610"
---
# <a name="char-function"></a>CHAR Function

Gibt das ANSI-Zeichen für eine Zahl zurück.
  
## <a name="syntax"></a>Syntax

CHAR (** *Anzahl* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Anzahl, dessen ANSI-Zeichen, die Sie abrufen möchten.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die resultierende Zeichenfolge wird einem Zeichen besteht. Der _Anzahl_ -Parameter muss eine ganze Zahl zwischen 1 und 255 (einschließlich) sein, oder die Funktion gibt einen Fehler zurück. 
  
## <a name="example"></a>Beispiel

CHAR(9) 
  
Gibt das Tabulatorzeichen zurück. 
  

