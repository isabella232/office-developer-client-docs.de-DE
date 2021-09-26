---
title: FORMAT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
ms.localizationpriority: medium
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Gibt das Ergebnis des Ausdrucks als Zeichenfolge zurück, die entsprechend formatpicture formatiert ist.
ms.openlocfilehash: bc5af650fdb4f5012963206f24a56d4bdd1c2592
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618945"
---
# <a name="format-function"></a>FORMAT Function

Gibt das Ergebnis des  _Ausdrucks_ als Zeichenfolge zurück, die entsprechend  _formatpicture_ formatiert ist.
  
## <a name="syntax"></a>Syntax

FORMAT(** *Ausdruck* **," ** *formatpicture* ** ") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Kombination aus Konstanten, Operatoren, Funktionen und Bezügen auf ShapeSheet-Zellen, die einen Wert ergeben.  <br/> |
| _formatpicture_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Formatierungsangabe zum Formatieren der Zeichenfolge.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Der Typ des Ausdrucks und der in der Formatierungsangabe angegebene Typ bestimmen das Verhalten der zurückgegebenen Zeichenfolge. Die  _Formatierung_ muss für den Ausdruckstyp geeignet sein. Weitere Informationen zum Angeben von Formatbildern finden Sie unter [Informationen zum Formatieren](about-format-pictures.md)von Bildern.
  
Gibt einen Fehler zurück, wenn das Ergebnis des  _Ausdrucks_ und der erwartete Typ in  _"formatpicture"_ einen anderen Typ haben oder wenn Syntaxfehler in  _"formatpicture"_ vorhanden sind.
  
## <a name="example-1"></a>Beispiel 1

FORMAT(1cm/4, "0,000 u")
  
Gibt 0,250 cm zurück.
  
## <a name="example-2"></a>Beispiel 2

FORMAT(1cm/4, "0,00 U")
  
Gibt 0,25 cm zurück.
  
## <a name="example-3"></a>Beispiel 3

FORMAT(1cm/4, "0,0 u")
  
Gibt 0.3 cm zurück.
  

