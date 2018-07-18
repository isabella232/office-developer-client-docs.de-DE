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
description: Gibt das Ergebnis von Expression als Zeichenfolge entsprechend der Formatierungsangabe formatiert.
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797067"
---
# <a name="format-function"></a>FORMAT Function

Gibt das Ergebnis von _Expression_ als eine _Formatierungsangabe_Zeichenfolge zurück.
  
## <a name="syntax"></a>Syntax

FORMAT (** *Ausdruck* **, "** *Formatierungsangabe* **") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Kombination aus Konstanten, Operatoren, Funktionen und Bezügen auf ShapeSheet-Zellen, die einen Wert ergeben.  <br/> |
| _die Funktion_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Formatierungsangabe zum Formatieren der Zeichenfolge.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Der Typ des Ausdrucks und der in der Formatierungsangabe angegebene Typ bestimmen das Verhalten der zurückgegebenen Zeichenfolge. Die _Formatierungsangabe_ muss für den Typ des Ausdrucks sein. Weitere Informationen zu Formatierungsangaben angeben finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).
  
Gibt einen Fehler zurück, wenn das Ergebnis von _Expression_ und der erwartete Typ in _Formatpicture_ unterschiedlich sind oder wenn _Formatpicture_Syntaxfehler vorhanden sind.
  
## <a name="example-1"></a>Beispiel 1

FORMAT(1cm/4, "0,000 u")
  
Gibt 0,250 cm zurück.
  
## <a name="example-2"></a>Beispiel 2

FORMAT(1cm/4, "0,00 U")
  
Gibt 0,25 cm zurück.
  
## <a name="example-3"></a>Beispiel 3

FORMAT(1cm/4, "0,0 u")
  
Gibt 0.3 cm zurück.
  

