---
title: FORMATEX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Gibt das Ergebnis von Expression in SrcUnit als Zeichenfolge ausgewertet formatiert entsprechend Format wurde.
ms.openlocfilehash: 08d123967272e0ab4e25990bcfab55cc80cef55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797069"
---
# <a name="formatex-function"></a>FORMATEX-Funktion

Gibt das Ergebnis von Expression in SrcUnit als Zeichenfolge ausgewertet formatiert entsprechend Format wurde.
  
## <a name="syntax"></a>Syntax

FORMATEX (** *Ausdruck* **, "** *Format* **", [** *SrcUnit* **], [** *DstUnit* **], [** *LangID* **] [, ** *CalID* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Kombination aus Konstanten, Operatoren, Funktionen und Bezügen auf ShapeSheet-Zellen, die einen Wert ergeben.  <br/> |
| _format_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Formatierungsangabe zum Formatieren der Zeichenfolge verwendet. Weitere Informationen zu Formatierungsangaben finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).  <br/> |
| _srcUnit_ <br/> |Optional  <br/> |**String** <br/> | Einheiten zum Auswerten von Expression (in, cm usw.).  <br/> |
| _dstUnit_ <br/> |Optional  <br/> |**String** <br/> |Einheiten, die für das Ergebnis von Expression (in, cm usw.) verwendet.  <br/> |
| _langID_ <br/> |Optional  <br/> |**Nummer** <br/> |Die Sprache, die beim Formatieren von Datums-/Zeitangaben in Microsoft Office System verwendet wird.  <br/> |
| _calID_ <br/> |Optional  <br/> |**Nummer** <br/> |Der Kalender, der beim Formatieren von Datums-/Zeitangaben in Microsoft Office System verwendet wird.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

String
  
## <a name="remarks"></a>Hinweise

Der Typ des Ausdrucks und der in der Formatierungsangabe angegebene Typ bestimmen das Verhalten der zurückgegebenen Zeichenfolge. Das Format muss für den Typ des Ausdrucks.
  
Das Argument SrcUnit wird verwendet, um die Ergebnisse nicht typisierter Ausdruck, wie etwa 3 + 4 skalieren. Wenn das Ergebnis von Expression ausdrücklich einen Typ besitzt, wird beispielsweise 3 ft + 8 ft, SrcUnit ignoriert.
  
Das Argument DstUnit wird verwendet, um die Maßeinheiten für das formatierte Ergebnis bestimmt. Wenn DstUnit nicht angegeben ist, werden die Einheiten für das Ergebnis des Ausdrucks verwendet.
  
Gibt ein Fehler, wenn das Ergebnis von Expression und der erwartete Typ in Format unterschiedlich sind Wenn formatPicture Syntaxfehler im Format, oder wenn es nicht erkennt, dass die Einheiten als SrcUnit oder DstUnit übergeben.
  
## <a name="example"></a>Beispiel

FORMATEX(5.5, "0,00 u", "cm", "ft") 
  
Gibt 0,18 Fuß zurück. 
  

