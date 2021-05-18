---
title: FORMAT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Gibt das Ergebnis des Ausdrucks als Zeichenfolge zurück, die gemäß formatpicture formatiert ist.
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404652"
---
# <a name="format-function"></a>FORMAT Function

Gibt das Ergebnis des _Ausdrucks_ als Zeichenfolge zurück, die gemäß _formatpicture formatiert ist._
  
## <a name="syntax"></a>Syntax

FORMAT(** *Expression* **," ** *formatpicture* ** ") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Kombination aus Konstanten, Operatoren, Funktionen und Bezügen auf ShapeSheet-Zellen, die einen Wert ergeben.  <br/> |
| _formatpicture_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Formatierungsangabe zum Formatieren der Zeichenfolge.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Hinweise

Der Typ des Ausdrucks und der in der Formatierungsangabe angegebene Typ bestimmen das Verhalten der zurückgegebenen Zeichenfolge. Das  _Formatpicture_ muss für den Ausdruckstyp geeignet sein. Weitere Informationen zum Angeben von Formatbildern finden Sie unter [Informationen zum Formatieren von Bildern](about-format-pictures.md).
  
Gibt einen Fehler zurück, wenn das Ergebnis des Ausdrucks und der in _formatpicture_ erwartete Typ eine andere Art sind oder wenn Syntaxfehler in  _formatpicture vorliegen._
  
## <a name="example-1"></a>Beispiel 1

FORMAT(1cm/4, "0,000 u")
  
Gibt 0,250 cm zurück.
  
## <a name="example-2"></a>Beispiel 2

FORMAT(1cm/4, "0,00 U")
  
Gibt 0,25 cm zurück.
  
## <a name="example-3"></a>Beispiel 3

FORMAT(1cm/4, "0,0 u")
  
Gibt 0.3 cm zurück.
  

